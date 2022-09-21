pipeline {
    agent any
    stages {
         stage('Checkout stage') {
      steps {
        git 'https://github.com/sanjaypjana/cloud-customers-docker'
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
        stage ("terraform init") {
            steps {
                sh ('terraform apply --auto-approve')
            }
        }
        }}
