node{
    
def mavenHome = tool name: "maven3.6.3"    

stage('CheckoutCode'){
git branch: 'development', credentialsId: 'f84471ac-b9d7-4d5a-980b-28aee7880325', url: 'https://github.com/Sujayjk/maven-web-application.git'
}

stage('Build'){
sh "${mavenHome}/bin/mvn clean package"
}
/*
stage('ExecuteSonarQubeReport'){
sh "${mavenHome}/bin/mvn sonar:sonar"
}
stage('UploadArtifactIntoNexus'){
sh "${mavenHome}/bin/mvn deploy"
}
stage('DeployAppIntoTomcatServer'){
sshagent(['98a34273-d178-4ae5-9e81-6ba7f388d788']) {
    sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@13.233.114.38:/opt/apache-tomcat-9.0.50/webapps/"
	}
}
stage('SendEmailNotification'){
emailext body: '''Build over..!

Regards
Sujay jk
Seoyon E Hwa penukonda''', subject: 'Build over!!', to: 'sujaydevops99@gmail.com,jskubsad1960@gmail.com'
}
*/
}
