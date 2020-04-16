pipeline {
    agent any
    stages {
        stage('Build') {
          steps {
            sh './mvnw package'
          }
        }

        stage('Test') {
          steps {
            echo 'Test'
          }
        }

        stage('Package') {
          steps {
            echo 'Package'
          }
        }

        stage('Deploy') {
          steps {
            echo 'Deploy'
          }
        }

        stage('Email') {
                      steps {
                        emailext(subject: 'All Passed!', body: 'All Passed!', from: 'tryh814@gmail.com', to: 'davidberard2@gmail.com')
                      }
                    }
    }
}
