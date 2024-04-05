# CICD-k8-Terraform
![image](https://github.com/rogerbarrow/CICD-k8-Terraform/assets/46138186/1cd6cdef-769d-4720-ac5f-a6abc0cbfb29)
# Step 1
* Use Terraform to Create an ec2 Instance for Jenkins, Docker and SonarQube
* `` resource "aws_instance" "web" {
  ami                    = "ami-0287a05f0ef0e9d9a"      #change ami id for different region
  instance_type          = "t2.large"
  key_name               = "Linux-VM-Key7"              #change key name as per your setup
  vpc_security_group_ids = [aws_security_group.Jenkins-VM-SG.id]
  user_data              = templatefile("./install.sh", {})

  tags = {
    Name = "Jenkins-SonarQube"
  }

  root_block_device {
    volume_size = 40
  }
}

resource "aws_security_group" "Jenkins-VM-SG" {
  name        = "Jenkins-VM-SG"
  description = "Allow TLS inbound traffic"

  ingress = [
    for port in [22, 80, 443, 8080, 9000, 3000] : {
      description      = "inbound rules"
      from_port        = port
      to_port          = port
      protocol         = "tcp"
      cidr_blocks      = ["0.0.0.0/0"]
      ipv6_cidr_blocks = []
      prefix_list_ids  = []
      security_groups  = []
      self             = false
    }
  ]

  egress {
    from_port   = 0
    to_port     = 0
    protocol    = "-1"
    cidr_blocks = ["0.0.0.0/0"]
  }

  tags = {
    Name = "Jenkins-VM-SG"
  }
}
``
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
