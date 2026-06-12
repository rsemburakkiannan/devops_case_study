## Use Case 1: Application Reachability Issue

### Scenario

A Java application is running on a Linux server. The application team confirms that the process is running, but users are unable to access the application via `https://app.company.com`.

### Question

You are given SSH access to the server.

Describe, step-by-step, how you would troubleshoot the issue. Your investigation should include:

* Verifying the application process
* Checking listening ports
* Reviewing system and application logs
* Validating DNS resolution
* Testing network connectivity
* Verifying firewall/security restrictions
* Confirming SSL/TLS certificate configuration
* Identifying whether the issue is application, OS, or network related

What Linux and networking commands would you use and why?

## Use Case 2: High CPU and Performance Degradation

### Scenario

A Linux server hosting multiple services is experiencing severe performance degradation.

Symptoms:

* CPU consistently above 95%
* Users report slow response times
* SSH login takes several minutes
* Memory utilization appears normal

### Question

Explain how you would investigate and identify:

* Which process is consuming CPU
* Whether the issue is caused by application code, system services, or network activity
* If excessive DNS lookups are contributing to the problem
* Whether a runaway process or fork bomb exists
* How you would safely remediate the issue without causing downtime

Include Linux commands, logs, and performance metrics you would analyze.

## Use Case 3: SSH Access Suddenly Stops Working

### Scenario

After a routine system update, users can no longer SSH into a production Linux server.

Symptoms:

* Ping works
* Port 22 appears closed from remote systems
* Console access is still available through the cloud provider

### Question

Describe how you would determine whether the issue is caused by:

* SSH service failure
* Firewall configuration
* User account problems
* File permission issues
* SELinux/AppArmor restrictions
* Recent system updates

Explain how you would restore access while maintaining security compliance.

## Use Case 4: Intermittent Application Connectivity Between Servers

### Scenario

A web server communicates with a backend API server over TCP port 8443.

Users report intermittent failures.

Symptoms:

* Requests fail randomly
* Some transactions succeed
* DNS resolution occasionally returns different IP addresses
* Network team reports no outages

### Question

Explain how you would investigate:

* DNS-related issues
* TCP connection establishment problems
* Packet loss or retransmissions
* SSL/TLS handshake failures
* Service availability on the target server
* Load balancer or reverse proxy issues

What Linux networking tools would you use to isolate the root cause?

## Use Case 5: Security Incident Investigation

### Scenario

A Linux server begins generating unusually high outbound network traffic.

Security monitoring reports:

* Connections to unknown external IP addresses
* New user accounts have appeared
* Several services are running that administrators do not recognize

### Question

As the first responder, describe your investigation approach.

Include how you would:

* Identify suspicious users and groups
* Review authentication and SSH logs
* Analyze running processes and services
* Determine persistence mechanisms
* Investigate network connections
* Examine file permission changes
* Collect forensic evidence while minimizing impact

What commands, logs, and Linux artifacts would you review first?

## Use Case 6: Security Incident Investigation

### Scenario

Users complain that a website is slow, but only from certain geographic locations.

The application servers show normal CPU, memory, and disk utilization.

### Question

Design a complete troubleshooting strategy covering:

* DNS resolution path
* TCP three-way handshake
* TLS negotiation
* HTTP request/response flow
* Reverse proxies
* CDN behavior
* Linux server logs
* Network latency analysis

How would you determine whether the bottleneck exists at the client, network, DNS, load balancer, web server, or application layer?

This question tests end-to-end understanding of Linux, TCP/IP, DNS, HTTP/HTTPS, services, logs, and troubleshooting methodology.
