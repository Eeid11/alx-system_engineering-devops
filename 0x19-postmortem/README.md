# Postmortem Report: Facebook Server Outage

## Issue Summary
**Duration:** The outage occurred from 10:00 AM to 12:30 PM (PST).  
**Impact:** The web application was down, affecting approximately 20% of users.  
**Root Cause:** A misconfigured load balancer caused service disruptions.

## Timeline
- **10:00 AM:** Issue detected through monitoring alerts.
- **10:05 AM:** Began investigation by exploring load balancer logs and backend services.
- **10:15 AM:** Initially assumed backend database issues.
- **10:30 AM:** Investigated incorrect firewall rules (misleading path).
- **11:00 AM:** Escalated to the Infrastructure team.
- **11:30 AM:** Infrastructure team identified the load balancer misconfiguration.
- **12:00 PM:** Corrected load balancer configuration.
- **12:30 PM:** Full service restoration confirmed.

## Root Cause and Resolution
**Root Cause:**  
The misconfiguration of the load balancer caused routing errors, leading to service disruptions for approximately 20% of users. The misconfiguration involved incorrect routing rules that prevented requests from reaching the appropriate backend servers.

**Resolution:**  
The issue was resolved by updating the load balancer settings to correct the routing rules. This involved reviewing the current configuration, identifying the errors, and applying the correct settings to ensure proper routing of traffic.

## Corrective and Preventative Measures
**Improvements:**  
- Enhance monitoring for load balancer health to detect similar issues promptly.
- Implement regular configuration reviews to catch misconfigurations early.
- Establish clearer documentation and procedures for load balancer configurations.

**Tasks:**
- Add more detailed monitoring on load balancer performance and health checks.
- Schedule bi-weekly reviews of load balancer configurations.
- Update internal documentation to include best practices for load balancer setup and maintenance.
- Conduct training sessions for the infrastructure team on load balancer management.

