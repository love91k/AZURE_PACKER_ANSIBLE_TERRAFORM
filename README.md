# AZURE_PACKER_ANSIBLE_TERRAFORM

Ansible, Packer, and Terraform Demo
===

## Usage

Prior to running, make sure you have both packer and terraform installed.

STEP 1 )
git clone https://github.com/love91k/azure_packer_ansible_erraform.git
cd azure_packer_ansible_terraform


STEP 1 )
az login
az group create -n mywebResourceGroup-l eastus
az ad sp create-for-rbac --query "{ client_id: appId, client_secret: password, tenant_id: tenant }"
az account show --query "{ subscription_id: id }"

put the client id  client seceret , tenant id and subscription id in variable section in packer/myweb_image.json



STEP 2)
cd packer
packer packer/myweb_image.json

STEP 3) 
cd ../terraform
terraform init 
terraform plan
terraform apply 

check the webpage page on  returned fullly qualifed name from terraform apply 


terraform destroy 

