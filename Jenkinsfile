node {
    checkout scm
    docker.image('node:lts-buster-slim').withRun('-p 3000:3000').inside() {
        stage('Build') {
            sh 'npm install'
        }
        stage('Test') {
            sh './jenkins/scripts/test.sh'
        }
    }
   
}