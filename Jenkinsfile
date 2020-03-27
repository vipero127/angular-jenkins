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
            image 'node:latest' 
            args '-p 3000:3000' 
            args '-u 0:0'
        }
    }
    environment {
        DISABLE_AUTH = 'true'
        DB_ENGINE    = 'sqlite'
    }
    stages {
        stage('Build') { 
            steps {
                echo "0001"
                deleteDir()
                echo "0002"
                sh 'node --version' 
                echo "0003"
//                sh 'npm install' 
//                sh 'npm run build' 
            }
        }
    }
}