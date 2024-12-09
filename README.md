# hello-world-with-sam
# AWS SAM Hello World Example

This repository contains a simple serverless application built using the **AWS Serverless Application Model (SAM)** framework. The application deploys an AWS Lambda function that responds with "Hello, World!" when invoked via an API Gateway.

# Demonstration video
https://drive.google.com/file/d/1u_hPyje0b8QoR_KCw1VWgQZNLvqBfB90/view?usp=drivesdk

## **Project Overview**

This project demonstrates the following:
- Setting up a basic serverless application with AWS SAM.
- Creating an API Gateway to trigger the Lambda function.
- Deploying and running the application locally and in AWS.

---

## **Project Architecture**

1. **AWS Lambda Function**: Executes Python code to return a "Hello, World!" response.
2. **Amazon API Gateway**: Routes HTTP requests to the Lambda function.
3. **AWS SAM CLI**: Facilitates building, packaging, and deploying the application.
4. **Amazon S3**: Temporarily stores packaged Lambda function artifacts during deployment.

---

## **Getting Started**

### **Prerequisites**
1. **AWS CLI**: [Install AWS CLI](https://aws.amazon.com/cli/).
2. **AWS SAM CLI**: [Install SAM CLI](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/install-sam-cli.html).
3. **Docker**: [Install Docker](https://www.docker.com/get-started).
4. **Python**: Ensure Python 3.9+ is installed on your system.

---

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
