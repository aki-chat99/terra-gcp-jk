pipeline {
  agent any
  stages {
    stage('intialize') {
      steps {
        echo 'creating gcp infra by terraform'
      }
    }
    stage('build infra') {
      steps {
        echo 'build infra by terraform'
        ws(dir: '/var/lib/jenkins/demo1') {
          sh '''cd /var/lib/jenkins/demo1
pwd
./iac_gcp.sh
'''
        }
        
      }
    }
  }
}