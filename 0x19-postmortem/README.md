Postmortem Report: Facebook Server Outage
Issue Summary
Duration: The outage occurred from 10:00 AM to 12:30 PM (PST).
Impact: The web application was down, affecting approximately 20% of users.
Root Cause: A misconfigured load balancer caused service disruptions.
Timeline
Issue Detection:
Detected at 10:00 AM through monitoring alerts.
Investigation Actions:
Explored load balancer logs and backend services.
Assumed backend database issues initially.
Investigated incorrect firewall rules (misleading path).
Escalation:
Escalated to the Infrastructure team.
Resolution:
Corrected load balancer configuration.
Root Cause and Resolution
Root Cause:
The load balancer misconfiguration led to routing errors.
Resolution:
Updated load balancer settings.
Corrective and Preventative Measures
Improved monitoring for load balancer health.
Scheduled regular configuration reviews.
