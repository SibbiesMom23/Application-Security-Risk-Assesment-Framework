# Sample Web Application Risk Assessment

## 1. Application Overview

- Application Name: Patient Portal Web Application
- Owner / Business Unit: Clinical Services
- Technical Owner: Web Applications Team
- Environment: Production
- Hosting Model: Cloud-hosted (IaaS)
- Criticality: High

The Patient Portal Web Application allows patients to view lab results, schedule appointments, send secure messages, and update demographic information.

## 2. Data Classification

- Data types processed:
  - Protected Health Information (PHI)
  - Personally Identifiable Information (PII)
  - Internal configuration and logging data

- Highest data classification level: PHI  
- Regulatory impact:
  - HIPAA
  - State-level privacy requirements

## 3. Architecture Summary

- Components:
  - Internet-facing web front end
  - Application layer with business logic
  - Backend database storing PHI and PII
  - API calls to internal scheduling and EMR systems

- Network exposure:
  - Internet-facing through HTTPS
  - Web application firewall in place

- Authentication/authorization:
  - Username/password with MFA
  - Role-based access control for patient vs. staff functions

## 4. Threats and Vulnerabilities

### Identified Threats

- Unauthorized access to PHI
- Credential stuffing and account takeover
- Injection attacks (SQL injection, command injection)
- Cross-site scripting (XSS)
- Misconfiguration in cloud-hosted infrastructure
- Weak or missing logging and alerting

### Known or Suspected Vulnerabilities

- Some legacy pages not using centralized input validation
- Inconsistent security headers on certain responses
- Limited alerting on administrative actions
- MFA not enforced on all user groups

### Recent Testing Results

- Vulnerability scan:
  - Several low findings, two medium findings related to missing security headers

- Penetration test:
  - Reflected XSS demonstrated on a legacy search page
  - Weak session timeout configuration identified

## 5. Security Controls

### Access Control

- SSO: Not implemented; local accounts only
- MFA: Required for staff, optional for patients
- RBAC: Implemented for staff roles

### Data Protection

- Encryption in transit:
  - TLS 1.2 and 1.3 enabled
  - Older protocols disabled

- Encryption at rest:
  - Database encryption enabled
  - Encrypted cloud volumes

- Key management:
  - Managed by cloud provider KMS

### Logging and Monitoring

- Centralized application logging
- Limited alerting rules
- No dedicated login anomaly dashboard

### Hardening and Configuration

- Standard server baselines applied
- Patching:
  - OS patched monthly
  - App dependencies patched quarterly

## 6. Risk Scoring

1–5 scale for both likelihood and impact.

### Risk 1: Reflected XSS on Legacy Search Page
- Likelihood: 3
- Impact: 4
- Risk Score: 12
- Rating: Medium–High

### Risk 2: MFA Optional for Patients
- Likelihood: 4
- Impact: 4
- Risk Score: 16
- Rating: High

## 7. Findings and Recommendations

### Finding 1: Reflected XSS on Legacy Search Page
- Description:
  - User input is not properly validated/encoded.
- Root cause:
  - Legacy code without centralized validation.
- Affected assets:
  - Public search page.
- Risk rating:
  - Medium–High (12)
- Recommendation:
  - Add server-side input validation and output encoding.
  - Add automated XSS tests to CI/CD.
- Target remediation:
  - 60 days.
- Owner:
  - Web Applications Team.

### Finding 2: MFA Not Enforced for All Users
- Description:
  - Optional MFA increases account takeover risk.
- Root cause:
  - Design choice during rollout.
- Affected assets:
  - Patient Portal.
- Risk rating:
  - High (16)
- Recommendation:
  - Gradually require MFA for patients.
  - Provide onboarding guidance.
- Target remediation:
  - 90 days.
- Owner:
  - Identity and Access Management Team.

## 8. Residual Risk and Approval

- Residual risk after remediation:
  - Moderate residual risk for users declining MFA.
- Approved by:
  - [Security Officer Name]
  - Information Security Officer
- Date:
  - [Date]
- Notes:
  - MFA adoption metrics reviewed quarterly.
