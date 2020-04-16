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
    }

    post {

        success {
            mail to: 'davidberard2@gmail.com',
                 subject: "Sucess Pipeline",
                 body: "Something is good"
        }

        failure {
            mail to: 'davidberard2@gmail.com',
                 subject: "Failed Pipeline",
                 body: "Something is wrong"
        }
    }
}
