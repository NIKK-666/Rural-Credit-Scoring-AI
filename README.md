

---

# 🌾 Jan-Dhan-Drishti (Agri-Credit Intelligence)

**Jan-Dhan-Drishti** is an AI-powered credit underwriting engine designed for rural India. It bridges the gap between traditional banking and marginal farmers by using **Voice-to-JSON** transcription (Bhashini), **Satellite Health Analysis** (Google Earth Engine), and **Fast LLM Extraction** (Groq).

## 🚀 The 60-Second Workflow
1.  **Farmer:** Sends a WhatsApp voice note in a regional language.
2.  **System:** * **Bhashini** transcribes voice to text.
    * **Groq (Llama 3)** extracts loan amount, crop type, and location.
    * **GEE** calculates NDVI (Crop Health) from Sentinel-2 satellite data.
    * **Scoring Engine** fuses satellite and UPI data.
3.  **Banker:** Views a "Yes/No" decision with a map visualization on a dashboard.

---

## 📂 Project Structure

```text
jan-dhan-drishti/
├── app_backend/                # BACKEND: FastAPI Server
│   ├── main.py                 # API Entry (Orchestrator)
│   ├── bhashini_handler.py     # Voice-to-Text REST Integration
│   ├── extraction_engine.py    # AI Slot-filling (Groq)
│   ├── satellite_engine.py     # NDVI Analysis (Google Earth Engine)
│   └── scoring_logic.py        # Credit Decision Algorithm
├── app_frontend/               # FRONTEND: Streamlit Dashboard
│   ├── app.py                  # Banker Command Center
│   └── api_client.py           # Frontend-to-Backend bridge
├── data/                       # STORAGE
│   ├── audio_cache/            # Local storage for farmer audio
│   └── mock_upi.csv            # Sample UPI transaction dataset
└── .env                        # Secret Keys (Not for Git)
```

---

## 🛠️ Tech Stack
* **Intelligence:** Groq (Llama 3 70B)
* **Voice:** Bhashini REST API (MeitY)
* **Vision:** Google Earth Engine (Sentinel-2 Data)
* **Backend:** FastAPI (Python)
* **Frontend:** Streamlit
* **Interface:** Twilio WhatsApp API + Ngrok

---

## 💻 Installation & Setup (Windows)

### 1. Prerequisites
* Python 3.10 or higher.
* An active Google Earth Engine account (run `earthengine authenticate`).

### 2. Clone and Install
```powershell
git clone https://github.com/your-repo/jan-dhan-drishti.git
cd jan-dhan-drishti
python -m venv venv
.\venv\Scripts\activate
pip install -r requirements.txt
```

### 3. Environment Variables
Create a `.env` file in the root directory:
```env
GROQ_API_KEY=your_groq_key
BHASHINI_API_KEY=your_bhashini_key
TWILIO_SID=your_sid
TWILIO_TOKEN=your_token
```

### 4. Running the App
Open two separate PowerShell terminals:

**Terminal 1 (Backend):**
```powershell
cd app_backend
uvicorn main:app --reload
```

**Terminal 2 (Frontend):**
```powershell
cd app_frontend
streamlit run app.py
```

---

## 👥 Team Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Nikhil Barman (AI/AWS)** | Bedrock/Groq Prompting, Satellite Data (GEE), Scoring Logic. | @NIKK-666
| **Harsh Srivastava (UI/Integrator)** | Bhashini REST Integration, Twilio Webhooks, Streamlit UI. | @Harsh Srivastava

---

## 📜 License
This project is built for the **2026 Agri-Fintech Hackathon**. Permission is granted for educational and prototype use only.

---

### **Next Step**
Would you like me to generate the **`requirements.txt`** file content or the **`scoring_logic.py`** to finish your Day 1 setup?
