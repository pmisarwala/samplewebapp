node {
    stage "CHECKOUT"
   echo 'Hello World'
   checkout([$class: 'GitSCM', branches: [[name: '*/master']], browser: [$class: 'GithubWeb', repoUrl: ''], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/pmisarwala/samplewebapp.git']]])

    stage "Build"
    def mvnHome = tool 'M3'
    sh "$mvnHome/bin/mvn -B verify"
    echo 'This is the build stage'
}
