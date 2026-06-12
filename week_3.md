# Use Case 1: Broken CI/CD Build After Dependency Upgrade

### Scenario

A Java application built with Maven has been building successfully for months. After a dependency update, the CI pipeline starts failing.

Error:

```text
Failed to execute goal
Could not resolve dependencies
Artifact not found
```

Developers claim the application builds successfully on their laptops.

### Question

Describe how you would investigate:

1. Whether the issue is related to Maven repositories.
2. Dependency version conflicts.
3. Local cache vs CI environment differences.
4. Network/proxy configuration issues.
5. Repository authentication problems.

Explain the Maven commands and files you would inspect.

### Hands-on Deliverable

Create a Maven project and:

* Introduce a dependency issue intentionally.
* Demonstrate troubleshooting steps.
* Document root cause and resolution.
* Push code and documentation to GitHub.

# Use Case 2: Automated Build Validation Using Python

### Scenario

A DevOps team manages 50+ applications built using Maven, Gradle, and npm.

Management wants a Python script that:

* Scans repositories.
* Detects build tool type.
* Executes build commands.
* Collects build results.
* Generates a consolidated report.

### Question

Design a Python automation solution.

Requirements:

* Detect:

  * `pom.xml`
  * `build.gradle`
  * `package.json`
* Run appropriate build command.
* Capture logs.
* Handle failures gracefully.
* Produce a summary report.

### Hands-on Deliverable

Create:

```text
build-validator/
├── validate_builds.py
├── sample-maven-app/
├── sample-gradle-app/
├── sample-node-app/
└── report.csv
```

Upload to GitHub.

# Use Case 3: npm Build Failure in Production Pipeline

### Scenario

A React application suddenly fails in CI.

Error:

```text
npm ERR! dependency tree conflict
```

Developers can run the application locally without issues.

### Question

Explain how you would investigate:

1. package.json
2. package-lock.json
3. Peer dependency conflicts
4. npm version differences
5. Node.js version mismatches
6. CI environment discrepancies

What commands would you run?

### Hands-on Deliverable

Create a sample npm application with:

* Intentional dependency conflict.
* Root cause analysis.
* Resolution steps.

Document everything in GitHub.

# Use Case 4: Large-Scale Dependency Audit

### Scenario

A security team identifies a critical vulnerability in a widely used library.

You must quickly determine:

* Which applications use the library.
* Affected versions.
* Upgrade recommendations.

Applications are built using:

* Maven
* Gradle
* npm

### Question

Design a Python solution that:

1. Scans repositories.
2. Extracts dependencies.
3. Detects vulnerable versions.
4. Produces a compliance report.

How would you make the solution scalable for hundreds of repositories?

### Hands-on Deliverable

Develop:

```text
dependency-audit/
├── dependency_scanner.py
├── vulnerability_rules.json
├── reports/
└── README.md
```

Upload to GitHub.

# Use Case 5: Build Performance Optimization

### Scenario

A Maven project build time has increased from:

```text
8 minutes → 35 minutes
```

No significant code changes have occurred.

### Question

Describe how you would determine whether the slowdown is caused by:

* Dependency downloads
* Plugin execution
* Test execution
* Code generation
* Repository latency
* Infrastructure issues

What tools and commands would you use?

How would you optimize build performance?

### Hands-on Deliverable

Create:

* Maven project
* Performance baseline report
* Optimization recommendations
* Before/after metrics

Upload findings to GitHub.

# Use Case 6: 

## Scenario

You are responsible for maintaining a platform hosting:

* Java (Maven)
* Java (Gradle)
* Node.js (npm)

applications.

Management wants a unified automation framework.

### Requirements

Create a Python-based Build Management Tool that:

#### Features

1. Detects application type.
2. Installs dependencies.
3. Executes build.
4. Runs tests.
5. Captures build duration.
6. Generates HTML/CSV report.
7. Identifies build failures.
8. Archives logs.

#### Supported Build Tools

* Maven
* Gradle
* npm

#### Example Usage

```bash
python build_manager.py --repo ./sample-app
```

### GitHub Deliverables

```text
build-manager/
├── build_manager.py
├── modules/
│   ├── maven.py
│   ├── gradle.py
│   └── npm.py
├── reports/
├── logs/
├── README.md
└── sample-apps/
```

### Evaluation Criteria

* Python coding quality
* Error handling
* Dependency management knowledge
* Build troubleshooting methodology
* Reporting and automation design
* GitHub project structure
* Documentation quality

These scenarios closely reflect real-world DevOps, Platform Engineering, and CI/CD engineering challenges rather than simple theoretical questions.
