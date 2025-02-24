pipeline {
    agent any

    environment {
        DOCKER_IMAGE = "hardikverma3044/mr-react-app"
        CONTAINER_NAME = "goofy_leaderberg"
        DEPLOY_PORT = "3000"
    }

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/erHardikVerma/Dockerized-React-App-with-Nginx.git'
            }
        }

        stage('Install Dependencies & Build') {
            steps {
                bat '''
                call npm install
                call npm run build
                '''
            }
        }

        stage('Build Docker Image') {
            steps {
                bat "docker build -t %DOCKER_IMAGE%:latest ."
            }
        }

        stage('Run Nginx Server') {
            steps {
                bat '''
                docker stop %CONTAINER_NAME% || exit 0
                docker rm %CONTAINER_NAME% || exit 0
                docker run -d -p %DEPLOY_PORT%:80 --name %CONTAINER_NAME% %DOCKER_IMAGE%
                '''
            }
        }
    }
}
