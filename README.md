# civic_setu
# 🇮🇳 CivicPulse AI
### One India. One Civic Intelligence Platform.

**Report locally. Connect nationally. Improve collectively.**

CivicPulse AI is a nationwide, AI-powered civic issue reporting and infrastructure intelligence platform designed to connect Indian citizens with the appropriate government authorities.

Citizens can simply upload a photograph of a civic problem. CivicPulse AI uses artificial intelligence, GPS and geographical intelligence to identify the issue, determine its location, identify the likely responsible authority and facilitate complaint submission through authorized government integrations.

Our mission is to make reporting public infrastructure problems simple, transparent and accessible to everyone.

---

## 🌍 The Problem

Across India, citizens encounter everyday infrastructure problems:

- Damaged roads and potholes
- Broken streetlights and electric poles
- Water leakage and supply disruptions
- Blocked drainage and garbage accumulation
- Flooding, damaged canals and irrigation problems
- Fallen trees and public safety hazards
- Public transport and traffic-related issues

However, reporting these problems can be complicated.

Citizens often struggle to identify the correct department, locate the appropriate complaint portal and follow up on unresolved issues.

Government authorities also need better ways to identify recurring problems, coordinate departments and prioritize infrastructure maintenance.

## 💡 Our Solution

CivicPulse AI simplifies the entire civic complaint process.

**Snap → Detect → Locate → Identify → Submit → Track**

1. Citizens upload a photograph of a civic issue.
2. AI identifies the problem and suggests its category and severity.
3. GPS identifies the geographical location with user permission.
4. The jurisdiction engine identifies the state, district and local authority.
5. The authority engine determines the likely responsible department using jurisdiction and infrastructure ownership information.
6. The complaint is submitted through an authorized government integration, where available.
7. Citizens track the complaint and receive status updates.

Where direct government integration is unavailable, CivicPulse provides the relevant official complaint channel rather than falsely claiming that a government complaint has been submitted.

---

## ✨ Key Features

### 📸 1. AI-Powered Issue Detection
- Analyse uploaded photographs.
- Identify different civic infrastructure problems.
- Automatically suggest issue categories.
- Estimate visible severity.
- Generate complaint descriptions.
- Identify potentially duplicate reports.

### 📍 2. GPS-Based Location Detection
- Request device location permission.
- Automatically capture geographical coordinates.
- Identify state, district and local administrative area.
- Display the issue location on an interactive map.
- Allow manual location correction.

### 🏛️ 3. Intelligent Authority Routing
Identify the appropriate government authority based on:
- Issue category.
- Geographical location.
- Administrative jurisdiction.
- Infrastructure ownership.
- Configured department responsibilities.

### 🇮🇳 4. Nationwide Support
Designed to support all Indian states and Union Territories through a configurable authority directory.

The platform will not depend on Kerala-specific departments. Each state can have its own department names, local bodies, routing rules and integration configurations.

### 📊 5. Public Civic Map
- View nearby reported issues.
- Explore infrastructure problems geographically.
- Filter reports by category and status.
- Identify recurring problem hotspots.
- Track publicly visible resolution progress.

### 🔔 6. Complaint Tracking
- Unique CivicPulse report IDs.
- Complaint status timelines.
- Government acknowledgement tracking where integrated.
- Resolution updates.
- Citizen verification and issue reopening.

### 🧠 7. Predictive Infrastructure Maintenance
- Identify recurring infrastructure problems.
- Analyse historical complaint patterns.
- Detect infrastructure hotspots.
- Generate prototype maintenance risk scores.
- Recommend inspection priorities.

Predictive scores are decision-support indicators, not certified engineering assessments.

### 🏢 8. Government Dashboard
- View incoming civic reports.
- Filter by department and location.
- Monitor complaint progress.
- Identify unresolved issues.
- Explore geographic hotspots.
- Review maintenance intelligence.

---

## 🏗️ System Architecture

```text
                 CITIZENS
                     |
                     v
              REACT FRONTEND
                     |
          Photo Upload + GPS Location
                     |
                     v
               FLASK BACKEND
                     |
          +----------+----------+
          |                     |
          v                     v
      AI ENGINE          GEOLOCATION ENGINE
          |                     |
          v                     v
    Image Detection       Jurisdiction Detection
    Severity Analysis     State / District / City
    Duplicate Detection   Asset Ownership
          |                     |
          +----------+----------+
                     |
                     v
             AUTHORITY ROUTER
                     |
                     v
          GOVERNMENT CONNECTORS
                     |
           +---------+---------+
           |                   |
           v                   v
     Authorized API       Official Portal
           |                   |
           +---------+---------+
                     |
                     v
             COMPLAINT TRACKING
                     |
                     v
               CITIZENS
```

