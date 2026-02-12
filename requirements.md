

---

# 📋 Requirements Specification: Jan-Dhan-Drishti

> **Project:** Rural Credit Scoring AI
> **Target:** Rural & Semi-Urban India (2026)
> **Compliance:** RBI Digital Lending & DPDP Act 2023

---

## 1. Functional Requirements (FR)

| ID | Feature | Description |
| --- | --- | --- |
| **FR-1** | **Multi-Source Ingestion** | System must ingest data from UPI (Account Aggregator), Mandi (e-NAM), and Satellite (Sentinel-2). |
| **FR-2** | **Geospatial Processing** | Automatically calculate NDVI (Crop Health) and moisture indices for provided land coordinates. |
| **FR-3** | **Credit Scoring Engine** | Generate a risk score (0-1000) based on weighted alternative data modalities. |
| **FR-4** | **Bilingual Interface** | Support voice-based interaction and SMS alerts in 22 regional languages via Bhashini. |
| **FR-5** | **Explainability** | For every rejected application, the system must provide top 3 "Reason Codes" (SHAP values). |

---

## 2. Non-Functional Requirements (NFR)

### 2.1 Performance & Scalability

* **Latency:** End-to-end scoring (from request to result) must be `< 3 seconds`.
* **Scalability:** System must handle up to `50,000 concurrent requests` during peak harvest seasons.
* **Availability:** Target `99.9% uptime` using Multi-AZ deployment in AWS Mumbai.

### 2.2 Security & Compliance

* **Data Residency:** All PII (Personally Identifiable Information) must be stored and processed within **ap-south-1 (Mumbai)**.
* **Consent:** System must record an auditable "Consent Log" before fetching any third-party data.
* **Encryption:** AES-256 for data at rest (KMS) and TLS 1.3 for data in transit.

---

## 3. Data Requirements

### 3.1 Input Data Standards

* **Satellite:** High-resolution multi-spectral imagery (10m-20m resolution).
* **Financial:** JSON-formatted transaction logs via the Account Aggregator (AA) ecosystem.
* **Mandi:** Real-time price and quantity data from the Agmarknet/e-NAM portals.

### 3.2 Feature Store Requirements

* **Consistency:** Features used for offline training must exactly match online inference features.
* **Freshness:** UPI features must refresh every `24 hours`; Satellite features every `5 days`.

---

## 4. Technical Constraints

* **Platform:** Must be built using **AWS Managed Services** (Serverless/SageMaker).
* **Cost:** Operational cost must not exceed **₹1.50 per credit score** at scale.
* **Bandwidth:** Mobile interfaces must be optimized for **2G/3G speeds** (low-poly UI/voice notes).

---

## 5. User Acceptance Criteria (UAC)

1. **UAC-1:** Borrower receives a loan eligibility notification in their local language within 60 seconds of submission.
2. **UAC-2:** NBFC Officer can view a "Truth Table" showing the relationship between crop health and transaction volume.
3. **UAC-3:** Auditor can retrieve a "Consent Chain" for any specific transaction in case of a dispute.

---

