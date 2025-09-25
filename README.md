🦅 BirdsEye: AI-Powered Geospatial Intelligence Platform (PS2: Multimodal Earth Analyst)
BirdsEye is an advanced, Next.js 15 application engineered as an AI-powered geospatial intelligence platform. It is designed to autonomously fuse time-series satellite imagery with diverse spatial and semantic datasets to deliver dynamic, evidence-backed insights for any location on Earth.

Leveraging Google Earth Engine (GEE) in the backend and a natural language Chat-Style Interface, BirdsEye moves beyond static maps to offer modular, AI-driven workflows for complex analyses like change detection, urban planning, and socioeconomic assessments.

The platform integrates Retrieval-Augmented Generation (RAG) to merge geospatial analysis with non-geospatial (textual) knowledge, providing Evidence-Based Storytelling through interactive dashboards and narrative summaries. It includes full authentication and database integrations for a complete user experience.

🎯 Objective: Multimodal Earth Analyst
The core objective of BirdsEye is to solve the fragmentation and inaccessibility of modern geospatial analysis. It does this by creating a unified system that integrates:

Satellite Imagery with AI-driven change detection.

Vector Geodata (e.g., OpenStreetMap).

Tabular Data (Census, socioeconomic, real estate datasets).

Environmental and Planning Data.

This fusion delivers deep, dynamic insights inaccessible through traditional static GIS tools.

✨ Key Features & Innovation
Feature	PS2 Objective Alignment	Description
Multimodal Data Fusion	Core Objective	Seamlessly align and analyze raster, vector, tabular, and text data across both space and time to provide a complete picture of an area.
Modular Tool Chaining	Ideas to Explore	The AI Assistant can intelligently select and combine geospatial tools (e.g., NDVI analysis + OSM + document summarization) based on a user's natural language intent.
Evidence-Based Storytelling	Ideas to Explore	Generate concise, narrative summaries and reports that are directly grounded in the visual and statistical evidence derived from the analysis.
Transparent Source Control	User-Centric Sourcing	Allows users to define trusted data sources (e.g., municipal GIS maps) and provides an audit trail, citing all sources used in the final response.
Interpretable Visualizations	Ideas to Explore	Outputs include interactive dashboards, dynamic maps using Maplibre GL, and charts that allow users to explore and validate the AI's insights.
RAG & Knowledge Base	Semantic Data Fusion	Upload custom documents to build a local knowledge base, enabling the AI to combine location-based insights with custom document knowledge.
Custom AI & GEE Integration	Analysis Toolkit	Leverages Google Earth Engine (GEE) for real-time remote sensing, combined with Vertex AI for deploying custom vision models (e.g., specific land cover tasks).

Export to Sheets
💻 Tech Stack
Frontend: Next.js

Cloud & Processing: Google Cloud Platform (GCP)

Google Earth Engine (GEE): Remote-sensing data invocation and processing.

Vertex AI: Hosting custom AI vision models for advanced classification.

Cloud Run: For containerized analysis and model invocation.

AI/LLM: Vercel AI, OpenAI (ChatGPT API), LangChain (RAG)

Database & Auth: Supabase (PostgreSQL)

Geospatial Utilities: Turf (for spatial operations), Maplibre GL (for dynamic map display)

🚀 Getting Started
1. Installation
Clone the repo and install dependencies:

Bash

git clone https://github.com/rajsameer6534/BirdsEye.git
cd BirdsEye
npm install
GEE Setup: Create a Google Earth Engine (GEE) account and project. This is essential for all remote-sensing analysis. GEE is currently free for non-commercial use:
https://earthengine.google.com

2. Set up Environment Variables
Create a .env.local file with the required credentials:

Bash

# General
BASE_URL=http://localhost:3000

# Google Cloud Platform (GCP) - Crucial for GEE and custom models
GOOGLE_MAPS_API_KEY=           
VERTEXTAI_ENDPOINT_BASE_URL=   
GEE_CLOUD_RUN_URL=             
GCP_BUCKET_NAME=               
GCP_SERVICE_ACCOUNT_KEY=       # Service Account key for GEE functions (must have all required permissions)

# Large Language Model (LLM)
OPENAI_API_KEY=                # Can be changed to another API supported by Vercel AI SDK.

# Supabase (Database & Authentication)
NEXT_PUBLIC_SUPABASE_URL=
NEXT_PUBLIC_SUPABASE_ANON_KEY=

# Optional: Esri Integration
ARCGIS_CLIENT_ID=
ARCGIS_CLIENT_SECRET=
ARCGIS_REDIRECT_URI=

# Optional: Feedback Submission (Mailgun)
MAILGUN_API_KEY=
MAILGUN_DOMAIN=
RECIPIENT_EMAIL=
SENDER_EMAIL=
3. Run the Development Server
Bash

npm run dev
Visit http://localhost:3000 to view the application.

🛢️ How to Set up Supabase Database, Storage Bucket, & Authentication
BirdsEye uses Supabase for its PostgreSQL database and authentication. A free-tier plan is available and sufficient for development.

Database & Auth Setup: Set up a Supabase project and use the database schema found in the db-schema folder to configure your tables and authentication rules.

Knowledge Base Storage (Optional): To use the RAG feature, create a storage bucket on Supabase and name it exactly: documents_bucket. This bucket stores the PDF documents you upload for the Knowledge Base.

📊 Available Geospatial Analyses
The following are examples of the modular analyses currently available in the platform. These modules can be combined by the AI through tool-chaining to answer complex, multimodal questions:

#	Analysis Type	Description
1	Urban Heat Island (UHI) Analysis	Evaluates temperature variations in urban areas compared to rural surroundings.
2	Land-Use/Land-Cover Mapping	Uses Google DynamicWorld to classify land cover types.
3	Land-Use/Land-Cover Change Mapping	Detects changes in land use over time using Google DynamicWorld.
4	Air Pollution Analysis (Partial Implementation)	Analyzes air pollution patterns and trends.

Export to Sheets
💡 Considerations
Production Readiness: This app is not yet production-ready. Some functionalities are still under development, and known/unknown bugs exist.

GEE Dependency: All remote-sensing analyses are based on GEE. Correct GEE environment setup is mandatory.

Interpretation: GEE-based examples use simple implementations. Care should be taken while interpreting results, as some source data may not be fully up-to-date.

🤝 Contributing & Support
The BirdsEye platform is a massive undertaking, and contributions are highly encouraged to advance the Multimodal Earth Analyst objective!

How to Contribute: Please check out the Contributing Guidelines before submitting a pull request.

Contact: If you are interested in contributing, have a feature request, or need to report a bug, please [suspicious link removed] on GitHub. For direct inquiries, you may reach the primary developer, Sameer Raj, via an open issue.
