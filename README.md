# aws_autodeploy
Uses Ansible and Docker DevOps tools to autodeploy a java jar file to AWS from scratch in an infrastructure-as-code approach

Tools used include: Ansible playbook, Cloudformation Templates and Dockerfile

The base YML file for the project is entrypoint.yml
Entrypoint.yml has 3 tasks

Task 1 creates the AWS Elastic Container Service stack for hosting the docker image, consisting of the ECR, ECS instances, Cluster etc, and the NGINX proxy server

Task 2 builds and tags the docker image and pushes the image to the repo

Task 3 creates the ECS task definitions and service

Pre-requisites:

My development environment looked like this:
Ubuntu linux 16 (installed packages include: python3, boto, boto3, ansible, docker, awscli)

