pipeline {
    agent any
    stages {
         stage("Checkout stage") {
      steps {
        git 'https://github.com/sanjaypjana/terraform-pipelines'
      }
    }
    stage ("terraform init") {
            steps {
                bat 'terraform init'
            }
        }
        stage ("terraform plan") {
            steps {
                bat 'terraform plan'
            }
        }
        stage ("terraform apply") {
            steps {
                bat 'terraform apply --auto-approve'
            }
        }
        }}
