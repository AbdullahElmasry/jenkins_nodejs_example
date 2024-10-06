pipeline {
    agent any

    stages {
        stage('CI') {
            steps {
                git "https://github.com/AbdullahElmasry/jenkins_nodejs_example.git"
                // Building the Dockerfile
                sh 'docker build . -t node-app:$BUILD_NUMBER'
            }
                post {
                    success {
                        echo "Build successfully"
                    }
                    failure {
                        echo "Build failed"
                    }
            }
        }
    }
}

