# Secure Software Development Lifecycle (SDLC) Procedure

## 1. Purpose

The purpose of this procedure is to ensure that all applications developed, acquired, or maintained by the organization follow secure practices throughout the entire software development lifecycle. This supports the prevention, detection, and remediation of security weaknesses before deployment and during ongoing maintenance.

## 2. Scope

This procedure applies to:

- All internally developed applications  
- All updates, enhancements, and patches  
- All third-party or open-source components used in applications  
- All environments (development, testing, staging, production)  

It covers planning, design, development, testing, deployment, and ongoing operations.

---

## 3. Roles and Responsibilities

### Developers
- Follow secure coding standards  
- Conduct peer reviews and remediate vulnerabilities  
- Use approved libraries and frameworks  

### Security / AppSec Team
- Provide security requirements and coding guidance  
- Conduct threat modeling and review architecture  
- Perform security testing (SAST, DAST, SCA)  

### QA / Testing Team
- Validate that security requirements are met  
- Test for common vulnerabilities (OWASP Top 10)  

### Project Managers / Product Owners
- Ensure secure SDLC tasks are included in project plans  
- Track remediation and approve releases  

---

## 4. Secure SDLC Stages

### **4.1 Planning and Requirements**
During initial planning:

- Identify data classification and regulatory requirements (HIPAA, PCI, etc.)  
- Identify potential security risks  
- Define security requirements for access control, encryption, and logging  
- Document functional and non-functional security needs  

### **4.2 Design**
Architecture must:

- Follow secure design patterns  
- Implement least privilege and zero-trust principles  
- Include threat modeling for high-impact applications  
- Document trust boundaries and data flows  

**AppSec reviews the design** for missing controls or risks.

### **4.3 Development**
Developers must:

- Follow secure coding standards (OWASP, SEI CERT)  
- Avoid deprecated or insecure functions  
- Store secrets using approved secret management tools  
- Validate all inputs and sanitize outputs  
- Use approved cryptographic libraries  

**Peer code reviews** are mandatory.

### **4.4 Security Testing**
Before deployment:

- **Static Application Security Testing (SAST)** must be performed  
- **Dynamic Application Security Testing (DAST)** must be performed for web apps  
- **Software Composition Analysis (SCA)** must check for vulnerable dependencies  
- **Manual security tests** must validate critical controls  
- High and critical vulnerabilities must be remediated prior to release  

### **4.5 Deployment**
To promote code to production:

- All required security testing must be completed  
- Risk ratings must be documented  
- Required approvals must be obtained  
- Deployment must follow change management policies  

Security reviews must be included in change tickets for high-risk releases.

### **4.6 Maintenance and Monitoring**
After deployment:

- Logs must be centralized and monitored  
- Vulnerabilities must be tracked and patched  
- Secrets and credentials must be rotated regularly  
- AppSec must re-review the application after major changes  
- New risks must be added to the application’s risk register  

---

## 5. Vulnerability Remediation SLAs

| Severity | SLA (Time to Remediate) |
|----------|---------------------------|
| Critical | 15 days |
| High     | 30 days |
| Medium   | 90 days |
| Low      | As-needed |

All exceptions must be documented and approved by Security.

---

## 6. Third-Party and Open-Source Components

- All external libraries must be vetted for vulnerabilities  
- SCA scans must be performed on every release  
- Deprecated or unsupported components must be replaced  

---

## 7. Documentation Requirements

The following must be documented:

- Design diagrams and data flows  
- Threat models  
- Testing results (SAST, DAST, SCA)  
- Vulnerability tickets and remediation status  
- Change management approvals  

---

## 8. Review Cycle

This procedure must be reviewed annually or whenever significant changes occur in technology, development processes, or security requirements.

---

# Document Owner
Information Security – Governance, Risk, and Compliance
