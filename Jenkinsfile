stage('Build'){
sh "${mavenHome}/bin/mvn clean package"
}
/*
stage('ExecuteSonarQubeReport'){
sh "${mavenHome}/bin/mvn clean sonar:sonar"
}

stage('UploadArticatIntoNexus'){
sh "${mavenHome}/bin/mvn clean deploy"
}

stage('DeployAppIntoTomcat'){
sshagent(['ac89ce9e-3ee7-4891-9a42-75e608e5e10a']) {
  sh "scp -o StrictHostkeyChecking=no target/maven-web-application.war ec2-user@172.31.15.70:/opt/apache-tomcat-9.0.91/webapps/"
}
}
*/
}
