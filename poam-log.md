# Plan of Action and Milestones (POA&M)

| POA&M ID | Control Affected | Weakness / Deficiency Description | Scheduled Completion | Status | Remediation Plan Action Steps |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **POAM-2026-001** | AU-2 (Event Logging) | Production Database Subnet B transaction logs are not forwarding to centralized SIEM. | July 15, 2026 | **Open** | 1. Review Network Security Group (NSG) rules.<br>2. Update firewall permissions to allow outbound traffic over port 514.<br>3. Verify log ingestion in SIEM dashboard. |
| **POAM-2026-002** | AC-12 (Session Termination) | Remote desktop user sessions fail to terminate automatically after 15 minutes of idle time. | June 30, 2026 | **In Progress** | 1. Deploy updated Group Policy Object (GPO) to enforce idle timeout limits across all corporate workstations. |
