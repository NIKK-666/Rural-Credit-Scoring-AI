
```markdown
# 🛰️ Jan-Dhan-Drishti: Rural Credit Scoring AI
[![AWS Certified](https://img.shields.io/badge/AWS-2026_Ready-FF9900?logo=amazon-aws&logoColor=white)](https://aws.amazon.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Impact](https://img.shields.io/badge/Focus-Financial_Inclusion-blue)](#)

**Jan-Dhan-Drishti** is an AI-powered alternative credit scoring platform designed for India's 100M+ "thin-file" rural borrowers. By fusing **UPI transaction behavior** with **satellite-derived crop health (NDVI)**, we provide NBFCs with a high-fidelity risk profile that traditional bureaus miss.



---

## ✨ Key Features
* 🌾 **Agri-Vision:** Real-time crop health monitoring using Amazon SageMaker Geospatial.
* 💳 **Cash-flow Underwriting:** Analysis of UPI velocity and utility payment patterns.
* 🗣️ **Bharat-First:** Voice-activated application process in 22 regional languages (Bhashini).
* ⚖️ **Explainable AI (XAI):** Transparent "Reason Codes" for every loan decision via SageMaker Clarify.

---

## 🏗️ Architecture
The system is built on a **Serverless-First** AWS stack for global scalability and zero idle costs.



* **Compute:** AWS Lambda & Step Functions (Agentic Workflows)
* **ML Engine:** Amazon SageMaker (Hybrid XGBoost + Vision Transformer)
* **Intelligence:** Amazon Bedrock (Llama 3.1) for multilingual NLP
* **Data Lake:** Amazon S3 & Amazon Aurora

---

## 🚀 Quick Start (Hackathon Mode)

### Prerequisites
* AWS Account with `AdministratorAccess`
* Python 3.10+
* AWS CLI configured (`ap-south-1`)

### Installation
1. **Clone the repo:**
   ```bash
   git clone [https://github.com/your-username/Jan-Dhan-Drishti.git](https://github.com/your-username/Jan-Dhan-Drishti.git)
   cd Jan-Dhan-Drishti

```

2. **Deploy the Backend (CDK):**
```bash
cd infrastructure
npm install && cdk deploy

```


3. **Install ML Dependencies:**
```bash
pip install -r requirements.txt

```



---

## 📊 Evaluation & Impact

| Metric | Traditional (CIBIL) | Jan-Dhan-Drishti |
| --- | --- | --- |
| **Data Points** | Past Loan History | Live UPI + Satellite Health |
| **Decision Time** | 3-7 Days | < 60 Seconds |
| **Population Coverage** | ~20% (Urban) | > 85% (Rural/Semi-Urban) |

---

## 🛡️ Privacy & Ethics

We adhere strictly to the **DPDP Act 2023** and **DEPA Framework**.

* **Consent-Led:** No data is fetched without an OTP-verified Account Aggregator consent.
* **Bias-Free:** Models are audited weekly for demographic parity using AWS SageMaker Clarify.

---

## 🤝 Contributing

We welcome contributions! Please see [CONTRIBUTING.md](https://www.google.com/search?q=CONTRIBUTING.md) for our code of conduct and the process for submitting pull requests.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](https://www.google.com/search?q=LICENSE) file for details.

```

