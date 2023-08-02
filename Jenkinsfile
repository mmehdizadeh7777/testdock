pipeline {
  agent any
  options {
    buildDiscarder(logRotator(numToKeepStr: '5'))
  }
  environment {
    DOCKERHUB_CREDENTIALS = credentials('dockerhub')
  }
  stages {
    stage('Build') {
      steps {
        sh 'docker build -t mmehdizadeh7777/jenkins-docker-hub .'
      }
    }
    stage('Login') {
      steps {
        sh 'echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u $DOCKERHUB_CREDENTIALS_USR --password-stdin'
      }
    }
    stage('Push') {
      steps {
        sh 'docker push mmehdizadeh7777/jenkins-docker-hub'
      }
    }
    stage ('Pull') {
      steps {
	sh 'docker pull mmehdizadeh7777/jenkins-docker-hub'
      }
   }
   
   stage ('Run') {
	steps {
	  sh 'docker run -i mmehdizadeh7777/jenkins-docker-hub'
      }
   }
  }
  post {
    always {
      sh 'docker logout'
    }
  }
}
