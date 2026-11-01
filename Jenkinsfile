pipeline {
    agent any
    stages{

        stage('Fetch Code') {
            steps {
                git branch: 'paac', url: 'git@github.com:tarigonds/vprofile-devops.git', credentialsId: 'github'
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
}
