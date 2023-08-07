pipeline{
    agent any
    stages{
        stage("Checkout of the code"){
            steps{
                sh 'git clone https://github.com/ghulk123/java-code1.git'
            }
           
        }
        stage("maven compile"){
            steps{
                sh 'mvn compile'
            }
           
        }
        stage("maven test"){
            steps{
                sh 'mvn test'
            }
           
        }
        stage("maven package"){
            steps{
                sh 'mvn package'
            }
           
        }
    }
   
}