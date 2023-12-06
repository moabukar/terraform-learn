# Terraform state file -

The terraform state file can be described as the backbone of your terraform configuration. It is your record of reality and serves as a reflection of your existing infrastructure.

It is very important to understand the relationship between your terraform configuration (desired state) and your existing infrastructure (current state).

## Desired vs current state:

- Terraforms primary function is to create, modify or destroy infrastructure resources to match the desired stated described in your terraform config.

- Current state is the actual state of resource that has been deployed. E.g deploying an EC2 t2.micro instance 'resource "aws_instance" "myec2" {
  ami = "ami-05d72852800cbf29e"
  instance_type = "t2.micro"
  }' and then modifying it in the AWS console to t2.medium. The desired state will remain as a t2.micro and current state as t2.medium. Hence running a terraform plan will indicate a change destroying the t2.medium instance and reverting it back to the desired t2.micro instance.

- Terraform tries to ensure that infrastructure code is based on desired state. If there is difference between the two, terraform plan presents the changes neccessary to achieve desired state.

- In order to check if the current state is the same as the desired state run a 'terraform plan' and you should receive a prompt back saying “No changes. Infrastructure up to date”.
