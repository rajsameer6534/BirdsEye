# 🦅 BirdEye: AI-Powered Remote Sensing for Urban Planning

**BirdEye** is a powerful **Next.js 15** application designed to provide rapid, remote-sensing-based geospatial analyses, making it an invaluable tool for **urban planners, researchers, and policymakers**.

It features a **chatbot-like interface** where you can interact using natural language to perform complex environmental monitoring. BirdEye leverages **Google Earth Engine (GEE)** in the backend for real-time processing of massive satellite datasets, giving you immediate insights for:

- 🌡️ **Urban Heat Island (UHI) Mitigation**  
- 🏙️ **Land-Use/Land-Cover Change Monitoring**  
- 🌬️ **Air Quality Assessment** *(in development)*  

BirdEye also allows you to **upload your own vector data** and utilize its **Retrieval-Augmented Generation (RAG)** system to integrate geospatial findings with custom textual knowledge bases, such as urban policy documents or zoning regulations.

---

## 🚀 Project Demo
Developed and maintained by **Sameer Raj**.

---

## ✨ Key Features for Urban Insight

### 🔹 Natural Language Geospatial Queries
- Interact with the system using a **chat-style interface**.  
- The AI Assistant translates natural language requests into **complex geospatial functions**.

### 🔹 Integrated Analysis Toolkit
- **Urban Heat Island (UHI) Analysis** → Quantify and map temperature disparities critical for planning.  
- **Land-Use/Land-Cover Mapping & Change Detection** → Track urbanization, deforestation, and ecosystem changes using **Google DynamicWorld**.  
- **Air Pollutants Analysis** *(in development)* for urban air quality monitoring.  
- Integration of **custom AI models via Vertex AI** for specialized land cover tasks.  

### 🔹 Data Integration and Custom Knowledge
- **Import your own vector data** (e.g., city boundaries, planning zones) for precise analysis masking and queries.  
- **RAG Knowledge Base** → Upload documents to build a local knowledge base, allowing the AI to combine environmental data with urban policy information.  

---

## 💻 Tech Stack

- **Frontend:** Next.js 15  
- **Mapping:** Maplibre GL  
- **Cloud & Data:**  
  - Google Earth Engine (GEE) → Core engine for remote sensing & processing  
  - Google Cloud Platform (GCP): Vertex AI (Custom Models), Cloud Run  
- **AI/LLM:** Vercel AI, OpenAI (ChatGPT API), LangChain (RAG)  
- **Database & Auth:** Supabase (PostgreSQL)  
- **Spatial Operations:** Turf  

---

## ⚡ Getting Started

### 1. Prerequisites
- **Google Earth Engine (GEE):** You must create a GEE account and a project.  
  👉 [Get Started with GEE](https://earthengine.google.com) (free for non-commercial use)  
- **Node.js & npm**  

---

### 2. Installation

```bash
# Clone the repository
git clone https://github.com/rajsameer6534/BirdsEye.git
cd BirdsEye

# Install dependencies
npm install
