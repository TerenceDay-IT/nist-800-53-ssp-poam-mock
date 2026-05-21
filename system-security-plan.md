# System Security Plan (SSP): LogiRoute LLC
**System Tier:** FedRAMP Moderate Baseline  
**Framework:** NIST SP 800-53 Rev. 5  

---

## 1. Access Control (AC) Control Family

### Control: AC-2 - Account Management
* **Control Requirement:** The organization manages information system accounts, including establishing, activating, modifying, reviewing, disabling, and terminating accounts in accordance with organizational policies.
* **System Implementation:** LogiRoute utilizes Microsoft Entra ID for centralized identity management. Account creation and modification require an approved ticket from the HR Management System. Accounts are automatically disabled after 90 days of inactivity.
* **Status:** **Compliant**

### Control: AC-7 - Unsuccessful Logon Attempts
* **Control Requirement:** The information system enforces a limit of consecutive invalid logon attempts by a user during a specified time period.
* **System Implementation:** LogiRoute locks user accounts out for a duration of 30 minutes after five (5) consecutive unsuccessful login attempts within a 15-minute window.
* **Status:** **Compliant**

---

## 2. Audit and Accountability (AU) Control Family

### Control: AU-2 - Event Logging
* **Control Requirement:** The organization identifies the types of events that the information system logs for audit purposes.
* **System Implementation:** LogiRoute configures production application servers and databases to log successful/failed login attempts, privilege escalations, and data modifications. Logs are forwarded in real-time to a centralized SIEM.
* **Status:** **Non-Compliant** (See POA&M ID: POAM-2026-001)
* **Current Gap:** Production Database Subnet B is currently failing to forward transaction logs to the SIEM due to a firewall misconfiguration.
