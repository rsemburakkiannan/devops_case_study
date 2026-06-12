# Use Case 1: Infrastructure Drift and Terraform State Management

### Scenario

Your team provisions AWS infrastructure using Terraform:

* VPC
* EC2
* Security Groups
* RDS

An engineer manually modifies a Security Group rule from the AWS Console.

A week later, Terraform deployments begin behaving unexpectedly.

### Question

Explain:

1. What infrastructure drift is.
2. How Terraform detects drift.
3. How you would investigate the issue.
4. Risks of manual changes.
5. How to safely reconcile Terraform state with AWS.

What Terraform commands would you use?

### Hands-on Deliverable

Create Terraform code that provisions:

* VPC
* EC2 Instance
* Security Group

Then:

* Make a manual AWS change
* Detect drift
* Correct the drift
* Document the process

# Use Case 2: Kubernetes Application Not Accessible

### Scenario

A containerized application is successfully deployed to Kubernetes.

```bash
kubectl get pods
```

shows:

```text
Running
```

However, users cannot access the application.

### Question

Describe how you would investigate:

1. Pod status
2. Deployment configuration
3. Service configuration
4. Port mappings
5. Endpoint availability
6. DNS resolution
7. Ingress configuration

How would you determine whether the issue exists in:

* Pod
* Deployment
* Service
* Network
* Application

### Hands-on Deliverable

Deploy:

```text
Nginx Container
      ↓
Deployment
      ↓
Service
```

Intentionally misconfigure one component and document:

* Symptoms
* Investigation
* Resolution

# Use Case 3: Pod CrashLoopBackOff Investigation

### Scenario

A newly deployed application enters:

```text
CrashLoopBackOff
```

State.

Business impact:

* Application unavailable
* Deployment blocked

### Question

Explain how you would investigate:

1. Container logs
2. Events
3. Resource limits
4. Image configuration
5. Startup commands
6. Environment variables
7. Secrets and ConfigMaps

What Kubernetes commands would you use?

### Hands-on Deliverable

Deploy a sample application and intentionally cause:

* Missing environment variable
* Incorrect image tag
* Startup failure

Document root cause and remediation.

# Use Case 4: Automated Infrastructure and Application Deployment

### Scenario

Management wants a fully automated deployment process:

Requirements:

1. Create AWS infrastructure.
2. Deploy Kubernetes cluster.
3. Deploy application.
4. Expose application externally.

### Question

Design a Terraform-based solution that provisions:

* VPC
* EKS Cluster
* Node Group
* Security Groups

Then deploy:

* Application Deployment
* Service
* Ingress

Explain:

* Terraform modules
* State management
* Dependency handling
* Kubernetes deployment strategy

### Hands-on Deliverable

Create repository:

```text
terraform-k8s-deployment/
├── terraform/
├── kubernetes/
├── docs/
└── README.md
```

Deploy a working application end-to-end.

# Use Case 5: Scaling and High Availability

### Scenario

A customer-facing application experiences traffic spikes.

Current deployment:

```text
1 Pod
1 EC2 Worker Node
```

Users report:

* Slow responses
* Timeouts

### Question

Describe how you would improve:

### Kubernetes

* Replica scaling
* Horizontal Pod Autoscaler
* Resource requests and limits

### AWS

* Node Group scaling
* Load balancing

### Terraform

* Infrastructure scaling automation

How would you ensure high availability during node or pod failures?

### Hands-on Deliverable

Implement:

* Multiple replicas
* Load-balanced service
* Auto Scaling configuration

Demonstrate failover and recovery.

# Use Case 6:

## Scenario

Build a cloud-native platform using Terraform and Kubernetes.

### Infrastructure (Terraform)

Provision:

* VPC
* Public/Private Subnets
* Internet Gateway
* NAT Gateway
* Security Groups
* EKS Cluster
* Managed Node Group

### Kubernetes

Deploy:

* Frontend Application
* Backend API
* PostgreSQL Database

### Kubernetes Resources

* Namespace
* Deployment
* Service
* ConfigMap
* Secret
* Ingress

### Operations

Implement:

* Rolling Updates
* Health Checks
* Resource Limits
* Autoscaling

### Architecture

```text
Internet
    ↓
ALB / Ingress
    ↓
Frontend Pods
    ↓
Backend Pods
    ↓
Database
```

### Deliverables

```text
cloud-native-platform/
├── terraform/
│   ├── vpc.tf
│   ├── eks.tf
│   ├── variables.tf
│   └── outputs.tf
├── kubernetes/
│   ├── namespace.yaml
│   ├── deployment.yaml
│   ├── service.yaml
│   ├── ingress.yaml
│   ├── configmap.yaml
│   └── secret.yaml
├── docs/
│   ├── architecture.md
│   ├── deployment.md
│   ├── troubleshooting.md
│   └── scaling.md
└── README.md
```

### Evaluation Criteria

* Terraform fundamentals
* Infrastructure as Code practices
* Kubernetes architecture knowledge
* Troubleshooting methodology
* AWS integration knowledge
* Scalability design
* High availability concepts
* Documentation quality

These scenarios closely mirror real-world responsibilities of DevOps Engineers, Cloud Engineers, Platform Engineers, and SREs working with AWS, Terraform, and Kubernetes.
