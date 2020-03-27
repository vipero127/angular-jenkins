node {
  try {
    stage('Checkout') {
      echo "checkout scm"
    checkout scm
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
}
