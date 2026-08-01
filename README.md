<div align="center">

# RespiGuard: AI-Powered Respiratory Health Assistant

<img alt="Wlogo" src="https://github.com/user-attachments/assets/58614a69-d500-4090-a860-d2e4f2430296" height="120"/>

<br><br>

![React](https://img.shields.io/badge/Frontend-React%20%2B%20Vite-61DAFB)
![Glassmorphism](https://img.shields.io/badge/UI-Glassmorphism-7C3AED)
![Flask](https://img.shields.io/badge/Backend-Flask-000000)
![Gemini](https://img.shields.io/badge/AI-Google%20Gemini-8E75B2)
![Gemini%20Embeddings](https://img.shields.io/badge/Embeddings-Gemini-4285F4)
![Pinecone](https://img.shields.io/badge/Vector%20DB-Pinecone-0DBD8B)
![Firebase](https://img.shields.io/badge/Database-Firebase-FFCA28)
</div>

`created & enhanced during Hack Zenith 2026`

> **“Others measure the air; we measure its impact on you.”**
>
> A personalized medical digital twin that combines real-time hyper-local air quality data with AI-driven clinical guidance to protect respiratory patients.

---

## 🚩 The Problem
- **Generic Data:** Standard weather apps show city-wide averages, ignoring the pollution right outside your door.
- **Panic, Not Pragmatism:** Global AQI standards often flag Indian air as "Hazardous" 24/7, causing alarm fatigue without actionable advice.
- **Lack of Medical Context:** A general "Avoid Outdoors" warning is useless for an office commuter. Patients need advice tailored to their specific conditions (e.g., Asthma) and medications.

## 🟢 The Solution: RespiGuard
RespiGuard moves beyond passive monitoring to **active health defense**:
1.  **🚦 Visual Risk Dashboard:** Converts complex PM2.5 numbers into a simple Red/Yellow/Green traffic light system.
2.  **🩺 AI Medical Twin:** Uses RAG (Retrieval-Augmented Generation) to give advice based on **your** specific condition and meds.
3.  **🧠 Pragmatic Risk Engine:** Distinguishes between "Exercise" (Avoid) and "Commute" (Wear N95), tailored to the Indian context.
4.  **🚨 Smart SOS:** A "Voice for the Voiceless" panic button that broadcasts location and medical history to guardians when the patient cannot speak.

---

## 📸 Screenshots
<table >
  <tr>
    <th align="center">Home Page</th>
    <th align="center">Dashboard</th>
    <th align="center">Ask AI</th>
  </tr>
  <tr>
    <td align="center"><img width="1897" height="866" alt="image" src="https://github.com/user-attachments/assets/8ff56546-c756-43c1-9445-20aede7fa518" width="300"/></td>
    <td align="center"><img width="1901" height="869" alt="image" src="https://github.com/user-attachments/assets/6a500995-08d5-4ffc-b603-ae801771dc77" width="300"/></td>
    <td align="center"><img width="1901" height="865" alt="image" src="https://github.com/user-attachments/assets/1325e59a-c514-49a4-8552-aa9d6912596e" width="300"/></td>
  </tr>
  <tr>
    <th align="center">User Profile</th>
    <th align="center">SOS Page</th>
    <th></th>
  </tr>
  <tr>
    <td align="center" ><img width="1900" height="868" alt="image" src="https://github.com/user-attachments/assets/0b205177-412c-4f92-a6d6-60ad1e37d53b" width="300"/></td>
    <td align="center"><img width="1900" height="863" alt="image" src="https://github.com/user-attachments/assets/71e9eb29-5313-4c8d-8100-533fdc9c8e9e" width="300"/></td>
    <td></td>
  </tr>
</table>


---

## ⚙️ Technology Stack

### **Frontend (Client)**
* **React + Vite:** Fast, modern UI with "Frutiger Aero" glassmorphism aesthetics.
* **Tailwind CSS:** For responsive and clean styling.
* **Lucide React:** Beautiful, consistent icons.

### **Backend (Server)**
* **Python Flask:** REST API server handling business logic.
* **LangChain:** Orchestrator for RAG (Retrieval-Augmented Generation).
* **Google Gemini 2.5 Flash:** High-speed LLM for medical reasoning and chat.
* **Pinecone:** Vector Database for storing GINA/WHO medical guidelines.

### **Services & APIs**
* **Firebase Firestore:** NoSQL database for User Profiles and History.
* **OpenWeatherMap API:** Real-time hyper-local AQI & PM2.5 data.
* **Twilio API:** SMS, WhatsApp, and Voice Call alerts for the SOS system.

---

## 🚀 Features

### 1. Hyper-Local AQI Dashboard
Real-time pollution tracking that calculates the **Indian National Air Quality Index (NAQI)**. It provides specific "Activity Cards" telling you if it's safe to:
- 🏃 Go for a run (Outdoor Exercise)
- 🚶 Walk to work (Commute)
- 🏠 Open windows (Ventilation)

### 2. The AI "Medical Doctor" (Chatbot)
Ask questions like *"Can I go out if I use my inhaler?"*
* **Context-Aware:** Knows your specific condition (e.g., Bronchial Asthma) and current medications.
* **Fact-Based:** Answers are grounded in verified medical documents (RAG), not generic AI hallucinations.
* **Memory:** Remembers previous turns in the conversation for a natural flow.

### 3. Smart SOS System
In a respiratory emergency, every second counts. One tap triggers:
* **WhatsApp Alert:** Sends live Google Maps location + Patient Medical Profile to guardians.
* **Voice Call:** Automated call to guardians reading out the emergency context.
* **First Aid Voice Mode:** Reads out immediate calming steps to the patient.

---

## 🛠️ Installation & Setup

### Prerequisites
* Node.js & npm
* Python 3.9+
* Firebase Project Credentials
* API Keys (Google Gemini, OpenWeather, Pinecone, Twilio)

### 1. Clone the Repository
```
git clone https://github.com/tulu-g559/Respi_Guard.git
cd RespiGuard
```
### 2\. Backend Setup
```
cd server  
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate  
pip install -r requirements.txt   `
```
_Create a .env file in /server with your keys:_

```
GOOGLE_API_KEY=your_key  

PINECONE_API_KEY=your_key 
PINECONE_INDEX=your_index_name 
OPENWEATHER_API_KEY=your_key  

TWILIO_SID=your_sid  
TWILIO_AUTH_TOKEN=your_token  
TWILIO_FROM_NUMBER=your_number
```
### 3\. Frontend Setup
```
cd client  
npm install
```
_Create a .env file in /client with your Firebase config:_

```
VITE_FIREBASE_API_KEY=your_firebase_api_key
VITE_FIREBASE_AUTH_DOMAIN=your_firebase_auth_domain
VITE_FIREBASE_PROJECT_ID=your_firebase_project_id
VITE_FIREBASE_STORAGE_BUCKET=your_firebase_storage_bucket
VITE_FIREBASE_MESSAGING_SENDER_ID=your_firebase_messaging_sender_id
VITE_FIREBASE_APP_ID=your_firebase_app_id
VITE_FIREBASE_MEASUREMENT_ID=your_firebase_measurement_id
```

### 4\. Run the App

**Terminal 1 (Backend):**
```
python app.py
```

**Terminal 2 (Frontend):**
```   
npm run dev
```

## 🔮 Future Roadmap

*   [ ] **Wearable Integration:** Connect with smartwatches to detect SpO2 drops automatically.
    
*   [ ] **Community Heatmap:** Crowdsource air quality data to find "Clean Air Pockets" in cities.
    
*   [ ] **Vernacular Voice Mode:** Support for Hindi/Bengali voice commands for rural accessibility.
    

## 🤝 Contributing

Contributions are welcome! Please fork the repository and submit a pull request.
