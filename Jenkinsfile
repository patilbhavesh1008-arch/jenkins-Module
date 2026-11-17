pipeline {
    agent any

    stages {
        stage('Git Checkout') {
            steps {
                echo 'Git Checkout successful - webhook Test'
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

        stage('Docker') {
            steps {
                echo 'Docker Stage Successful'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment Successful'
            }
        }
    }
}
// Testing automatic webhook trigger
