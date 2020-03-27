/* node {
  try {
    stage('Checkout') {
      echo "checkout scm"
    }
    stage('Environment') {
      sh 'git --version'
      sh 'npm --version'
    } 
    stage('Build') {
      echo "npm install"
    } 
  }
  catch (err) {
    throw err
  }
} */
/* pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo "Hello World"'
                sh 'npm --version'
                sh 'npm install'
            }
        }
    }
}*/


pipeline {
    agent {
        docker {
            image 'node:13.11' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'npm install' 
            }
        }
    }
}