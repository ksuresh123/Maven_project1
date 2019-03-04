pipeline {
    agent any
    
    stages {
        stage('Ok') {
            steps {
                echo "Ok"
            }
        }
    }
    post {
        always {
            emailext body: 'A Test EMail', recipientProviders: [[$class: 'sureshconfi12345@gmail.com'], [$class: 'sureshconfi12345@gmail.com']], subject: 'Test'
        }
    }
}
