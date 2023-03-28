node
{

  def mavenHome=tool name: "maven3.6.3"
  
 stage('Checkout')
 {
 	git credentialsId: 'ebc00fd9-71e6-4733-9585-ca4104f98e2b', url: 'https://github.com/Sandeep6478/https-github.com-MithunTechnologiesDevOps-maven-web-application.git'
 
 }
 /*
 stage('Build')
 {
 sh  "${mavenHome}/bin/mvn clean package"
 }
 
 stage('ExecuteSoanrQubeReport')
 {
 sh  "${mavenHome}/bin/mvn sonar:sonar"
 }
 
 stage('UploadArtifactintoNexus')
 {
 sh  "${mavenHome}/bin/mvn deploy"
 }
 
 stage('DeployAppintoTomcat')
 {
 sshagent(['cd93d61f-2d0f-4c60-8b33-34cf4fa888b0']) {
  sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@172.31.48.143:/opt/apache-tomcat-9.0.73/webapps/"
 }
 }
*/
 stage('SendEmailNotification')
 {
 emailext body: '''Build is over..

 Regards,
 Mithun Technologies,
 9980923226.''', subject: 'Build is over', to: 'devopstrainingblr@gmail.com'
 }
}
