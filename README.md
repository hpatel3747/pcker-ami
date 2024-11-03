## pcker-ami : packer is hashicorp tool for creating machine images from source configuration
1. install packer

#### install yum config-manager to manage your  repos
```text
sudo yum install -y yum-utils
```
add repos
```text
sudo yum-config-manager --add-repo https://rpm.releases.hashicorp.com/RHEL/hashicorp.repo
```
install
```text
sudo yum -y install packer
```
verify
```text
packer
```
packer is hashicorp tool for creating machine images from source configuration
2. Initialize packer configuration
```text
packer init ec2-pkr.hcl
```
3. run the packer build command providing your image template file
```text
packer build ec2-pkr.hcl
```
- note AMI id , you will need to pass it into your terraform configuration step
4. Deploy your packer image with Terraform
```text
Add the AMI id in the main.tf file
initiate and apply terrafrom script
```
