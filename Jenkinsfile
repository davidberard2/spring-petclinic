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
            sh 'mvn test'
          }
        }

        stage('Package') {
          steps {
            sh 'mvn package'
          }
        }

        stage('Deploy') {
          steps {
            sh 'mvn deploy'
          }
        }

        stage('Email') {
              steps {
                emailext(subject: 'Build Passed!', body: 'Build Passed!', from: 'davidberard2@gmail.com', to: 'davidberard2@gmail.com')
              }
            }
    }
}
