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
      sh "npm install"
      sh "npm run build"
      sh "docker login -u \"ganatan\" -p \"Trustno1982Beastmaster\" docker.io"
      sh "docker build -t helloimage:1.0.0 ."
      sh "docker tag helloimage:1.0.0 ganatan/angular-example-starter:1.0.0"
      sh "docker push ganatan/angular-example-starter:1.0.0"
    } 
  }
  catch (err) {
    throw err
  }
}
