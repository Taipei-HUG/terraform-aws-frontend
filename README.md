# terraform-aws-frontend

This terraform module is for aws terraform workshop [CH04](https://github.com/Taipei-HUG/workshop/tree/master/aws/ch04), the main purpose is for demonstrating how to use Terragrunt


## What AWS Resource Created

Before using this module, please confirm a ssh key pair in ~/.ssh/ with the name id_rsa.pub and id_rsa, this example use the key pair for frontend instance. And this module mainly creates below two items

### AWS Auto Scaling Group
There is one AWS auto scaling group to launch frontend EC2 instance, but it's just for demo usage, hence, from the user_data in provisoin folder can be found, there is only install nginx.

### AWS Elastic Load Balancer‎
In order to let multiple frontend ec2 instances can be accessed publicly, hence the EC2 frontend instances which created by the AWS auto scaling group need to be bind to load balancer

