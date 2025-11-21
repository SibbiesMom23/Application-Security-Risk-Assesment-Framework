# Application Risk Assessment Template

## 1. Application Overview

- Application Name:
- Owner / Business Unit:
- Technical Owner:
- Environment (Prod / Dev / Test):
- Hosting Model (On-prem / Cloud / Hybrid):
- Criticality (High / Medium / Low):

## 2. Data Classification

- Types of data processed:
  - Examples: PHI, PII, PCI, Internal Only, Public
- Highest data classification level:
- Regulatory impact:
  - Examples: HIPAA, PCI-DSS, GDPR, None

## 3. Architecture Summary

- High-level description of the architecture:
- Key components (web server, app server, database, APIs, third-party integrations):
- Network exposure (internal only, VPN, internet-facing):
- Authentication and authorization model:

## 4. Threats and Vulnerabilities

- Known threats:
  - Examples: data exfiltration, account takeover, injection, misconfiguration
- Known or suspected vulnerabilities:
- Results from recent testing (if available):
  - Vulnerability scan:
  - Penetration test:
  - Code review:

## 5. Security Controls

- Access control:
  - SSO used? (Yes/No)
  - MFA enforced? (Yes/No)
  - Role-based access control? (Yes/No/Partial)

- Data protection:
  - Encryption in transit (TLS version, ciphers):
  - Encryption at rest (database, storage):
  - Key management approach:

- Logging and monitoring:
  - Centralized logging? (Yes/No)
  - Security alerts configured? (Yes/No)
  - Who reviews alerts and how often?

- Hardening and configuration:
  - Baseline configuration standard used:
  - Patch management process:

## 6. Risk Scoring

Use a simple 1–5 scale for both likelihood and impact.

- Likelihood (1–5):
- Impact (1–5):

**Risk Score = Likelihood × Impact**

- Calculated Risk Score:
- Risk Rating (High / Medium / Low):

## 7. Findings and Recommendations

### Finding 1
- Description:
- Root cause:
- Affected assets:
- Risk rating:
- Recommended remediation:
- Target remediation date:
- Owner:

### Finding 2
- Description:
- Root cause:
- Affected assets:
- Risk rating:
- Recommended remediation:
- Target remediation date:
- Owner:

(Add more findings as needed.)

## 8. Residual Risk and Approval

- Residual risk after planned remediation:
- Accepted by (name, role):
- Date of acceptance:
- Conditions or comments:
