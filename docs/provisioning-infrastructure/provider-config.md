# What is a terraform provider?

- In Terraform, providers are plugins that interact with APIs of various cloud platforms, services, or third-party systems. They enable Terraform to manage resources and infrastructure across different platforms in a consistent manner. This allows terraform to operate in a cloud agnostic manner.

## How to configure your provider?

- As a prerequisite ensure that you have installed terraform and set up an account for whatever cloud platform you are using with the relevant credentials.

- Refer to the docs of the provide and follow the ''' use provider ''' instructions.

- Lets use AWS for example. The documentation for using the AWS provider can simply be found at https://registry.terraform.io/providers/hashicorp/aws/latest/docs. The configuration provided ''' terraform {
  required_providers {
  aws = {
  source = "hashicorp/aws"
  version = "5.29.0"
  }
  }
  }

provider "aws" {} ''' can simply be copied into a provider.tf file.

- Finally running ''' terraform init ''' in order to download and install all the plugins for the provider from the terraform registry.
