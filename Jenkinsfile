pipeline {
    agent any
    
    stages {
        stage('Test') {
            steps {
                echo 'Building..'
                sh "wget https://github.com/sbt/sbt/releases/download/v0.13.15/sbt-0.13.15.tgz"
                sh "tar xf sbt-0.13.15.tgz"
                sh "pwd"
                sh "ls"
                sh "cd /var/jenkins_home/jobs/sample-maven-job/workspace/"
                sh "sbt assembly"
            }
        }
    } 
}
