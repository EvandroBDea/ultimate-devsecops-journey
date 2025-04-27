📁 Lab 4 – Provisioning with Terraform + Docker (NGINX)

Goal: Provision an NGINX container using Terraform.

main.tf structure:

-------------------------------------------------------------------
terraform {
  required_providers {
    docker = {
      source  = "kreuzwerker/docker"
      version = "~> 3.0.1"
    }
  }
}

provider "docker" {}

resource "docker_image" "nginx" {
  name         = "nginx"
  keep_locally = false
}

resource "docker_container" "nginx" {
  image = docker_image.nginx.image_id
  name  = "tutorial"

  ports {
    internal = 80
    external = 8000
  }
}

-------------------------------------------------------------------

Result: NGINX container available locally at http://localhost:8000

