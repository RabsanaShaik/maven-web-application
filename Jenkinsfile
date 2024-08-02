node{
echo "the job name is: ${env.JOB_NAME}"
echo "the node name is: ${env.NODE_NAME}"
def mavenHome = tool name: 'maven3.9.7'
stage('checkoutcode'){
git branch: 'development', credentialsId: '09e62cc3-3dbd-4a7b-b415-ed32bef126e4', url: 'https://github.com/RabsanaShaik/maven-web-application.git'
}

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
