# Terraform always comes up with a plan!

- Following our understanding of state files it is important to know what our outputed plan represents. It reads the current state of any already-existing remote objects to make sure that the Terraform state is up-to-date. If not the plan will suggest to either create, change or destroy resources to reach the desired state.

- This command is simply executed by running `terraform plan`

- When operating with large scale infrastructure it can be very inconvenient filtering through very large plans. If you would like to have a granular approach you can simply use the `- target` flag for the relevant resource.

- The `plan` command alone does not actually carry out the proposed changes
