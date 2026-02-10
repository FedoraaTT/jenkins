pipeline{
    agent any

    environment {
        DOCKER = "C:\Program Files\Docker\Docker\resources\bin\docker.exe"
    }
        
    }

    stages{
        stage('Build'){
            steps{
                echo 'Building the application...'
                bat '%DOCKER% build -t python-app .'
            }
        }
        stage('Test'){
            steps{
                echo 'Running tests...'
                bat '%DOCKER% run python-app pytest'
            }
        }
        stage('Deploy'){
            steps{
                echo 'Deploying the application...'
                bat '%DOCKER% run  python-app'
            }
        }
    }

}
