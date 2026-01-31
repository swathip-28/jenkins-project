pipeline {
    agent any

    stages {

        stage('Download Code') {
            steps {
                echo "Code downloaded"
            }
        }

        stage('Build Docker Image') {
            steps {
                bat "docker build -t myimage ."
            }
        }

        stage('Run Website') {
            steps {
                bat "docker run -d -p 8081:80 myimage"
            }
        }
    }
}
