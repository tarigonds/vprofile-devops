pipeline{
    agent any
    stages{
        stage('Fetch the code'){
            steps{
                git branch:'main', url:'git@github.com:tarigonds/vprofile-devops.git',
                    credentialsId: 'github'
                
            }
        }
        stage('Build'){
            steps{
                sh 'mv install'
            }
        }
        stage('Test'){
            steps{
                sh 'mvn test'
            }
        }
    }
}
