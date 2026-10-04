pipeline {
    agent any

    options {
        timestamps()
    }

    stages {

        stage('Git Integration Test') {
            steps {
                echo 'GitHub → Jenkins integration is working!'
                sh 'git --version'
                sh 'git branch --show-current || true'
                sh 'echo Jenkins build triggered successfully'
            }
        }

        stage('AWS Access Test') {
            steps {
                echo 'Testing Jenkins → AWS access through EC2 IAM role...'

                sh '''
                    set -e

                    aws sts get-caller-identity
                    aws configure list

                    echo "AWS access from Jenkins is working."
                '''
            }
        }

        stage('EKS Access Test') {
            steps {
                echo 'Testing Jenkins → EKS access...'

                sh '''
                    set -e

                    aws eks describe-cluster \
                        --region ap-south-1 \
                        --name streamingapp-cluster \
                        --query 'cluster.name' \
                        --output text

                    kubectl get nodes

                    echo "Jenkins → EKS connectivity is working."
                '''
            }
        }

    }

    post {
        success {
            echo 'Sprint 1 Jenkins pipeline completed successfully.'
        }

        failure {
            echo 'Sprint 1 Jenkins pipeline failed. Check the stage output.'
        }
    }
}