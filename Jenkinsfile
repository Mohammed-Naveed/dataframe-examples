pipeline {
    agent{
    node {
  def sbtHome = tool 'sbt-0.13.15'
  def sbt = "${sbtHome}/bin/sbt -no-colors -batch"
  stage('build') {
    sh "${sbt} clean assembly"
  }
    }

    }
}
