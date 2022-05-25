pipeline{
    agent any
    tools{
        maven 'MAVEN'
    }
    stages {
        stage('Build Maven') {
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: '83c4959c-80f9-4ffe-ae84-9250a40ff26e', url: 'https://github.com/jainshreeyans/jenkins-docker-example.git']]])
                sh "mvn -Dmaven.test.failure.ignore=true clean package"
                
            }
        }
    }
}
