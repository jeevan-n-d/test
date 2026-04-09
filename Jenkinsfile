pipeline {
    agent none

    stages {

        stage('build') {
            agent { label 'DevServer' }
            steps {
                echo "Running on ${env.NODE_NAME}"
                sh 'hostname'
            }
        }

        stage('test') {
            agent { label 'DevServer' }
            steps {
                echo "Testing..."
            }
        }

        stage('deploy') {
            agent { label 'ProdServer' }
            steps {
                echo "Deploying on ${env.NODE_NAME}"
                sh 'hostname'
            }
        }
    }
}