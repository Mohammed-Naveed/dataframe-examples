pipeline {
    agent any
    
    stages {
        stage('Test') {
            steps {
                echo 'Building..'
                
                
                sh "pwd"
                sh "ls"
                
                
                sh "sbt assembly"
            }
        }
    } 
}
