// Jenkinsfile
node('master') {
  stage 'dev'
    git url: 'https://github.com/jglick/simple-maven-project-with-tests.git', branch: 'master'
    def mvnHome = tool 'M3'
    sh "${mvnHome}/bin/mvn -B verify"
  stage 'qa'
    sh "${mvnHome}/bin/mvn -B verify"
  stage 'prod'
    sh "${mvnHome}/bin/mvn -B verify"
}
