pipeline {
    agent {
        label 'Jenkins-Demo-Agent'
    }
            
    stages {

        stage('Deploy to Server') {
            steps {
                script {
                        sh 'docker compose -f docker-compose.yaml up -d'
                        sh 'docker ps'
                   
                }
            }
        }

        
    }
    post {
        always {
                sh 'docker image prune -a --force'
        }
    }
}
