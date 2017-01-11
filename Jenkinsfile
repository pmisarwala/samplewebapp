node{
    stage "CHECKOUT"
   echo 'Hello World'
   git url: 'https://github.com/pmisarwala/samplewebapp.git', branch: 'master'

   stage "Build"
    def mvnHome = tool 'M3'
   env.PATH = "${mvnHome}/bin:${env.PATH}"
 sh 'mvn -B verify'
 step([$class: 'ArtifactArchiver', artifacts: '**/target/*.jar', fingerprint: true])
  step([$class: 'JUnitResultArchiver', testResults: '**/target/surefire-reports/TEST-*.xml'])
    echo 'This is the build stage'
}

