## AWS Three-Tier Architecture Deployment

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
**Screenshot Placeholder**: *![AWS 3-Tier Architecture](https://github.com/user-attachments/assets/d2d2b0d8-c458-4cbf-93c9-01bc18b0defc)
*
## Environment Setup

### Steps:
1. **Account Setup**:
   - Logged into the AWS Management Console and accessed services like EC2, Lambda, API Gateway, and RDS.

     **Screenshot Placeholder**: *![AWS 3- Tier Architecture Account Login](https://github.com/user-attachments/assets/896beb57-c825-4def-8e06-e5fe8931979a)

*

2. **VPC and Subnets**:
   - Created a **Virtual Private Cloud (VPC)** with subnets for public and private resources.
   - Configured **Route Tables**, **Internet Gateway**, and **NAT Gateway** for network connectivity.

 **Screenshot Placeholder**: *![AWS 3-Tier Architecture- VPC](https://github.com/user-attachments/assets/b892de2f-bcad-4a81-99f0-7a848c70df21)
*
 **Screenshot Placeholder**: *![AWS 3-Tier Architecture- Subnets](https://github.com/user-attachments/assets/a34825b4-91a5-43fe-bd71-6938db7a1daa)
*
 **Screenshot Placeholder**: *![AWS 3-Tier Architecture- Route Tables](https://github.com/user-attachments/assets/a48a3f04-98ce-446c-8170-663d3f37ca88)
*
 **Screenshot Placeholder**: *![AWS 3-Tier Architecture-Nat Gateways](https://github.com/user-attachments/assets/c14a86f4-d388-4ef0-b2cf-f43368ecfeb1)
*
3. **Database Setup**:
   - Created an **RDS MySQL** database instance.
   - Configured **security groups** to allow access from the application layer.
      **Screenshot Placeholder**: *![AWS 3-Tier Architectre-Database](https://github.com/user-attachments/assets/9aae4ce6-9638-40ea-a54a-c8ebf191960e)
*

4. **Lambda and API Gateway**:
   - Deployed a **Lambda function** to handle backend logic.
   - Integrated the Lambda function with **API Gateway** to expose RESTful APIs.

      **Screenshot Placeholder**: *![AWS 3-Tier Architecture Backend](https://github.com/user-attachments/assets/9af667c6-cbb9-49cf-a70a-1c956b382009)
*

5. **EC2 Web Application**:
   - Launched an **EC2 instance** with Apache Web Server to host the frontend application.
   - Configured the **Application Load Balancer (ALB)** to distribute traffic across multiple EC2 instances.

---

## Testing and Verification

- **Database Connectivity**: Verified that the Lambda function could connect to the RDS instance.
- **API Gateway**: Tested API endpoints to ensure proper integration with the Lambda function.
- **Web Application**: Confirmed that the EC2-hosted web application could communicate with the backend APIs.

  **Screenshot Placeholder**: *![AWS 3-Tier Architecure-Testing-Verification](https://github.com/user-attachments/assets/65589e68-45e3-4861-8821-b5f7188724b8)

*


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
