# provision-eks-cluster-with-terraform
This repository helps you provision a cluster in AWS EKS using Terraform
Requires active AWS account
Note that using this will charge your AWS account.  EKS is more expensive than ec2.

# Deploying the cluster
This is a development cluster meant for practicing skills.
To deploy this run the following:

terraform init
terraform plan #optional
terraform validate #optional: if you make changes
terraform fmt #optional: if you make changes
terraform apply --auto-approve 

# Removing the Cluster
When you are done with the cluster and want to remove it run the following:

terraform destroy --auto-approve

# Additional Commands
For additonal commands run the following

terraform --help