#!groovy

pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo sh(returnStdout: true, script: 'env')

                echo 'Testing pipeline: Creating temp.out...'
                //sh (script: 'touch /var/jenkins/readme.out')
                sh (script: 'touch /home/ec2-user/readme.out')
                sh (script: 'echo "your test deployment worked!!!" >> /var/jenkins/readme.out')
                //sh ('/bin/touch /var/jenkins/readme.out')
                //sh ('echo "your test deployment worked!!!" > /var/jenkins/readme.out')
                echo 'Testing pipeline: Test successful!'
                
                echo 'Pulling from the GitHub master branch...'
                
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
    post {
        always {
            cleanWs()
        }
    }
}
