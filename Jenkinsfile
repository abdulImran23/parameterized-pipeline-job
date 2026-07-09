/******  BRANCH - main  *****/
pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean package -DskipTests=true'
                archiveArtifacts 'target/hello-demo-*.jar'
            }
        }
        stage('Containerization') {
            steps {
                sh 'echo Docker Build Image..'
                sh 'echo Docker Tag Image....'
                sh 'echo Docker Push Image......'
            }
        }
        stage('Integration Testing') {
            steps {
                sh 'sleep 10s'
                sh 'echo Testing using cURL commands......'
            }
        }
    }
}
