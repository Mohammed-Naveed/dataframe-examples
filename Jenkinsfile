node {
   stage('Git') {
      git 'https://github.com/Mohammed-Naveed/dataframe-examples.git'
   }
   stage('Build') {
       def builds = [:]
       builds['scala'] = {
           // assumes you have the sbt plugin installed and created an sbt installation named 'sbt-0.13.13'
           sh "${tool name: 'sbt-0.13.13', type: 'org.jvnet.hudson.plugins.SbtPluginBuilder$SbtInstallation'}/bin/sbt compile test"
       }
       builds['frontend'] = {
           echo 'building the frontend'
       }
     parallel builds
   }
   stage('Results') {
      junit '**/target/test-reports/*.xml'
   }
}
