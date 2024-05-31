# Terraform Beginners Guide

<img alt="Terraform" src="https://www.datocms-assets.com/2885/1629941242-logo-terraform-main.svg" width="600px">  

<!-- ![tf word cloud](./imgs/01-tf-word-cloud.png)  -->

- ### [00-Terraform-Basics](00-Terraform-Basics) - Terraform Definitions and more

- ### [02-Terraform-Terminologies](02-Terraform-Terminologies)

    - **Provider** : Define the providers like AWS, Azure, GCP
    - **Resource** : Infrastructure Resources to be created, ex: VPC, S3, EC2
    - **Data Sources** (optional) : Pull the data from the provider
    - **Variable**: Give user option to enter the value for defined resources
    - **Arguments** : Inputs
    - **Attributes** : Outputs
    - **Meta-Arguments** : Terraform specific Inputs ex: count, for_each,depends_on

- ### [03-Terraform-Top-Level-Blocks](03-Terraform-Top-Level-Blocks) - Terraform Top Level Blocks
    - **Terraform Block** (>0.13 version) or Terraform Settings Block or Terraform Configuration Block 
    - **Provider Block**
    - **Resource Block**
    - **Input Variables Block**
    - **Output Values Block**
    - **Local Values Block**
    - **Data Sources Block**
    - **Modules Block**


- ### [04-Terraform-Commands](04-Terraform-Commands) - Basic Terraform Commands
    - *`terraform init`*
    - *`terraform validate`*
    - *`terraform plan`*
    - *`terraform apply`* or *`terraform apply -auto-approve`*
    - *`terraform destroy`* or *`terraform destroy -auto-approve`*


- ### [05-Terraform-Resources](05-Terraform-Resources) - Understanding Resource behavior
    - ***created***
    - ***destroyed*** 
    - ***updated***

- ### [06-Terraform-Resource-Meta-Arguments](06-Terraform-Resource-Meta-Arguments) - Terraform Meta-Arguments
    1. [***`count`***](07-Terraform-Resource-Meta-Arguments/08-01-count/)
    2. [***`for_each`***](07-Terraform-Resource-Meta-Arguments/08-02-for_each/) 
    3. [***`depends_on`***](07-Terraform-Resource-Meta-Arguments/08-03-depends_on/)
    4. [***`provider`***](07-Terraform-Resource-Meta-Arguments/08-04-provider/) 
    5. [***`lifecycle`***](07-Terraform-Resource-Meta-Arguments/08-05-lifecycle/)

- ### [07-Terraform-Variables](07-Terraform-Variables) - Terraform Variables
    1. [**Terraform Variables with `default` Option**](07-Terraform-Variables/)
    2. [**Overriding `default` Variable values with `-var` Option**](07-Terraform-Variables/)
    3. [**Overriding `default` Variable values with `Environment Variables` Options**](07-Terraform-Variables/)
    4. [**Overriding `default` Variable values with `terraform.tfvars` file**](07-Terraform-Variables/07-01-Terraform-Variables-tfvars/)
    5. [**Overriding `default` Variable values with different `.tfvars` using *`-var-file`* Option**](07-Terraform-Variables/07-02-Terraform-Variables-tfvars-var-file/)
    6. [**Terraform Variables type *list***](07-Terraform-Variables/07-03-Terraform-Variables-list/)
    7. [**Terraform Variables type *map***](08-Terraform-Variables/07-04-Terraform-Variables-map/)
    8. [**Custom Validation Rules**](/08-Terraform-Variables/07-05-Custom-Validation-Rules/)
    9. [**Sensitive Variables**](/08-Terraform-Variables/07-06-Sensitive-Variables/)

- ### [08-Terraform-Outputs](08-Terraform-Outputs) - Terraform Output Values

- ### [09-Terraform-Data-Sources](09-Terraform-Data-Sources) - Terraform Data Sources

- ### [10-Terraform-State](10-Terraform-State) - Terraform State

- ### [11-Terraform-Show](11-Terraform-Show) - Terraform Show (need to update)

- ### [12-Terraform-Refresh](12-Terraform-Refresh) - Terraform Refresh Desired and Current state sync

- ### [13-Terraform-State-Commands](13-Terraform-State-Commands) - Inspect, Modify, and Manage the Terraform state

- ### [14-Terraform-Workspaces](14-Terraform-Workspaces) - Manage multiple sets of infrastructure (dev, uat, pre, and prd) with the same Terraform configuration

- ### [15-Terraform-Modules](15-Terraform-Modules) - Reusable terraform codes

- ### [16-Terraform-Import](16-Terraform-Import) - Bring Existing Infrastructure Under IaC

- ### [17-Terraform-Debug](17-Terraform-Debug) - Debugging Terraform

<!--
    - [Simple EC2 Creation](99-Terraform-Example-Codes/01-ec2-creation/)
    - [Simple EC2 Creation Using Data Blocks](99-Terraform-Example-Codes/01.1-ec2-creation-data-blocks/)
    - [S3 Static Website Hosting](99-Terraform-Example-Codes/02-s3-static-website/)
    - [S3 Static Website Hosting multi Env](99-Terraform-Example-Codes/02.1-s3-static-website-env/)

-->
