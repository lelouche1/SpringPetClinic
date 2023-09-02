pipeline{
    agent any
    tools{ maven 'M3'}
    stages{
        
        stage('checkout'){
            steps{
                git branch: 'main', url: 'https://github.com/lelouche1/SpringPetClinic.git'
            }
        }
        stage('build'){
            steps{
             sh 'mvn compile'   
            }
        }
        stage('package'){
            steps{
                sh 'mvn package'
            }
        }
        stage('deploy'){
            steps{
                sh 'java -jar /var/lib/jenkins/workspace/petClinicDeclaratif/target/*.jar'
            }
        }
    }
}
