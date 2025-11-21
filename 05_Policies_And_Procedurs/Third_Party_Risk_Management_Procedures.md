# Third-Party Risk Management Procedure

## 1. Purpose

The purpose of this procedure is to ensure that all third-party vendors, service providers, and external partners are assessed, approved, and monitored to protect the organization’s data, applications, and systems. This procedure supports compliance with regulatory requirements such as HIPAA, GDPR, SOC 2, and other relevant standards.

## 2. Scope

This procedure applies to:

- All vendors that store, process, or transmit organizational data  
- All service providers with access to internal systems, applications, or infrastructure  
- Any third-party providing software, cloud services, consulting, or managed services  

It includes both new vendor onboarding and ongoing monitoring of existing vendors.

---

## 3. Roles and Responsibilities

### **Vendor Owners / Requestors**
- Initiate vendor onboarding requests  
- Provide business justification and required documentation  
- Ensure vendor complies with approved security requirements  
- Track remediation activities  

### **Information Security (GRC / AppSec)**
- Conduct security risk assessments  
- Review questionnaires, SOC 2 reports, and compliance documentation  
- Identify risks and recommend mitigation actions  
- Approve or reject vendor engagements based on risk  

### **Procurement / Contracts**
- Ensure security requirements and contractual obligations are included in agreements  
- Validate that Business Associate Agreements (BAAs) or Data Processing Agreements (DPAs) are executed when required  

### **Third-Party Vendors**
- Provide accurate and timely security documentation  
- Remediate identified risks within required timelines  
- Notify the organization of incidents or major changes  

---

## 4. Procedure Steps

### **Step 1: Vendor Request Submission**
The business owner submits the following:

- Vendor name  
- Description of service  
- Data types handled (PHI, PII, Internal, Public)  
- Business justification  
- Integration method (SaaS, API, on-prem tool, consulting services)  

If PHI or regulated data is involved, a **BAA or DPA is required**.

---

### **Step 2: Security Questionnaire and Documentation Collection**

The vendor must provide:

- Completed security questionnaire  
- SOC 2 Type II report or ISO 27001 certification (if available)  
- Penetration test summary (last 12 months)  
- Vulnerability management policy  
- Incident response plan  
- Business continuity/disaster recovery documentation  
- List of subprocessors  

If documentation is missing, the vendor is flagged as **higher risk**.

---

### **Step 3: Security Review and Risk Assessment**

GRC performs the assessment:

1. **Review documentation** for gaps or red flags  
2. **Evaluate key control areas**, including:
   - Access control and authentication  
   - Encryption practices  
   - Logging and monitoring  
   - Data protection  
   - Regulatory compliance  
   - Network and infrastructure security  
3. **Score risks** using the application/vendor risk rubric  
4. **Document findings** and required remediation  
5. **Assign overall vendor risk rating**:
   - Low  
   - Medium  
   - High  
   - Critical  

If high or critical risk is identified, additional approval is required.

---

### **Step 4: Risk Remediation and Acceptance**

- GRC assigns remediation items with due dates  
- Vendor provides remediation plan or compensating controls  
- If residual risk remains, business owner must **formally accept the risk** before onboarding continues  
- High-risk residual items must be approved by Information Security leadership  

---

### **Step 5: Contractual Requirements**

Procurement ensures agreements include:

- Security requirements  
- Regulatory clauses  
- Breach notification timelines  
- Data ownership and return/destruction requirements  
- Right to audit  
- BAA or DPA (if applicable)  

Vendor onboarding cannot proceed without required documents.

---

### **Step 6: Onboarding Approval**

A vendor can only be approved when the following conditions are met:

- Security review completed  
- Risk findings documented  
- Required remediation accepted or completed  
- Contractual requirements executed  
- Final approval by GRC  

---

### **Step 7: Ongoing Monitoring**

All vendors undergo periodic reviews based on risk tier:

- **Low-risk** vendors: every 24 months  
- **Medium-risk** vendors: annually  
- **High-risk** vendors: every 6 months  

Monitoring includes:

- Reviewing updated SOC 2 reports or security questionnaires  
- Checking for known breaches  
- Ensuring no major control failures  
- Reassessing risk when services or data usage changes  

Vendors handling PHI or sensitive data require **annual reviews at minimum**.

---

## 5. Risk Ratings and Remediation SLAs

| Risk Level | Description | Expected Remediation Timeline |
|------------|-------------|-------------------------------|
| Critical   | High likelihood + severe impact | 0–30 days |
| High       | Elevated likelihood/impact | 30–60 days |
| Medium     | Moderate impact | 60–90 days |
| Low        | Minor or informational | As needed |

---

## 6. Exceptions

- Must be documented with business justification  
- Must be approved by Information Security  
- Residual risk must be accepted by leadership  

---

## 7. Review Cycle

This procedure must be reviewed annually or when significant changes occur in regulatory requirements or the vendor ecosystem.

---

# Document Owner
Information Security – Governance, Risk, and Compliance
