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
                sh "sbt -Dsbt.global.base=.sbt -Dsbt.boot.directory=.sbt -Dsbt.ivy.home=.ivy2 assembly"
                sh "ls"
                sh "cd target
                sh "ls"
            }
        }
    } 
}
