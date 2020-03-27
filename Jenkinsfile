node {
  try {
    stage('Checkout') {
      echo "checkout scm"
    }
    stage('Environment') {
      sh 'git --version'
      sh 'npm --version'
    } 
    stage('Build') {
      sh 'npm install'
    } 
  }
  catch (err) {
    throw err
  }
}
