# What is IAC?

IAC stands for Infrastructure as code. It is surprisingly quite self explanatory and is the concept of treating infrastructure provisioning, configuration, and management as code.

Before diving into what Terraform does or is there is an important distinction that needs to be made between Infrastructure Orchestration and Configuration Management.

## Infrastructure Orchestration vs Config management:

- Terraform, Cloudformation are infrastructure orchestration tools which means they can provision servers and infrastructure by themselves.

- Ansible,chef and puppet are config management tools hence designed to configure and manage software on existing servers. They streamline tasks such as software installation, updates, and enforcing desired system states across multiple machines.

- Config management tools can do some infrastructure provisioning but better fit for other tasks.
