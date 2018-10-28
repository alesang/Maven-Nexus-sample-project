pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat 'mvn clean package'
            }
        }
        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }
    }

    post {
        always {
            archiveArtifacts artifacts: '/**/*.jar', fingerprint: true
            //junit '/**/*.xml'
            //a
        }
    }
}
