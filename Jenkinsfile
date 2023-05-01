node{
    def mavenHome = tool name = "maven3.9.1"
    echo " The Node Name is : {$env.NODE_NAME}"
    echo " The Build Number is : {$env.BUILD_NUMBER}"
    echo " The Job Name is : {$env.JOB_NAME}"
    
//checkout stage
    stage("Checkout Code"){
    git branch: 'main', credentialsId: '3738e079-bce9-46da-9c02-e4ac90d5afe0', url: 'https://github.com/Fazakarim007/maven-web-application.git'
    }
    
//Build Stage
    stage("Build"){
    sh "$mavenHome/bin/mvn clean package"
    }
/*    
//SonarQube Reports Generation
    stage("Code Coverage"){
    sh "$mavenHome/bin/mvn sonar:sonar"    
    }
    
//Upload Artifacts to Nexus
    stage("Nexus Artifacts"){
    sh "$mavenHome/bin/mvn deploy"
    }
    
//Deploy Apps into Tomcat Server
    stage("Deploy Applications"){
    sshagent(['cc293b24-fe89-4fd6-8552-5c794c7b9293']){
    sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@65.2.11.20:/opt/apache-tomcat-9.0.74/webapps"
    }
    }
*/
}
