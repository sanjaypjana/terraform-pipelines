pipeline {
    agent any
    tools {
  terraform 'Deploy-Iac'
}
    stages {
         stage("Checkout stage") {
      steps {
        git 'https://github.com/sanjaypjana/terraform-pipelines'
      }
    }
        
        stage('Handshake') {
      steps {
        withCredentials([aws(accessKeyVariable: 'AWS_ACCESS_KEY_ID', credentialsId: 'AKIAX6213AGRU2WUURCR', secretKeyVariable: 'AWS_SECRET_ACCESS_KEY')]) {
        }
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
