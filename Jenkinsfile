pipeline {
    agent any

    stages {
        stage('build') {
            steps {
                 sh 'docker build -t test/jenkins-docker-hub .'
            }
        }
         stage('test') {
            steps {
                echo 'testing...'
            }
        }
        stage('deploy') {
            steps {
                echo 'deploying...'
            }
        }
    }
}
