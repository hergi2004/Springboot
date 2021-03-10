# Answer Outline
1. Setup Terraform with Container Resource using HTTPD Image
2. Update Container Resource for Port 80
3. Apply Terrform Script

# Answer File
main.tf
```
# Configure the Docker provider - AKA Plugin
provider "docker" {
  host = "tcp://localhost:2375"
}

# Image Resource from Dockerhub
resource "docker_image" "httpd" {
  name = "httpd:2.4.43"
}

# Container Resource
resource "docker_container" "httpd-server" {
  image = "${docker_image.httpd.name}"
  name  = "httpd-server"
  ports {
    internal = 80
    external = 80
  }
}

```
