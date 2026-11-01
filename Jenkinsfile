pipeline{
    agent any
    stages{
        stage('Fetch the code'){
            steps{
                git branch:'main', url:'https://github.com/Tarigondasiva/vprofile-devops',
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
