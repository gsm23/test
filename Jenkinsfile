pipeline {
  agent any
  stages {
    stage('Prepare') {
      steps {
        echo 'Starting the Pipeline'
      }
    }
    stage('') {
      steps {
        parallel(
          "build test": {
            sh '''echo "Lets execute the unit test....."
pwd
uname -a'''
            sleep 5
            
          },
          "pull git": {
            sh 'git clone https://github.com/gsm23/python_projects'
            
          }
        )
      }
    }
    stage('Deploy') {
      steps {
        sh '''echo "Lets deploy"
ls -lR
'''
      }
    }
  }
}