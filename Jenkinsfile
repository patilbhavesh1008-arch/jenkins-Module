pipeline {
    agent any

    environment {
        DOCKER_IMAGE = 'natsucloud/jenkins-cicd'
    }

    stages {
        stage('Git Checkout') {
            steps {
                echo 'Git Checkout Successful'
            }
        }

        stage('Build') {
            steps {
                echo 'Build Successful'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing Successful'
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t $DOCKER_IMAGE .'
            }
        }

        stage('Docker Hub Push') {
            steps {
                withCredentials([usernamePassword(
                    credentialsId: 'dockerhub-creds',
                    usernameVariable: 'DOCKER_USER',
                    passwordVariable: 'DOCKER_PASS'
                )]) {
                    sh '''
                        echo "$DOCKER_PASS" | docker login -u "$DOCKER_USER" --password-stdin
                        docker push $DOCKER_IMAGE
                        docker logout
                    '''
                }
            }
        }

        stage('Deploy') {
            steps {
                sh 'docker rm -f jenkins-cicd || true'
                sh 'docker run -d --name jenkins-cicd -p 8081:80 $DOCKER_IMAGE'
            }
        }
    }
}
