pipeline {
    agent any
    
    stages {
        stage('init') {
      steps {
        script {
         def sbtHome = tool 'sbt-0.13.15'
         env.sbt= "${sbtHome}/bin/sbt -no-colors -batch"
        }
      }
    }
    stage('Build') {
        steps {
          sh "${sbt} 'set test in assembly := {}' assembly"
          archive includes: 'target/scala-*/toto.jar'
        }
    }
    } 
}
