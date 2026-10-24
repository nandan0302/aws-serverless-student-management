# AWS Serverless Student Management System

A serverless web application built using AWS services to submit student information, store records in a NoSQL database, and retrieve student data through REST APIs.

## Project Overview

This project demonstrates how multiple AWS services can work together to build a serverless application without managing traditional application servers.

The frontend provides a form to enter student details, while the backend processes requests using AWS Lambda and stores or retrieves records from Amazon DynamoDB.

**Project status:** Previously built project. The original AWS infrastructure is currently inactive, and the application has not been retested in a live AWS environment.

## Architecture

The application uses the following AWS services:

- **Amazon S3:** Stores the static frontend files.
- **Amazon CloudFront:** Delivers frontend content globally over HTTPS.
- **Amazon API Gateway:** Provides REST API endpoints for frontend requests.
- **AWS Lambda:** Executes backend logic using Python.
- **Amazon DynamoDB:** Stores and retrieves student records.
- **AWS IAM:** Controls permissions for AWS service access.

### Application Workflow

1. The user opens the frontend application.
2. The user enters a student ID, name, class, and age.
3. The frontend sends a POST request to API Gateway to save the record.
4. The API invokes a Python Lambda function.
5. Lambda writes the student record to DynamoDB.
6. A GET request retrieves student records through API Gateway and Lambda.
7. The frontend displays the retrieved records in a table.

## Features

- Student information submission through a web form.
- Form validation for required fields.
- REST API integration using JavaScript and jQuery.
- Serverless backend processing with AWS Lambda.
- Student record storage using DynamoDB.
- Retrieval and display of student records.
- Loading indicators and success/error messages.
- CloudFront-based frontend delivery over HTTPS.

## Technologies Used

| Technology | Purpose |
|---|---|
| HTML5 | Frontend structure |
| CSS3 | Styling and responsive layout |
| JavaScript | Frontend logic |
| jQuery | AJAX requests and form interactions |
| Python | Lambda backend functions |
| Amazon API Gateway | REST API endpoints |
| AWS Lambda | Serverless compute |
| Amazon DynamoDB | NoSQL database |
| Amazon S3 | Static frontend hosting |
| Amazon CloudFront | Content delivery |
| AWS IAM | Access control |


## Security Considerations

- Use IAM roles to grant Lambda only the permissions it needs.
- Avoid committing AWS access keys, secrets, or real student information.
- Configure API Gateway authorization and appropriate CORS policies before production use.
- Restrict database access to authorized application components.
- Review public access settings for S3 and use CloudFront Origin Access Control where appropriate.

## Challenges and Learnings

During development, I worked on troubleshooting issues involving frontend and backend integration, including:

- Matching JSON attribute names between JavaScript and DynamoDB.
- Configuring API Gateway HTTP methods.
- Handling API responses and displaying records in the frontend.
- Connecting Lambda functions to DynamoDB.
- Understanding how IAM permissions support communication between AWS services.

## Future Improvements

- Correct and validate frontend API configuration.
- Add authentication and authorization.
- Improve error handling and backend input validation.
- Replace full-table scans with more efficient query patterns where appropriate.
- Configure automated testing and deployment.
- Re-deploy the application and validate the complete workflow in AWS.

## Documentation

The `docs/` directory contains the original project report, including the architecture, implementation steps, code examples, and troubleshooting notes.

## Disclaimer

This repository documents a previously built learning project. The original AWS environment is no longer active, so the current deployment status and end-to-end functionality have not been verified.

---

**Project:** AWS Serverless Student Management System  
**Focus:** AWS Serverless Architecture, Cloud Services, and Backend Integration