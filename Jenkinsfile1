pipeline {
    agent any
    stages {
        stage("Checkout") {   
            steps {               	 
                git branch: 'master', url: 'https://github.com/Ramkhushi/java-code1.git'        	 
            }    
        }
        stage('Maven Clean') {
            steps {
                sh "mvn clean"  	 
            }
        }
        stage('Maven Build') {
            steps {
                sh "mvn compile"  	 
            }
        }
        stage("Unit Test") {          	 
            steps {  	 
                sh "mvn test"          	 
            }
        }
        stage("Maven Package") {
            steps {
                sh "mvn package"
            }
        }
        stage('deploy to tomcat') {
            steps {
              deploy adapters: [tomcat9(credentialsId: 'admin1', path: '', url: 'http://34.125.35.76:8080')], contextPath: 'app12', war: '**/target/*.war'
            }
        }
    }
}   


 
 


