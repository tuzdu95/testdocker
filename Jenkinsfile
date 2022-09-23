pipeline {
    agent any
    stages {
        stage('Stage one') {
            steps {
                script {
                    echo "Parameter from template creation: " + templateParams.someParam
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