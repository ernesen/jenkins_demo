pipeline {
    agent {
        docker { image 'ernesen/migratecf:2.0' }
    }
    stages {
        stage('Test Java') {
            steps {
                sh 'java -version'
            }
        }
        stage('More Maven') {
            steps {
                sh 'mvn -v'
            }
        }
        stage('More helm') {
            steps {
                sh 'helm version --short'
            }
        }
    }
}
