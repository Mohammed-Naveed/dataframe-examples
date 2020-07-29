pipeline {
    agent any
  environment {
      SBT_HOME = tool name: 'sbt-0.13.15', type: 'org.jvnet.hudson.plugins.SbtPluginBuilder$SbtInstallation'
      PATH = "${env.SBT_HOME}/bin:${env.PATH}"
    }

    stages {
        stage('Build') {
            steps {
                echo "Compiling..."
                sh "wget https://github.com/sbt/sbt/releases/download/v0.13.15/sbt-0.13.15.tgz"
                sh "tar xf sbt-0.13.15.tgz"
                sh "sudo mv sbt /opt"
                sh "export PATH=$PATH:/opt/sbt/bin"
                sh "whereis sbt"
                sh "ls"
                sh "sbt assembly"
            }
        }
    }
}
