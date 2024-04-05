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

# from the Script
 * Docker is install
 * Jenkins is install
 * Trivy is install
 * ![image](https://github.com/rogerbarrow/CICD-k8-Terraform/assets/46138186/9fd858e4-9a60-436e-8b85-af67a7f502db)

# Step 7 Configure Jenkins
  *get the Public IP and access port 8080
  * ![image](https://github.com/rogerbarrow/CICD-k8-Terraform/assets/46138186/ee6f8053-0cc5-4ec2-a0c9-69c96e5c2ec3)

![image](https://github.com/rogerbarrow/CICD-k8-Terraform/assets/46138186/95bbc921-201b-46f3-9bf0-288d97502943)
 lets down the required plugins
   * eclipse temurin install
   * Sonarqube Scanner
   *  Sonar gates
   *  Docker
   *  Node.js
   * ![image](https://github.com/rogerbarrow/CICD-k8-Terraform/assets/46138186/dc083e1e-3e32-4280-ba82-3c108c61ad5d)
# Step 8 Download tools
 * Install nodejs
 * Install JDK
 * install Docker
 * Install sonar
 * ![image](https://github.com/rogerbarrow/CICD-k8-Terraform/assets/46138186/04c9ed38-a6ef-4633-b4a6-46e5f378776c)
# Configure SonarQube and Integrate SonarQube with Jenkins
  * ![image](https://github.com/rogerbarrow/CICD-k8-Terraform/assets/46138186/5b79b714-2fbf-4140-aef6-9ed10ba10784)
  * ![image](https://github.com/rogerbarrow/CICD-k8-Terraform/assets/46138186/59f091b5-a2b3-4103-928f-40b2da5d0780)
# Create Jenkins pipeline to build and push dokcer image to Dockerhub
  * ![image](https://github.com/rogerbarrow/CICD-k8-Terraform/assets/46138186/6696bc3a-ae1f-4961-bdc6-01babda053b9)
  * ![image](https://github.com/rogerbarrow/CICD-k8-Terraform/assets/46138186/10017ce0-6fe0-4eb2-acbe-13db9b037027)
  *![image](https://github.com/rogerbarrow/CICD-k8-Terraform/assets/46138186/95a89b6d-b03a-4d05-801f-18459aa5c08e)

