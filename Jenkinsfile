pipeline{
    agent any
    stages{
        stage('Fetch Cod'){
            steps{
                git branch: 'main', url: 'git@github.com:tarigonds/vprofile-devops.git',
                    credentialsId: 'github'
       
        stage('Build'){
            steps{
                sh 'mvn install'
            }
        }
        stage('Test'){
            steps{
                sh 'mvn test'
            }
        }
    }
}
    }
}
