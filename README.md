
---

AWS Three-Tier Architecture Deployment

## Overview
This project involves the deployment of a **three-tier architecture** on **Amazon Web Services (AWS)**. The architecture consists of a **presentation layer**, **application layer**, and **data layer**, implemented using various AWS services such as **EC2**, **RDS**, **Lambda**, **API Gateway**, and **CloudWatch**. The project was completed as part of an assignment for the **Cloud Security and Management** course at the **University of Petroleum and Energy Studies (UPES)**.

---

## Architecture Design

### Components:
1. **Presentation Layer**:
   - **EC2 Instances**: Hosting a web application using Apache Web Server.
   - **Application Load Balancer (ALB)**: Distributes traffic across multiple EC2 instances.

2. **Application Layer**:
   - **AWS Lambda**: Handles backend logic and processing.
   - **API Gateway**: Integrates with Lambda functions to expose APIs.

3. **Data Layer**:
   - **Amazon RDS (MySQL)**: Stores application data.
   - **RDS Proxy**: Manages database connections for scalability and security.

4. **Monitoring**:
   - **AWS CloudWatch**: Monitors the performance and health of the application.

---

## Environment Setup

### Steps:
1. **Account Setup**:
   - Logged into the AWS Management Console and accessed services like EC2, Lambda, API Gateway, and RDS.

2. **VPC and Subnets**:
   - Created a **Virtual Private Cloud (VPC)** with subnets for public and private resources.
   - Configured **Route Tables**, **Internet Gateway**, and **NAT Gateway** for network connectivity.

3. **Database Setup**:
   - Created an **RDS MySQL** database instance.
   - Configured **security groups** to allow access from the application layer.

4. **Lambda and API Gateway**:
   - Deployed a **Lambda function** to handle backend logic.
   - Integrated the Lambda function with **API Gateway** to expose RESTful APIs.

5. **EC2 Web Application**:
   - Launched an **EC2 instance** with Apache Web Server to host the frontend application.
   - Configured the **Application Load Balancer (ALB)** to distribute traffic across multiple EC2 instances.

---

## Testing and Verification

- **Database Connectivity**: Verified that the Lambda function could connect to the RDS instance.
- **API Gateway**: Tested API endpoints to ensure proper integration with the Lambda function.
- **Web Application**: Confirmed that the EC2-hosted web application could communicate with the backend APIs.

---

## Challenges and Solutions

1. **Database Connectivity Issues**:
   - **Challenge**: The Lambda function could not connect to the RDS instance due to incorrect security group rules.
   - **Solution**: Updated the security group to allow inbound connections from the Lambda VPC endpoint.

2. **API Gateway CORS Errors**:
   - **Challenge**: Encountered CORS issues when making requests from the EC2 web application.
   - **Solution**: Enabled CORS in the API Gateway settings.

---

## Areas for Improvement

1. **Scalability**:
   - Use **Elastic Load Balancer (ELB)** to handle increased traffic and improve fault tolerance.

2. **Security**:
   - Implement **encryption for data at rest** in the RDS instance.
   - Use **AWS Secrets Manager** to securely store and manage database credentials.

---

## Conclusion

The three-tier architecture was successfully deployed on AWS, meeting all functional requirements of the assignment. The project demonstrates a secure and scalable application design using AWS services, with proper separation of concerns across the presentation, application, and data layers.


---

This README file provides a concise summary of the project. 😊
