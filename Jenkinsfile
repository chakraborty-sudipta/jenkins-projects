pipeline {
    agent any 

    stages { 

        stage('Build docker image') {
            steps {  
                sh 'docker build -t sudip2024/flaskapp:$BUILD_NUMBER .'
            }
        }

        stage('login to dockerhub') {
            steps {
                withCredentials([usernamePassword(credentialsId: 'dockerhub', 
                                                 usernameVariable: 'DOCKER_USER', 
                                                 passwordVariable: 'DOCKER_PASSWORD')]) {
                    sh 'echo $DOCKER_PASSWORD | docker login -u $DOCKER_USER --password-stdin'
                }
            }
        }

        stage('push image') {
            steps {
                sh 'docker push ylmt/flaskapp:$BUILD_NUMBER'
            }
        }
    }
    
    post {
        always {
            sh 'docker logout'
        }
    }
}
