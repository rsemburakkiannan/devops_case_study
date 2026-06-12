# Use Case 1: Application Unreachable After Deployment

### Scenario

A web application has been deployed on an EC2 instance inside a VPC.

Users report that the application is inaccessible from the internet.

Environment:

* EC2 instance is running
* Application service is running on port 8080
* Public IP assigned
* Route Table contains Internet Gateway route

### Question

Describe how you would troubleshoot the issue.

Your investigation should include:

* Security Groups
* Network ACLs
* Route Tables
* Internet Gateway
* EC2 OS firewall
* Application listening ports
* DNS configuration

How would you identify whether the issue is:

* Application
* EC2
* VPC networking
* Security configuration

### Hands-on Deliverable

Deploy a sample application on EC2 and document:

* Architecture diagram
* Security Group configuration
* Troubleshooting steps
* Validation evidence

# Use Case 2: Secure File Processing Using S3, Lambda, and SNS

### Scenario

A business uploads CSV files into an S3 bucket.

Requirements:

1. Automatically detect new uploads.
2. Validate file format.
3. Send notification if validation fails.
4. Store processing logs.
5. Alert operations team.

### Question

Design an AWS solution using:

* S3
* Lambda
* SNS
* CloudWatch

Explain:

* Event flow
* Security controls
* IAM permissions
* Error handling
* Monitoring strategy

### Hands-on Deliverable

Implement:

```text
User Upload
      ↓
S3
      ↓
Lambda
      ↓
SNS Notification
```

Provide:

* Source code
* IAM policies
* Architecture diagram
* Deployment instructions

# Use Case 3: EKS Application Failure Investigation

### Scenario

An application running in Amazon EKS becomes unavailable.

Symptoms:

* Pods repeatedly restart
* Service endpoint inaccessible
* CloudWatch reports increased errors

### Question

Explain how you would investigate:

1. Pod status
2. Deployment configuration
3. Service configuration
4. Ingress configuration
5. Container logs
6. Node health
7. IAM permissions
8. Network policies

What AWS and Kubernetes commands would you use?

### Hands-on Deliverable

Deploy a sample application on EKS and intentionally introduce:

* Misconfigured service
* Resource limits issue
* Failing container

Document root cause analysis and resolution.

# Use Case 4: Decoupling Microservices Using SQS

### Scenario

An e-commerce platform experiences failures because the Order Service directly calls the Inventory Service.

When Inventory becomes slow:

* Orders fail
* User experience degrades

Management wants a more resilient architecture.

### Question

Design a solution using:

* SQS
* Lambda or ECS
* CloudWatch

Explain:

* Message flow
* Retry strategy
* Dead Letter Queue (DLQ)
* Failure recovery
* Monitoring

How would you guarantee message processing reliability?

### Hands-on Deliverable

Build:

```text
Order Service
      ↓
SQS
      ↓
Worker Service
      ↓
Inventory Update
```

Demonstrate:

* Successful processing
* Failure handling
* DLQ processing

# Use Case 5: AWS Cost and Performance Optimization

### Scenario

A development environment has become expensive.

Resources include:

* EC2
* RDS
* ECS
* EKS
* S3

Monthly costs have increased by 40%.

### Question

Describe how you would identify optimization opportunities.

Include:

### EC2

* Rightsizing
* Auto Scaling
* Reserved Instances
* Spot Instances

### S3

* Lifecycle policies
* Storage classes

### RDS

* Instance sizing
* Backup optimization

### ECS/EKS

* Resource requests and limits
* Node utilization

### CloudWatch

* Metrics to review

### Hands-on Deliverable

Prepare a cost optimization report showing:

* Current architecture
* Cost drivers
* Recommended changes
* Estimated savings

# # Use Case 6

## Scenario

Design and deploy a highly available cloud-native application.

### Requirements

#### Infrastructure

* VPC
* Public and Private Subnets
* Security Groups
* IAM Roles

#### Compute

Choose either:

* ECS Fargate
* EKS

#### Database

* RDS MySQL/PostgreSQL

#### Storage

* S3

#### Event Processing

* SQS
* SNS

#### Monitoring

* CloudWatch Dashboard
* CloudWatch Alarms

#### Security

* Least-privilege IAM
* Encryption at rest
* Encryption in transit

### Example Architecture

```text
Internet
    ↓
Load Balancer
    ↓
ECS/EKS
    ↓
RDS

Application
    ↓
SQS
    ↓
Worker

Application
    ↓
S3
    ↓
Lambda
    ↓
SNS
```

### Deliverables

* GitHub repository
* Infrastructure as Code (CloudFormation/Terraform preferred)
* Deployment guide
* Architecture diagram
* Monitoring dashboard screenshots
* Cost estimation
* Security review

### Evaluation Criteria

* AWS fundamentals knowledge
* Networking understanding (VPC, SG, routing)
* IAM and security best practices
* Troubleshooting methodology
* Container platform knowledge (EKS/ECS)
* Event-driven architecture design
* Operational excellence and monitoring

These scenarios closely mirror the kinds of AWS challenges faced by Cloud Engineers, DevOps Engineers, Platform Engineers, and SREs in enterprise environments.
