# PCI DSS Policy

## 1. Purpose
- Establish security standards and procedures
- Protect Cardholder Data (CHD) in line with PCI DSS
- Guide for IT and Operations

## 2. Scope
- Applies to all systems and users handling CHD
- Includes employees and third parties with access to CHD systems

## 3. Policy Overview
- Compliance with PCI DSS is mandatory
- Failure leads to fines, breaches, reputational damage

## 4. Cardholder Data Handling
- No CHD storage unless legally required
- CHD must be securely deleted quarterly
- SAD (e.g., CVV, PIN) must not be stored post-auth
- PAN must be encrypted and masked unless justified
- PAN must not be copied or moved to unauthorized systems
- CHD transmission must use strong encryption (e.g., TLS 1.2+)
- CHD not to be sent over email, chat, SMS
- Only approved roles may view full PAN

## 5. Access Control
- Access based on least privilege and role
- Access requires management approval
- User and vendor access reviewed every 6 months
- Unique ID required for all users
- Passwords must follow strong security standards
- MFA is mandatory for PCI-impacting systems
- Shared accounts only with justification and controls
- Access revocation on termination
- Session timeouts after inactivity

## 6. Physical Security
- No CHD on physical/removable media
- POS/POI devices inventoried and inspected quarterly
- Visitor access controlled and logged
- All media tracked and assigned ownership

## 7. Logging and Alerting
- Individual CHD access logged
- Logs reviewed daily for critical systems
- Use of synchronized NTP servers
- Logs retained for 1 year, 3 months online
- Critical control failures must trigger alerts and response

## 8. Vulnerability Management
- No direct wireless access to production
- Quarterly internal and external vulnerability scans
- Authenticated internal scans required
- High/critical vulnerabilities must be fixed and rescanned
- Annual penetration tests and segmentation checks
- IDS/IPS must be updated and monitored

## 9. Ongoing DSS Maintenance
### Targeted Risk Assessments
- Define frequency for periodic tasks
- Reviewed annually

### Cryptographic Protocols
- Inventory and monitor all protocols and cipher suites

### Hardware/Software Review
- Evaluate support and compliance status annually

### Scope Confirmation
- Annual or post-change CDE validation

### Incident Management
- Detect unexpected PAN storage and respond accordingly

### Third-Party Reviews
- Annual review of service provider PCI compliance

### Internal Reviews (Service Providers)
- Quarterly checks for adherence to policy and task execution

## 10. Configuration Standards
- Network changes must follow change control
- Firewall rules reviewed semi-annually
- Traffic restricted by rule, zone, and protocol
- NAT, anti-spoofing, and firewall rules enforced
- Mobile devices must have personal firewall enabled

## 11. PCI System Level Settings
- Default accounts and services removed before deployment
- One function per server
- Apply critical patches within 30 days; others within 60 days

## 12. Key Management
- Change/remove default encryption keys at installation
- Rotate keys annually or on personnel change
- Keys stored securely and encrypted
- Use split knowledge and dual control for manual keys
- Inventory and manage all cryptographic material

## 13. Wireless Standards
- Direct wireless access to CHD systems prohibited
- Secure access point settings and firewalls enforced

## 14. Exceptions and Violations
- Exceptions require IT Manager approval
- Violations may result in disciplinary action

## 15. Breach Notification (Appendix B)
- Notify Visa, MasterCard, Discover, AmEx as required
- Incident manager coordinates investigation
- Public notification and remediation steps planned

## 16. Secure Development (Appendix C)
- SDLC must align with OWASP and PCI DSS
- Code reviews and secure coding enforced
- No use of real CHD in test environments
- Scripts in browser must be verified for integrity
- Annual training for developers
- All changes must go through change control with testing
