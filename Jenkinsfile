pipeline {
    agent any
    stages {
         stage('Checkout stage') {
      steps {
        git 'https://github.com/sanjaypjana/terraform-pipelines'
      }
    }
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
        stage ("terraform apply") {
            steps {
                sh ('terraform apply --auto-approve')
            }
        }
        }}
