pipeline {
    agent any
    stage('build da imagem docker'){
        stephs{
            sh 'docker build -t devops/app .'
        }
    }
    stage('subir docker compose - redis e app'){
        stephs{
            sh 'docker-compose up --build -d'
        }
    }
    stage('sleep para subida de containers'){
        stephs{
            sh 'sleep 10'
        }
    }
    stage('teste da aplicação'){
        stephs{
            sh 'teste-app.sh'
        }
    }
}