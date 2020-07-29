pipeline {
    agent any
     environment {
      SBT_HOME = tool name: 'sbt.13.13', type: 'org.jvnet.hudson.plugins.SbtPluginBuilder$SbtInstallation'
      PATH = "${env.SBT_HOME}/bin:${env.PATH}"
    }
    
    stages {
        stage('Test') {
            steps {
                echo 'Building..'
               // sh "wget https://github.com/sbt/sbt/releases/download/v0.13.15/sbt-0.13.15.tgz"
                
                sh "sbt assembly"
            }
        }
    } 
}
