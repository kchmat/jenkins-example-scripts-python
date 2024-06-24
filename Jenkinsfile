pipeline {
  agent any
  stages {
      stage('Install Dependencies') {
            steps {
                script {
                    // Installer pip si ce n'est pas déjà fait
                    sh "apt-get update && apt-get install -y python3-pip"

                    // Installer pywinrm
                    sh "pip3 install pywinrm"
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
