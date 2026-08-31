# Simple-Queue-Service-Project
Serverless Employee Management System using AWs Lambda, API Gateway, S3, SQS, and DynamoDB.

# Serverless Employee Management System

## Project Overview
A serverless Employee Management System built using AWS services. 
The application allows users to add employees and retrieve employee data through a web interface.

## Architecture
S3 → API Gateway → Lambda → SQS → Lambda → DynamoDB

## AWS Services Used
- Amazon S3
- AWS Lambda
- Amazon API Gateway
- Amazon SQS
- Amazon DynamoDB
- Amazon CloudWatch

## Application Workflow
1. User enters employee details in the web application.
2. S3 hosts the frontend application.
3. API Gateway receives the request.
4. Employee Producer Lambda sends employee data to SQS.
5. SQS triggers the Employee Consumer Lambda.
6. Consumer Lambda stores the employee data in DynamoDB.
7. Get Employees Lambda retrieves employee records from DynamoDB.

## Project Screenshots
Screenshots of the AWS infrastructure and working application are included in this repository.

## Lambda Functions
- employee-producer – Sends employee data to SQS.
- employee-consumer – Reads SQS messages and stores data in DynamoDB.
- get-employees – Retrieves employee records from DynamoDB.

## API Endpoints
- POST /register – Add a new employee.
- GET /employees – Retrieve all employees.

## Deployment Steps
1. Create DynamoDB table.
2. Create SQS queue.
3. Create Lambda functions.
4. Configure SQS trigger.
5. Create API Gateway routes.
6. Configure CORS.
7. Host frontend using Amazon S3.
8. Test the application.

## Key Features
- Serverless architecture
- Asynchronous message processing using SQS
- Employee data storage using DynamoDB
- HTTP API using API Gateway
- Static frontend hosted on S3
