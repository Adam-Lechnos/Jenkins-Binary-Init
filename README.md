# Jenkins Binary Init
Dynamically initialize Jenkins pipeline dependent binary files during Jenkins build.

#### Description
Devops pipeline based binaries use devops tested and sanctioned versions of binaries which pipeline function are dependent upon, such as Terraform and Terragrunt. End-users end devops admins are encouraged to leverage this tool to ensure local binaries match the of the versions sanctioned for use in their devops pipeline counterparts. Ensuring consitent versioning between local and pipeline binaries, Terraform state files will remain consistent on the back-end.
 
#### Intended Audience
* Devops

#### Pre-requisites
* Jenkinsfile with scripted pipeline step to create a variable for substituion into the positional parameters as explained under the [Usage](#Usage) section.

#### Usage
Arguments are based on position paramters where the variables contain the desired binary versions assigned to a variable in the Jenkinsfile, or may be specified manually.
* i.e., `binary-init-client ${Terraform Version variable} ${Terragrunt Version version variable}`

##### Options

* First position - Terraform Version
* Second position - Terragrunt Version

##### Examples

  * Use the test branch inside the account_config repo
    * `binary-init-client v1.1.9 v0.36.7`

