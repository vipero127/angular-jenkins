node {
  try {
    stage('Checkout') {
      echo "checkout scm"
    checkout scm
    }
    stage('Environment') {
      sh 'git --version'
      sh 'npm --version'
      sh 'docker version'
    } 
    stage('Build') {
      echo "Build"
/*      sh "npm install"
      sh "npm run build"*/
    } 
  }
  catch (err) {
    throw err
  }
}
