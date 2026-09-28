pipeline{
    agent any
    stages{
        stage("Build"){
            steps{
                sh 'mvn clean package'
            }
        }
        stage("Deploy"){
            steps{
                deploy adapters: [tomcat8(alternativeDeploymentContext: '', credentialsId: 'da7545c6-a5bb-4e27-acd9-f4ba731db76a', path: '', 
                url: 'http://ec2-43-204-141-113.ap-south-1.compute.amazonaws.com:8080/')], 
                contextPath: 'javawebapp', war: '**/java-web-project.war'
            }
        }        
    }
}    
