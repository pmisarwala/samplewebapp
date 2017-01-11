node {
    stage "CHECKOUT"
   echo 'Hello World'
   git url: 'https://github.com/pmisarwala/samplewebapp.git', branch: 'master'

   stage "Build"
    def mvnHome = tool 'M3'
   env.PATH = "${mvnHome}/bin:${env.PATH}"
 sh 'mvn -B verify'
    echo 'This is the build stage'
}
node{
echo 'this is test node' > myfile1
}

