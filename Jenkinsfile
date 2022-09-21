pipeline {
    agent any
    stages {
    stage ("terraform init") {
            steps {
                sh ('terraform init')
            }
        }
        stage ("terraform plan") {
            steps {
                sh ('terraform init')
            }
        }
        stage ("terraform init") {
            steps {
                sh ('terraform apply --auto-approve')
            }
        }
        }}
