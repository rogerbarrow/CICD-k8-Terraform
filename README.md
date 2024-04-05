# CICD-k8-Terraform
![image](https://github.com/rogerbarrow/CICD-k8-Terraform/assets/46138186/1cd6cdef-769d-4720-ac5f-a6abc0cbfb29)
# Step 1
* Use Terraform to Create an ec2 Instance for Jenkins, Docker and SonarQube

# Step 2
  * Create main.tf file with correct AMI for your region
 * ![image](https://github.com/rogerbarrow/CICD-k8-Terraform/assets/46138186/391d0338-7094-45a0-9d9e-cc9b4259d134)
# Step 3
 * Create a provider.tf file
  * ![image](https://github.com/rogerbarrow/CICD-k8-Terraform/assets/46138186/d6b99a5b-eaf2-4d8c-aa6f-264e9b6993af)
  # Step 4 
  * Create a install.sh file
  * this will update package, Install Docker, Install jdk, Jenkins and run SonarQube
![image](https://github.com/rogerbarrow/CICD-k8-Terraform/assets/46138186/57dd36b5-a96f-4b66-9cc9-bbb97411a3ee)
# Step 5 Login to AWS 
* with Your acess Key and Secret Key
* ![image](https://github.com/rogerbarrow/CICD-k8-Terraform/assets/46138186/aefe37db-c126-421f-a448-28cb5f1ef7b6)
# Step 6 run Terraform
    * terraform init
    * terraform plan
    * terraform apply -auto-approve
    
  * ![image](https://github.com/rogerbarrow/CICD-k8-Terraform/assets/46138186/30044cb7-346c-49c2-b86d-31d275895428)
* ![image](https://github.com/rogerbarrow/CICD-k8-Terraform/assets/46138186/2a5dac22-0e87-4506-b2c7-3e3304f5735f)
# Login to AWS to verify EC2 is runnning
 *![image](https://github.com/rogerbarrow/CICD-k8-Terraform/assets/46138186/d4218d66-9d00-47df-9db5-4793ae187aea)
 * ![image](https://github.com/rogerbarrow/CICD-k8-Terraform/assets/46138186/5c459695-c232-42be-b41a-9d6b43efbafe)
# Step 7 SSH into the Instance 
![image](https://github.com/rogerbarrow/CICD-k8-Terraform/assets/46138186/2872cde7-7f40-48bb-b77e-5266cf4541e3)
* ![image](https://github.com/rogerbarrow/CICD-k8-Terraform/assets/46138186/f2eeccf5-ba32-4baa-a3d2-65b274aaa3cc)



