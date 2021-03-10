# Student

# 1. Download VS Code

# 2. Installing VS Code Plugins. 
Installing Plugin Terraform Plugin by HashiCorp

The plugin that we are looking for it: 
Plugin ID: mauve.terraform

# 3. Install the Terraform CLI

Manual Installation
3.a You can download the Terraform CLI using: https://www.terraform.io/downloads.html

3.b Run in a Command Line the following:

```
terraform -version
```

Recommendations: Use a Linux Command Emulator such as CMDR if running on windows. 
You can download at: https://cmder.net/

Choco Installation:

3c. Installatin Chococalety
```
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
```

3d. Install Terraform with Choco
```
choco install terraform
```

# 4. terraform init 
When you are are initialling you are pull in third party providers and obtaining the latest updates for the version of terraform that you have installed. 
It is also checking for compliance of main.tf

# 5. Install Docker for Windows
You can download and install here:
https://docs.docker.com/docker-for-windows/install/

# 6. Exposing port 2375 for localhost docker.
6a. Right click on the docker icon in the taskbar. 
6b. Go to Settings
6c. "Expose daemon on tcp://localhost:2375 without TLS"
6d. Apply and Restart

# 7. terraform plan
```
terraform plan
```
* Run through the code and verify issues with formatting. 
* Check that every thing is correctly apply in the specs required by the provider(s).
* Add and Subtracts like Code changes the Infra Structure.
AKA Checks and Balances

# 8. terraform apply
```
terraform apply
```
* Creating the Resource Configured and Planned Out. 
* Request validation prior to commit
* Identifies at the bottom the resources added, changed, or destroyed. 


# 9. Verify
Run the following command to view all docker process:
```
docker ps
```

# 10. Teardown
```
terraform destroy
```
* Require Verfication
* Destroy all resource in the terraform script. 

