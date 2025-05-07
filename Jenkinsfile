pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/Sneha-S-U/portfolio.git'
            }
        }

        stage('Deploy HTML') {
            steps {
                // Copy files to web directory - adjust the path if needed
                sh 'mkdir -p /var/www/html/portfolio'
                sh 'cp -r * /var/www/html/portfolio'
            }
        }
    }
}
