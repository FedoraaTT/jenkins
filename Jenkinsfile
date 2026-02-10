pipeline{
    agent any


        

    stages{
        stage('Build'){
            steps{
                echo 'Building the application...'
                bat 'docker build -t python-app .'
            }
        }
        stage('Test'){
            steps{
                echo 'Running tests...'
                bat 'docker run -rm python-app pytest'
            }
        }
        stage('Deploy'){
            steps{
                echo 'Deploying the application...'
                bat 'docker run -rm python-app'
            }
        }
    }

}





