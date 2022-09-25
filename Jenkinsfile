pipeline {
    agent any
    stages {
        stage('Stage one - edited') {
            steps {
                script {
                    echo "Parameter from template creation: "
                }
            }
        }
        stage('Stage two - Clone') {
            steps {
                script {
                    git 'https://github.com/tuzdu95/testdocker.git'
                }
            }
        }
        stage('Stage three - Build and push') {
            steps {
                script {
                    withDockerRegistry(credentialsId: 'dockerhub', url: 'https://index.docker.io/v1/') {
                        sh 'docker build -t tuzdu1202/testpipeline'
                        sh 'docker push tuzdu1202/testpipeline'
                    }
                }
            }
        }
    }
}