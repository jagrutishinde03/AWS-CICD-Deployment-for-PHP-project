# PHP eCommerce Website Deployment with CICD on AWS

This repository contains the code for a PHP-based eCommerce website. The project is configured to be deployed using a CI/CD pipeline on AWS. This detailed description covers the steps to set up and deploy the application, including creating the database, configuring the CICD pipeline, setting up the EC2 instance, and deploying the application with CodeDeploy.

## Table of Contents
1. [Prerequisites](#prerequisites)
2. [Architecture Overview](#architecture-overview)
3. [Setup Instructions](#setup-instructions)
   - [1. RDS Setup](#1-rds-setup)
   - [2. CodeCommit Setup](#2-codecommit-setup)
   - [3. CodeBuild Setup](#3-codebuild-setup)
   - [4. EC2 Setup](#4-ec2-setup)
   - [5. CodeDeploy Setup](#5-codedeploy-setup)
4. [Usage](#usage)
5. [Contributing](#contributing)
6. [License](#license)

## Prerequisites

Before you begin, ensure you have the following prerequisites:

- AWS Account
- MySQL Database Engine
- AWS CodeCommit
- AWS CodeBuild
- EC2 Instance
- AWS CodeDeploy
- PHP, Apache, Git installed on EC2 Instance

## Architecture Overview

The deployment architecture includes:

- **Amazon RDS**: MySQL Database Engine
- **AWS CodeCommit**: Version control for source code
- **AWS CodeBuild**: Build automation
- **EC2 Instance**: Hosting PHP application
- **AWS CodeDeploy**: Automated deployment to EC2
[!image](https://github.com/jagrutishinde03/AWS-CICD-Deployment-for-PHP-project/blob/main/Project%20Architecture.png)
## Setup Instructions

### 1. RDS Setup

- Create an RDS instance with the following options:
  - Engine options: MySQL
  - Templates: Free Tier
  - Database name: ecommerce
  - Public access: Yes

**COPY RDS ENDPOINT URL**

### 2. CodeCommit Setup

- Create a repository on AWS CodeCommit.
- Clone the repository to your local machine.

### 3. CodeBuild Setup

- Create a build project on AWS CodeBuild.
- Configure the build project to use the repository on AWS CodeCommit.
- Artifacts should be stored in an S3 bucket.

### 4. EC2 Setup

- Launch an EC2 instance with Ubuntu OS.
- Install PHP, Apache, MySQL, Git.
- Set up environment variables in `admin/inc/config.php`.

### 5. CodeDeploy Setup

- Create an application and deployment group on AWS CodeDeploy.
- Configure deployment to use the S3 bucket as the source.

## Usage

After completing the setup, access the eCommerce website using the public IP address of the EC2 instance.

## Contributing

Contributions are welcome! Please fork the repository and create a pull request with your changes.

## License

This project is licensed under the MIT License. See the LICENSE file for details.

**Author**: Jagruti Shinde

**Email**: jagruti03shinde@gmail.com
