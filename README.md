# Static Website CI/CD Pipeline on AWS

## Project Overview

This project demonstrates a complete CI/CD (Continuous Integration and Continuous Deployment) pipeline for a static website using AWS services. Whenever code is pushed to GitHub, AWS CodePipeline automatically deploys the latest version of the website to Amazon S3.

## Architecture

GitHub Repository → AWS CodeConnections → AWS CodePipeline → Amazon S3 Static Website Hosting

## Services Used

* GitHub
* AWS CodeConnections
* AWS CodePipeline
* Amazon S3
* IAM
* CloudWatch Logs

## Project Workflow

1. Developer updates website code locally.
2. Changes are pushed to GitHub.
3. AWS CodeConnections detects the repository update.
4. CodePipeline automatically starts.
5. Build stage validates the files.
6. Deploy stage uploads files to the S3 bucket.
7. Website is updated automatically.

## Repository Structure

```text
static-site-cicd/
│
├── index.html
└── README.md
```

## Prerequisites

* AWS Account
* GitHub Account
* S3 Bucket
* AWS CodePipeline
* AWS CodeConnections

## Deployment Steps

### 1. Create Static Website

Create an `index.html` file:

```html
<h1>Welcome to My Static Website</h1>
```

### 2. Push Code to GitHub

```bash
git init
git add .
git commit -m "Initial commit"
git push origin main
```

### 3. Create S3 Bucket

* Create an S3 bucket.
* Enable Static Website Hosting.
* Set index document as `index.html`.
* Configure bucket policy for public access.

### 4. Create CodePipeline

* Source Provider: GitHub
* Repository: static-site-cicd
* Branch: main
* Deploy Provider: Amazon S3

### 5. Test Pipeline

Update the website:

```bash
git add .
git commit -m "Website update"
git push origin main
```

The pipeline automatically deploys the updated files to Amazon S3.

## Skills Demonstrated

* CI/CD Pipeline Implementation
* Git & GitHub Integration
* AWS CodePipeline
* AWS CodeConnections
* Amazon S3 Static Website Hosting
* IAM Permission Management
* CloudWatch Logging

## Outcome

Successfully automated static website deployment using AWS CI/CD services, eliminating manual uploads and ensuring faster and more reliable releases.

## Author

Mahammad Shahinoor
