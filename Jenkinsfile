pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'returnStdout: true, script: 'env'
                sh 'echo "your test deployment worked!" > /var/jenkins/readme.out'
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
