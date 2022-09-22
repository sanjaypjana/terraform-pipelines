pipeline {
    agent any
    stages {
        stage("Hello") {
         steps {
            def tfHome = tool name: 'Terraform', type: 'com.cloudbees.jenkins.plugins.customtools.CustomTool'
            env.Path = "${tfHome};${env.Path}"
            bat 'terraform --version'
            echo 'Hello World'
         }
      }
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
