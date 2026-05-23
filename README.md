# Spiceworks IT Help Desk & Incident Lifecycle Lab

## Project Overview
This repository documents the end-to-end design, configuration, and management of an enterprise-grade IT Help Desk infrastructure using the **Spiceworks Cloud Help Desk** platform. The primary objective of this project is to simulate real-world Tier 1 Help Desk operations, demonstrating technical proficiency, logical troubleshooting workflows, multi-tier escalations, and rigorous service documentation standards required for an entry-level help desk role.

By operating simultaneously as the end-user (generating service requests) and the IT support technician (triaging and resolving incidents), this project maps the complete technical and administrative lifecycle of enterprise IT tickets.

---

## Core Technical Competencies
* **Platform Administration:** Provisioned a cloud service desk from scratch, configured user roles, defined operational categories, and mapped simulated departments (HR, Finance, Marketing).
* **Incident Triage & Lifecycle Management:** Enforced structural queue management standards, adjusted Service Level Agreement (SLA) priorities (Low, Medium, High, Urgent), utilized ticket locking/ownership mechanics, and executed proper ticket closure states.
* **Multi-Tier Escalation Workflows:** Simulated operational hand-offs by routing critical database/server-level infrastructure failures from a Tier 1 Support persona to a Tier 2 Systems Administrator account.
* **Technical Documentation & ITSM Compliance:** Authored explicit internal diagnostic notes detailing structural troubleshooting steps (e.g., command-line network utilities, software services diagnostics) while crafting professional, jargon-free resolution notes for end-users.

---

## System Architecture & Environment Configuration
* **Deployment Platform:** Spiceworks Cloud Help Desk
* **Simulated Organizational Directory:**
    * `janesmith@yourcompany.com` (Human Resources)
    * `bjohnson@yourcompany.com` (Finance / CFO)
    * `jdoe@yourcompany.com` (Marketing)
* **Service Catalog Dropdown Categories:** `Hardware`, `Software`, `Network`, `Security / InfoSec`
* **SLA Classification Matrix:** `Low`, `Medium`, `High`, `Urgent`

---

## Documented Case Studies & Incident Lifecycle

### Case Study 1: Identity & Access Management (Low Priority)
* **The Issue:** User `janesmith@yourcompany.com` (HR) reported a system lockout on the corporate payroll portal due to multiple forgotten password attempts.
* **Incident Triage:** Category set to `Software` | Priority set to `Low` | Ticket assigned to Primary Technician.
* **Internal IT Diagnostic Note:**
    > *"Contacted user via phone to verify corporate identity. Located user account in Active Directory; account status flagged as locked out due to invalid logon thresholds. Cleared security lock, initiated a password reset, and checked 'Force password change at next logon' to ensure compliance with identity policies."*
* **Public Resolution & Communication:**
    > *"Hi Jane, your account has been successfully unlocked and your temporary password is set to 'Welcome2026!'. You will be automatically prompted to establish a new secure password immediately upon your next login. Please reach back out if you experience further issues. - IT Support"*
* **Final State:** Ticket status updated from `Open` to `Closed`.

### Case Study 2: Hardware Peripheral Triage & Connectivity (Medium Priority)
* **The Issue:** User `jdoe@yourcompany.com` (Marketing) submitted an incident indicating the main department printer was completely unresponsive and showing as 'Offline' on local systems.
* **Incident Triage:** Category set to `Hardware` | Priority set to `Medium` | Ticket assigned to Primary Technician.
* **Internal IT Diagnostic Note:**
    > *"Initiated a network ping test against the printer's static IP address (192.168.1.55) from the command-line interface—all requests timed out. Verified local client print spooler services on the workstation were running properly. Walked down to the Marketing floor for physical layer inspection. Located the printer and discovered the RJ-45 ethernet cable had been completely unseated from the wall jack during facility cleaning. Securely re-seated the network cable. Re-executed command-line ping tests—successfully returned 0% packet loss. Confirmed end-to-end connectivity."*
* **Public Resolution & Communication:**
    > *"Hi John, the main Marketing printer is now fully operational and back online. A physical network cable was found disconnected from the wall jack and has been securely reconnected. Your queued print jobs should now execute automatically. Let us know if any further issues arise. - IT Support"*
* **Final State:** Ticket status updated from `Open` to `Closed`.

### Case Study 3: Business-Critical Outage & Tier 2 Escalation (High / Urgent Priority)
* **The Issue:** User `bjohnson@yourcompany.com` (Finance / CFO) reported an immediate network timeout error when launching the core enterprise accounting software on the final day of month-end financial closing.
* **Incident Triage:** Category set to `Software` | Priority set to `Urgent` | Ticket assigned to Primary Technician for immediate intake.
* **Internal IT Diagnostic Note (Tier 1 Intake):**
    > *"Verified user's local network and internet connectivity are perfectly stable. Attempted a remote connection directly to the centralized accounting database server from the management console—connection dropped with a socket exception. Inspected server dashboard; identified that the core database service has crashed due to memory exhaustion. Incident requires system-level engineering remediation. Locking ticket and escalating directly to Tier 2 Systems Administration queue."*
* **Escalation Path:** Assignee field modified from Primary Technician to Secondary Technician account (`sysadmin@yourcompany.com`) to simulate multi-tiered escalation.
* **Internal IT Diagnostic Note (Tier 2 Resolution):**
    > *"Ticket received via Tier 1 escalation. Connected to the database host environment via secure terminal. Executed a complete service cycle restart on the accounting engine and flushed localized cache allocations. Monitored resource utilization metrics for 10 minutes—operation stabilized. Confirmed remote client access is fully restored."*
* **Final State:** Ticket status updated to `Closed` via the Tier 2 Admin persona.

### Case Study 4: Security Incident Response & Threat Mitigation (InfoSec Category)
* **The Issue:** User `janesmith@yourcompany.com` forwarded a highly deceptive external email impersonating corporate payroll requesting her to immediately input bank routing details via an embedded link.
* **Incident Triage:** Category updated to `Security / InfoSec` | Priority set to `High` | Ticket assigned to Primary Technician.
* **Internal IT Diagnostic Note:**
    > *"Analyzed email headers and confirmed message originated from a malicious external spoofing domain trying to capture corporate employee credentials. Confirmed with user that no link was clicked and no corporate credentials were leaked. Accessing the central mail administration console immediately: compiled a tenant-wide purge rule using the malicious sender's hash and successfully extracted the message from all internal corporate inboxes to prevent widespread exposure. Initiated an endpoint security compliance malware scan on the reporting user's local workstation as an absolute precaution—scan completed with clean results."*
* **Public Resolution & Communication:**
    > *"Hi Jane, thank you for immediately identifying and safely reporting this malicious message. You handled this perfectly by not interacting with the embedded link. IT has successfully isolated the threat and scrubbed the email completely from all corporate mailboxes. Your machine has been scanned and is fully secure. Excellent vigilance! - IT Security"*
* **Final State:** Ticket status updated from `Open` to `Closed`.

---

## Technical Evidence & Artifacts
*(To display these screenshots on your live profile, place your captured images inside an `images/` directory within this repository and link them below)*

* **Main Operations Queue:**
    ![Help Desk Dashboard Queue](dashboard_queue.png) 
* **ITSM Audit Trail & Timeline:**
    ![Detailed Ticket History](ticket_audit_trail.png)