---

## 🛠️ Technology Stack

| Component | Technology |
|---|---|
| Frontend | React.js + Vite |
| Styling | Tailwind CSS |
| Backend | Python + Flask |
| Database | PostgreSQL |
| Geospatial Database | PostGIS |
| Mapping | Leaflet + OpenStreetMap |
| AI Image Analysis | Cloud Vision AI API |
| Geolocation | Browser Geolocation API |
| Geocoding | Reverse Geocoding Service |
| Image Storage | Cloudinary |
| Version Control | Git + GitHub |
| Deployment | Render / Cloud Hosting |

---

## 📂 Project Structure

```text
civicpulse-ai/
│
├── frontend/
│   ├── public/
│   └── src/
│       ├── assets/
│       ├── components/
│       ├── pages/
│       ├── services/
│       ├── hooks/
│       └── App.jsx
│
├── backend/
│   ├── routes/
│   ├── models/
│   ├── services/
│   ├── integrations/
│   ├── config/
│   ├── run.py
│   └── requirements.txt
│
├── ai-engine/
│   ├── vision/
│   ├── geolocation/
│   ├── authority/
│   ├── duplicate/
│   └── predictive/
│
├── docs/
│   ├── architecture.md
│   └── api-contract.md
│
├── sample-data/
│
├── .gitignore
└── README.md
```

---

## ⚙️ Installation and Setup

### Prerequisites

Install the following:

- Python 3.11+
- Node.js and npm
- Git
- PostgreSQL
- Visual Studio Code

### 1. Clone the repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
cd civicpulse-ai
```

### 2. Setup the frontend

```bash
cd frontend

npm install

npm run dev
```

The frontend will be available at:

```text
http://localhost:5173
```

### 3. Setup the backend

Open another terminal:

```bash
cd backend

py -3.11 -m venv venv
```

Activate the virtual environment on Windows:

```powershell
venv\Scripts\activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Start the Flask server:

```bash
python run.py
```

The backend will be available at:

```text
http://127.0.0.1:5000
```

### 4. Environment Variables

Create a `.env` file in the appropriate project directory.

Example:

```env
FLASK_ENV=development
SECRET_KEY=your_secret_key

DATABASE_URL=your_postgresql_connection_string

AI_API_KEY=your_ai_api_key

CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_cloudinary_key
CLOUDINARY_API_SECRET=your_cloudinary_secret
```

Never commit `.env` files, passwords or API keys to GitHub.

---

## 👥 Team Members

| Member | Role | Responsibilities |
|---|---|---|
| Sai Sainath | Project Lead & Technical Integrator | Architecture, GitHub, integration, testing and deployment |
| Member 2 | Frontend Developer | React, UI/UX, reporting interface and citizen dashboard |
| Member 3 | Backend Developer | Flask APIs, PostgreSQL and complaint management |
| Member 4 | AI & GIS Developer | AI detection, GPS, jurisdiction and predictive intelligence |

---

## 🗺️ Development Roadmap

- [ ] Project foundation and GitHub repository
- [ ] Public-facing React website
- [ ] Citizen reporting interface
- [ ] GPS-based location detection
- [ ] AI-powered image classification
- [ ] India-wide authority directory
- [ ] Jurisdiction and asset ownership engine
- [ ] Government submission connector framework
- [ ] Public civic issue map
- [ ] Complaint tracking system
- [ ] Predictive maintenance engine
- [ ] Government administration dashboard
- [ ] Testing and security
- [ ] Cloud deployment

---

## 🔐 Privacy, Security and Transparency

CivicPulse AI aims to:

- Request location permission before accessing GPS.
- Protect personal and contact information.
- Secure uploaded images and user data.
- Validate uploaded files.
- Prevent unauthorized access to government integrations.
- Clearly distinguish CivicPulse reports from officially submitted government complaints.
- Protect private citizen information on public maps.
- Keep AI recommendations subject to human review.

Government integrations will only be enabled through authorized channels.

---

## 🎯 Our Vision

We envision an India where reporting public infrastructure problems is as simple as taking a photograph.

CivicPulse AI aims to build a connected civic ecosystem where citizens can report problems, authorities can coordinate solutions and infrastructure organisations can identify recurring maintenance needs.

**One India. One Civic Intelligence Platform.**

---

## 📌 Project Information

**Project Name:** CivicPulse AI  
**Project Type:** AI-Powered Civic Technology Platform  
**Target Market:** India  
**Primary Users:** Indian Citizens  
**Customers:** Government Organisations and Infrastructure Operators  
**Development Model:** Team-Based Development  
**Project Stage:** Prototype / Under Development

---

*Built with the vision of making India's public infrastructure more connected, transparent and responsive.* 🇮🇳
