node {
  try {
    stage('Checkout') {
      echo "checkout scm"
    }
    stage('Environment') {
      sh 'git --version'
      sh 'npm --version'
    } 
  }
  catch (err) {
    throw err
  }
}
