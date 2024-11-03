## pcker-ami 
1. packer is hashicorp tool for creating machine images from source configuration
2. Initialize packer configuration
```text
packer init ec2-pkr.hcl
```
3. run the packer build command providing your iimage template file
```text
packer build ec2-pkr.hcl
```
- note AMI id , you will need to pass it into your terraform configuration step
4. Deploy your packer image with Terraform
```text
Add the AMI id in the main.tf file
initiate and apply terrafrom script
```
