pipeline {
    agent any

    stages {
      /*  stage('github clone') {
            steps {
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/malleshdevops/devops17-eks.git']])
            }
        }*/
        stage('terraform init') {
            steps {
              sh 'terraform init'    
            }
        }
        stage('terraform validate') {
            steps {
                sh 'terraform validate'
            }
        }
        stage('terraform plan') {
            steps {
                sh 'terraform plan'
            }
        }
        stage('terraform apply') {
            steps {
                sh 'terraform destroy --auto-approve'
            }
        }
    }
}
