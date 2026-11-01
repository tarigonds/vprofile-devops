pipeline{
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
        stage('Test'){
            steps{
                sh 'mvn test'
            }
     
        }
    }
}

    
