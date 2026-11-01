pipeline{
    agent any
    stages{
       
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
