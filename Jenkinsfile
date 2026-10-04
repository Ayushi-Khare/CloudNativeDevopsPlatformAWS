pipeline {
    agent any

    stages {
        stage('Git Integration Test') {
            steps {
                echo 'GitHub → Jenkins integration is working!'
                sh 'git --version'
                sh 'echo Jenkins build triggered successfully'
            }
        }
    }
}
