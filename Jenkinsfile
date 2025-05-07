pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                checkout([$class: 'GitSCM',
                    branches: [[name: '*/main']],
                    userRemoteConfigs: [[
                        url: 'https://github.com/Sneha-S-U/portfolio.git'
                    ]]
                ])
            }
        }

        stage('Deploy HTML') {
            steps {
                sh 'sudo mkdir -p /var/www/html/portfolio'
                sh 'sudo cp -r * /var/www/html/portfolio'
            }
        }
    }
}


