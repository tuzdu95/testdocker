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
    }
}