pipeline {
    agent any
    stages{

        stage('Fetch Code') {
            steps {
                git branch: 'paac', url: 'https://github.com/devopshydclub/vprofile-project.git'
            }
        }
        stage('BUILD'){
            steps {
                sh 'mvn clean install -DskipTests'
            }
            post {
                success {
                    echo 'Now Archiving...'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }

        stage('UNIT TEST'){
            steps {
                sh 'mvn test'
            }
        }
    }
}pipeline{
    agent any
    stages{
        stage('Fetch') {
            steps {
                git branch:'main', url: 'git@github.com:tarigonds/vprofile-devops.git', credentialsId: 'github'
            }
        }
        stage('Build'){
            steps{
                sh 'mvn clean install -DskipTests'
            }
        }
          post {
            sucess{
                echo 'Now Archiving...'
                    archiveArtifacts artifacts: '**/target/*.war'
            }
        }
    }
        stage('Test'){
            steps{
                sh 'mvn test'
            }
     
        }
    
}

    
