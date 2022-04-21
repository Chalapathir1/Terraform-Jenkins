pipeline{
    agent any
    environment {
        PATH = "${PATH}:${getTerraformPath()}"
    }
    stages{
        stage("Terraform-init and apply" ){
            steps{
                sh "terraform init"
                sh "terraform apply -var-file=dev.tfvara -auto-approve"
            }
        }
    }
}

def getTerraformPath(){
  def tfHome = tool name: 'terraform-1', type: 'org.jenkinsci.plugins.terraform.TerraformInstallation'
  return tfHome
}
