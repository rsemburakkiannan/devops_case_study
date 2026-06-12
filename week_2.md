# Use Case 1: Production Hotfix Using Git Cherry-Pick

### Scenario

Your team follows this branching strategy:

* `main` → Production
* `release` → Upcoming release
* `develop` → Ongoing development

A critical bug is fixed in `develop` through commit:

```
a1b2c3d
```

However, the next release is still 3 weeks away and the fix must go to production immediately.

### Question

Explain:

1. How you would safely move only this fix to production.
2. Which Git commands you would use.
3. Risks associated with cherry-picking.
4. How you would verify the fix was deployed correctly.
5. How you would avoid duplicate commits in future merges.

### Hands-on Deliverable

Create a Git repository demonstrating:

* Multiple branches
* Bug fix commit
* Cherry-pick workflow
* Documentation of the process

# Use Case 2: Resolving Complex Merge Conflicts

### Scenario

Two developers modify the same deployment script.

Branch A:

```bash
kubectl apply -f deployment.yaml
```

Branch B:

```bash
kubectl apply -f deployment.yaml --record
```

Another section of the script is also modified differently in both branches.

When merging, Git reports conflicts.

### Question

Describe:

1. How Git detects conflicts.
2. How you would identify conflicting sections.
3. How to decide the correct resolution.
4. Commands used during conflict resolution.
5. How to validate the merged code before pushing.

### Hands-on Deliverable

Create:

* Two branches
* Intentional merge conflict
* Conflict resolution
* Pull Request description documenting decisions

# Use Case 3: Automated Log Analysis Script

### Scenario

Operations teams receive application logs every day.

Example:

```text
INFO User login successful
ERROR Database timeout
INFO Health check passed
ERROR Connection refused
ERROR Authentication failed
```

Management wants a daily report.

### Question

Create a Bash script that:

1. Accepts a log file as input.
2. Counts:

   * Total lines
   * INFO entries
   * ERROR entries
3. Displays top 5 most common errors.
4. Generates a summary report.

### Expected Skills

* Variables
* Loops
* grep
* awk
* sort
* uniq
* command-line arguments

### Hands-on Deliverable

Upload to GitHub:

```
log-analyzer.sh
README.md
sample.log
```

# Use Case 4: Linux Health Check Automation

### Scenario

Every morning the support team manually checks:

* CPU utilization
* Memory utilization
* Disk usage
* Running services
* Recent failed logins

Management wants complete automation.

### Question

Write a Bash script that:

1. Collects system health information.
2. Produces output like:

```text
===== SERVER HEALTH =====

CPU Usage: 45%
Memory Usage: 62%
Disk Usage: 70%

Failed Logins:
3

Critical Services:
nginx - Running
docker - Running
```

3. Saves results into a timestamped file.

### Bonus

Generate warnings if:

* CPU > 80%
* Memory > 85%
* Disk > 90%

### Hands-on Deliverable

GitHub repository containing:

```
health-check.sh
README.md
sample-output/
```

# Use Case 5: GitHub-Based Release Automation

### Scenario

Your organization releases software weekly.

Current manual process:

1. Create release tag
2. Generate release notes
3. Archive artifacts
4. Notify team

This process frequently causes mistakes.

### Question

Design a Git + Bash-based release automation process.

Requirements:

* Accept version number as input
* Validate current branch
* Create Git tag
* Generate release notes from commit history
* Package artifacts
* Push tag to remote repository

Example:

```bash
./release.sh v2.1.0
```

### Expected Topics

* Git tags
* Git log
* Bash functions
* Error handling
* Exit codes

### Hands-on Deliverable

GitHub repository:

```
release.sh
README.md
CHANGELOG.md
```

# Expert-Level End-to-End Assignment

### Scenario

You are asked to build a Server Maintenance Toolkit.

### Requirements

Create a GitHub repository containing:

#### Scripts

1. Health Check Script
2. Log Analyzer Script
3. Backup Script
4. Service Monitoring Script

#### Git Requirements

* Feature branches
* Pull Requests
* Merge conflict example
* Tagged release (`v1.0.0`)

#### Documentation

* Architecture diagram
* Usage guide
* Troubleshooting guide

### Evaluation Criteria

* Git workflow maturity
* Bash scripting quality
* Error handling
* Code readability
* Documentation quality
* Automation mindset

This assignment closely mirrors what many organizations expect from DevOps Engineers and SREs during practical assessments.
