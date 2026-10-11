pipeline {
  agent any
  tools {
      go 'go_test'
  }
  environment {
      GO111MODULE='on'
  }
  
  stages {
    stage('Test') {
      steps {
        git 'https://github.com/Shaikh-naveed-ahmed/ci-cd-demo.git'
        sh 'go test ./...'
      }
    }
    stage('Build') {
        steps {
        git 'https://github.com/Shaikh-naveed-ahmed/ci-cd-demo.git'
        sh 'go build .'
        }
    }
    stage('Run') {
        steps {
            sh 'cd /var/lib/jenkins/workspace/full-cicd-go2 && go-webapp-sample &'
        }
    }

  }
}
