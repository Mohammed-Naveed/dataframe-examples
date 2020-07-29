pipeline {
    agent {
        docker {
            image 'bigtruedata/sbt'
        }
    }
    stages {
        stage('Test') {
            steps {
                echo 'Building..'
                sh "sbt test"
            }
        }
    } 
}
