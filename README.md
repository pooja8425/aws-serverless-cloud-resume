# AWS Serverless Cloud Resume & Database Pipeline ☁️

**Live Production Link:** [View My Secure Resume Here](https://d2xlaaem5zfncp.cloudfront.net)

## Project Overview
This project goes beyond a standard static website. It is a globally distributed, highly available web portfolio built entirely on AWS serverless infrastructure. It features a live visitor enrollment pipeline that processes web traffic through an API Gateway, triggers backend compute, and securely writes to a NoSQL database.

## Tech Stack & AWS Services Used
* **Frontend Hosting:** Amazon S3 (Simple Storage Service)
* **Content Delivery Network (CDN):** Amazon CloudFront (for global edge-caching and native HTTPS encryption)
* **API Routing:** Amazon API Gateway (HTTP API configured with strict CORS validation)
* **Serverless Compute:** AWS Lambda (Python)
* **Database:** Amazon DynamoDB (NoSQL)

## Cloud Engineering Concepts Demonstrated
1. **$0 Operational Footprint:** Designed a 100% cloud-native architecture that operates entirely within the AWS Free Tier limitations.
2. **Global High Availability:** Decoupled storage boundaries by pointing the CloudFront CDN directly at the S3 web endpoint, ensuring sub-millisecond load times worldwide while hiding the direct S3 bucket URL.
3. **Security & Permissions:** * Implemented explicit **IAM Execution Roles** to grant Lambda least-privilege access to DynamoDB.
    * Successfully engineered and resolved strict **CORS (Cross-Origin Resource Sharing)** policies and `OPTIONS` preflight checks between the CloudFront origin and API Gateway.
    * Automated HTTP to HTTPS redirection at the edge layer.
