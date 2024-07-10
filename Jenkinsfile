pipeline {
  agent any
  stages {
      stage('Install Dependencies') {
            steps {
                script {
                    // Installer pip si ce n'est pas déjà fait
                    //sh "yum update && yum install -y python3-pip"
                    sh "sudo apt-get update"
                    // Installer pywinrm
                    //sh "pip3 install pywinrm"
                }
            }
        }
    stage('version') {
      steps {
        sh 'python3 --version'
      }
    }
    stage('hello') {
      steps {
        sh 'python hello.py'
      }
    }
  }
}
