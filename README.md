# provision-eks-cluster-with-terraform
This repository helps you provision a cluster in AWS EKS using Terraform

# Requirements
- AWS account
- Installed kubernetes-cli 
- IDE like VScode
- Git

For the kubernetes-cli, open a powershell terminal as the administrator on your windows workstation.
Run the following:

```
choco install kubernetes-cli -y
```

If successful you should get the version with the following command while still on
powershell as the administrator:

```
 kubectl version
 Client Version: v1.30.3
 ```

# Deploying the cluster
Will take approximately 10-20 minutes.

```
mdkir ~/dev_eks_cluster
git clone https://github.com/skrajewski1/dev_eks_0001.git
cd ~/dev_eks_cluster
terraform init
terraform apply --auto-approve
```

After the cluster comes online you will need to run the following with the cluster name.
The cluster name will be part of the outputs after terraform completes.  Add the region switch
to be safe incase you are working in multiple regions.

```
aws eks update-kubeconfig --name cluster_name --region us-east-1
```

# Removing the cluster

```
terraform destroy --auto-approve
```

