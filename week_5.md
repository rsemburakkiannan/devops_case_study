# Use Case 1: Application Works Locally but Fails Inside Docker

### Scenario

A Python web application runs successfully on a developer's laptop.

After containerization:

```bash
docker run -p 8080:8080 myapp:latest
```

The container starts successfully, but users cannot access the application.

### Question

Describe how you would investigate:

1. Container status and logs
2. Application binding (`localhost` vs `0.0.0.0`)
3. Port mapping issues
4. Docker networking
5. Missing dependencies
6. Dockerfile configuration mistakes

What Docker commands would you use?

### Hands-on Deliverable

Create:

```text
docker-python-app/
├── app.py
├── requirements.txt
├── Dockerfile
└── README.md
```

Demonstrate:

* Initial failure
* Root cause analysis
* Corrected implementation

Upload to GitHub.

# Use Case 2: Multi-Container Application with Docker Compose

### Scenario

A web application requires:

* Frontend
* Backend API
* MySQL Database

Developers currently start all services manually.

Management wants a single-command deployment.

### Question

Design a Docker Compose solution that:

1. Starts all services together.
2. Establishes inter-container communication.
3. Stores database data persistently.
4. Supports environment-specific configurations.
5. Handles startup dependencies.

Explain:

* Service discovery
* Docker networks
* Volumes
* Environment variables

### Hands-on Deliverable

Repository structure:

```text
docker-compose-app/
├── frontend/
├── backend/
├── db/
├── docker-compose.yml
└── README.md
```

Run:

```bash
docker compose up -d
```

Successfully deploy the entire stack.

# Use Case 3: Persistent Storage and Data Recovery

### Scenario

A MySQL container stores business-critical data.

An engineer accidentally deletes the container:

```bash
docker rm -f mysql-prod
```

After recreation, all data is lost.

### Question

Explain:

1. Why the data was lost.
2. Difference between:

   * Container filesystem
   * Named volumes
   * Bind mounts
3. How Docker volumes work.
4. Backup and recovery strategy.
5. How to migrate data between hosts.

### Hands-on Deliverable

Create:

```text
mysql-persistence/
├── docker-compose.yml
├── backup.sh
├── restore.sh
└── README.md
```

Demonstrate:

* Data persistence
* Backup creation
* Successful restore

# Use Case 4: Container Resource and Performance Troubleshooting

### Scenario

A containerized Java application experiences:

* High CPU usage
* Frequent restarts
* Slow response times

Host server resources appear healthy.

### Question

Describe how you would determine whether the issue is caused by:

* Application memory leaks
* CPU throttling
* Resource limits
* Health check failures
* Container restarts
* Image inefficiencies

What Docker commands and metrics would you inspect?

### Hands-on Deliverable

Deploy a sample application and:

* Configure CPU and memory limits
* Simulate resource exhaustion
* Capture observations
* Document recommendations


# Use Case 5: Secure Container Image Development

### Scenario

A security scan reports:

* Critical vulnerabilities
* Excessive image size
* Containers running as root
* Sensitive credentials embedded in images

### Question

Describe how you would improve:

1. Dockerfile design
2. Base image selection
3. Multi-stage builds
4. Secret management
5. User permissions
6. Image scanning process

What best practices would you implement?

### Hands-on Deliverable

Create:

```text
secure-container/
├── Dockerfile
├── Dockerfile.optimized
├── security-report.md
└── README.md
```

Show:

* Before/after image size
* Security improvements
* Scan results

---

# Use Case 6:

## Scenario

Containerize and deploy a complete microservices application.

### Architecture

```text
Frontend Container
       |
       v
Backend API Container
       |
       v
PostgreSQL Container

Background Worker Container
       |
       v
Redis Container
```

### Requirements

#### Docker

* Custom Dockerfiles
* Multi-stage builds
* Non-root containers
* Health checks

#### Docker Compose

* Custom network
* Named volumes
* Environment variables
* Startup dependencies

#### Persistence

* PostgreSQL volume
* Redis persistence

#### Monitoring

* Container logs
* Health status checks

#### Security

* Least privilege
* Secret handling
* Image scanning

### Deliverables

```text
containerized-platform/
├── frontend/
├── backend/
├── worker/
├── postgres/
├── redis/
├── docker-compose.yml
├── docs/
│   ├── architecture.md
│   ├── troubleshooting.md
│   └── security-review.md
└── README.md
```

### Evaluation Criteria

* Docker architecture understanding
* Dockerfile quality
* Networking knowledge
* Volume management
* Troubleshooting skills
* Security best practices
* Documentation quality
* Production readiness

These scenarios closely reflect real-world challenges faced by DevOps Engineers, Platform Engineers, Cloud Engineers, and SREs working with Docker-based application deployments.
