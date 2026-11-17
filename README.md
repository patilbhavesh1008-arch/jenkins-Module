# DevOps CI/CD Pipeline Project

## Project Overview
An automated CI/CD pipeline using Jenkins, Docker,
Docker Hub, GitHub Webhooks and AWS EC2.

## Technologies Used
- AWS EC2
- Jenkins
- Docker
- Docker Hub
- Git & GitHub
- GitHub Webhooks
- Linux
- Nginx

## Project Architecture

Developer
   |
   v
GitHub Repository
   |
   v
GitHub Webhook
   |
   v
Jenkins Pipeline
   |
   v
Docker Image Build
   |
   v
Docker Hub
   |
   v
AWS EC2 Deployment
   |
   v
Live Web Application

## Pipeline Stages
1. Git Checkout
2. Build
3. Test
4. Docker Build
5. Docker Hub Push
6. Deploy

## Deployment

The application is deployed on AWS EC2
using Docker and Nginx.

## Live Application

http://3.108.221.149:8081

## GitHub Repository

https://github.com/patilbhavesh1008-arch/jenkins-Module

## Author
Bhavesh Patil
