pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                checkout scm
            }
        }

        stage('Deploy HTML') {
            steps {
                sh '''
                    echo "Creating deploy directory..."
                    sudo mkdir -p /var/www/html/portfolio

                    echo "Copying files..."
                    sudo cp -r * /var/www/html/portfolio/
                '''
            }
        }
    }
}


