pipeline {
    agent any
    stages {
        stage('Build') {
          steps {
            sh './mvnw package'
          }
        }

        stage('Email') {
                      steps {
                        emailext(subject: 'Build Passed!', body: 'Build Passed!', from: 'davidberard2@gmail.com', to: 'davidberard2@gmail.com')
                      }
                    }

        stage('Test') {
          steps {
            sh 'mvn test'
          }
        }

        stage('Email') {
                      steps {
                        emailext(subject: 'Test Passed!', body: 'Test Passed!', from: 'davidberard2@gmail.com', to: 'davidberard2@gmail.com')
                      }
                    }

        stage('Package') {
          steps {
            sh 'mvn package'
          }
        }

        stage('Email') {
                      steps {
                        emailext(subject: 'Package Passed!', body: 'Package Passed!', from: 'davidberard2@gmail.com', to: 'davidberard2@gmail.com')
                      }
                    }

        stage('Deploy') {
          steps {
            sh 'mvn deploy'
          }
        }
        
        stage('Email') {
                      steps {
                        emailext(subject: 'Deploy Passed!', body: 'Deploy Passed!', from: 'davidberard2@gmail.com', to: 'davidberard2@gmail.com')
                      }
                    }
    }
}
