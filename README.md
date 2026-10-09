# 🧠 AI Security Log Classifier
### Enterprise‑Grade AI‑Driven DevSecOps Security Platform

A cloud‑ready, intelligent security analytics engine that automatically classifies, detects, and remediates threats across logs and pipelines.  
It combines **machine learning**, **LLM‑powered remediation**, and **DevSecOps automation** to deliver continuous compliance and zero‑trust security.

---

## 🔐 Key Features
- AI‑powered log classification (TF‑IDF + Logistic Regression)
- LLM remediation engine for automated threat response
- Zero‑Trust architecture with IAM, SCPs, and OPA Rego policies
- Continuous compliance via AWS Config, Security Hub, and Audit Manager
- Cloud‑agnostic deployment (AWS, Azure, or hybrid)
- Infrastructure‑as‑Code security using Terraform, CDK, and cfn‑guard
- Automated evidence collection and compliance reporting

---

## ☁️ Architecture
| Layer | Technology | Purpose |
|-------|-------------|----------|
| Frontend | FastAPI | RESTful API for log ingestion and classification |
| AI Layer | TF‑IDF + Logistic Regression + LLM | Log classification and remediation |
| Infrastructure | Terraform + AWS CDK | Secure IaC deployment |
| Security Controls | SCPs, OPA Rego, Cedar | Policy enforcement |
| Monitoring | CloudWatch + GuardDuty | Threat detection and anomaly analysis |
| Compliance | Config + Audit Manager | Continuous compliance |

---

## ⚙️ DevSecOps Workflow
1. Code Commit → GitHub Actions triggers IaC scan  
2. Build & Deploy → Terraform/CDK deploys secure infrastructure  
3. Log Ingestion → FastAPI receives logs from cloud workloads  
4. AI Classification → ML model categorizes threats  
5. LLM Remediation → Automated response via Bedrock or Azure OpenAI  
6. Compliance Audit → AWS Config + Audit Manager generate evidence  

---

## 🧰 Installation
```bash
git clone https://github.com/ilowilfred-pixel/ai-security-log-classifier.git
cd ai-security-log-classifier
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
uvicorn src.main:app --reload
## 🧪 Usage
```bash
curl -X POST http://localhost:8000/classify \
-H "Content-Type: application/json" \
-d '{"log": "Unauthorized access attempt detected"}'
{
  "classification": "Critical Threat",
  "remediation": "IAM policy updated, access revoked"
}

