pipeline {
    agent any

    stages {
        stage('build') {
            steps {
                sh "docker build -t testimage -"
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
