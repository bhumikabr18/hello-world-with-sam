# hello-world-with-sam
# AWS SAM Hello World Example

This repository contains a simple serverless application built using the **AWS Serverless Application Model (SAM)** framework. The application deploys an AWS Lambda function that responds with "Hello, World!" when invoked via an API Gateway.

# Demonstration video
https://drive.google.com/file/d/1u_hPyje0b8QoR_KCw1VWgQZNLvqBfB90/view?usp=drivesdk

# Project Overview

This project demonstrates the following:
- Setting up a basic serverless application with AWS SAM.
- Creating an API Gateway to trigger the Lambda function.
- Deploying and running the application locally and in AWS.

---
# Features
* Serverless Architecture: Built using AWS Serverless Application Model (AWS SAM), leveraging cloud-native resources.
* API Integration: Exposes an API Gateway endpoint for triggering a Lambda function.
* Dynamic Response: A simple "Hello World" response generated dynamically via AWS Lambda.
* Efficient Deployment: Fully automated deployment pipeline using AWS SAM CLI and CloudFormation.
* Scalable and Cost-effective: Uses AWS's serverless compute, ensuring scalability without managing infrastructure.

# Technologies Used
* AWS SAM: To define and deploy serverless applications.
* AWS Lambda: For executing the Hello World logic.
* Amazon API Gateway: To expose the Lambda function as an HTTP endpoint.
* AWS CloudFormation: To manage the underlying infrastructure.
* AWS CLI: For managing AWS services and resources.
* Python: The programming language used for the Lambda function.
* Postman: For testing the deployed API endpoints.

# Architecture
1. API Gateway: Serves as the entry point for HTTP requests.
2. AWS Lambda: Processes incoming requests and returns a "Hello World" response.
3. CloudFormation: Provisions and manages the serverless infrastructure as code.

---

# Prerequisites
1. **AWS CLI**: [Install AWS CLI](https://aws.amazon.com/cli/).
2. **AWS SAM CLI**: [Install SAM CLI](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/install-sam-cli.html).
3. **Docker**: [Install Docker](https://www.docker.com/get-started).
4. **Python**: Ensure Python 3.9+ is installed on your system.

---

# How It Works
1. Code Setup: The application code and its resources are defined using an AWS SAM template (template.yml), which specifies the Lambda function, API Gateway, and other resources.

2. Local Build and Testing: The sam build command packages the application locally, while sam local invoke allows testing the Lambda function using sample events.

3. Deployment to AWS: Using the sam deploy --guided command, the application is uploaded to AWS, creating an S3 bucket, deploying a CloudFormation stack, and provisioning the defined resources.

4. API Gateway Integration: API Gateway exposes an HTTP endpoint, forwarding incoming requests to the Lambda function for processing.

5. Lambda Execution: The Lambda function runs Python code to generate a dynamic "Hello World" response upon receiving a request.

6. Response Handling: The response is sent back to the client, accessible via tools like Postman or any HTTP client.

### **Project Structure**
```plaintext
.
├── hello_world/                # Contains the Lambda function code
│   ├── __init__.py
│   ├── app.py                  # Main Python function
│   └── requirements.txt        # Python dependencies
├── events/                     # Sample events for local testing
│   └── event.json
├── tests/                      # Unit tests for Lambda function
│   ├── __init__.py
│   └── test_handler.py
├── template.yaml               # SAM template definition
└── README.md                   # Project documentation
