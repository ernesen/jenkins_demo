pipeline {
    agent {
        docker { image 'ernesen/migratecf:2.0' }
    }
    stages {
        stage('Test Java') {
            steps {
                // send build started notifications
                slackSend (color: '#FFFF00', message: "STARTED: Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]' (${env.BUILD_URL})")
                sh 'java -version'
            }
        }
        stage('More Maven') {
            steps {
                sh 'mvn -v'
            }
        }
        stage('More docker') {
            steps {
                sh 'docker version'
            }
        }
    }
}
