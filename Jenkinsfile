pipeline{
    agent any
    tools {
        terraform 'terraform-11'
    }
    stages{
        stage('Terraform init'){
            steps{
                sh 'terraform init'
            }
        }
        stage('Terraform apply'){
            steps{
                sh 'terraform apply -var="name=params.bucket_name" --auto-approve'
            }
        }
    }
}
