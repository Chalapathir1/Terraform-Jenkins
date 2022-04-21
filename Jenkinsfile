pipeline{
    agent any
    environment {
        PATH = "${PATH}:${getTerraformPath()}"
    }
    stages{
        stage("Terraform-init"){
            steps{
                sh "terraform init"
            }
        }
    }
}

def getTerraformPath(){
  def tfHome = tool name: 'terraform-1', type: 'org.jenkinsci.plugins.terraform.TerraformInstallation'
  return tfHome
}
