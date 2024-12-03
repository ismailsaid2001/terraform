
pipeline {
    agent any
    stages {
        stage('Terraform Init') {
            steps {
                dir('infrastructure') {
                    sh 'terraform init'
                }
            }
        }
        stage('Terraform Plan') {
            steps {
                dir('infrastructure') {
                    sh 'terraform plan'
                }
            }
        }
        stage('Terraform Apply') {
            steps {
                dir('infrastructure') {
                    sh 'terraform apply -auto-approve'
                }
            }
        }
    }
}
