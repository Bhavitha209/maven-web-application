node{
    echo "Job Name is:  ${env.JOB_NAME}"
    echo "Node Name is: ${env.NODE_NAME}"
   def mavenHome = tool name: 'maven3.8.5'

//Get the code from Github Repo
stage('CheckoutCode'){
git branch: 'development', credentialsId: '33f0a274-7b60-4d55-a160-8a798fabd978', url: 'https://github.com/Bhavitha209/maven-web-application.git'

}

//Do  the build by suing Maven Build tool
stage ('Build'){
sh "${mavenHome}/bin/mvn clean package"
}

/*
//Execute the SonarQube Report
stage ('ExecutetheSonarQubeReport'){
sh "${mavenHome}/bin/mvn sonar:sonar"
}

//Upload Artifacts into Artifactory Repo
stage ('UploadArtificatsintoNexus'){
sh "${mavenHome}/bin/mvn deploy"
}
//Deploying the Applocation into Tomcat Server
stage('DeployApplication into Tomcat Server'){
sshagent(['53d860d0-cf81-45b5-82f6-4acca67b1d08']) {
sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@3.111.170.95:/opt/apache-tomcat-9.0.62/webapps/"
}
    
}
*/

}

