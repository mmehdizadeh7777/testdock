pipeline {
    agent any

    stages {
        stage('build') {
            steps {
                sh """
		pwd
		docker build -f Dockerfile -t testimage -
		"""
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
