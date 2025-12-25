# Document Management System 


## 👥 Team 
- Teammate 1 – Dhaval Solanki 
- Teammate 2 – Anish Shah
- Teammate 3 – Dhrumil Vaghela
- Teammate 4 - Utsav Lakhani

## 🏆 Hackathon Details
- Event: Hackovate LJ
- Track: AI / Responsible Tech

## 📌 Project Overview
Organizations handle large volumes of unstructured data such as documents, reports, contracts, and emails. Traditional methods like manual tagging and keyword-based search are inefficient, error-prone, and slow.
Our project is an AI-driven Document Classification and Indexing System that:
Automatically classifies documents into predefined categories.
Extracts metadata and summaries for intelligent indexing.
Enables semantic search for fast and accurate document retrieval.
Ensures security and role-based access.
Provides a user-friendly frontend dashboard for seamless interaction.

Designed for hackathons, this system is lightweight, extendable, and ideal for real-world organizational use.

---

## 🏗 Tech Stack
- **Frontend:** React.js (dashboard, document view, search/filter)
- **Backend:** FastAPI (Python)
- **Machine Learning / Models:**
 -Document classification with pre-trained models or custom ML pipelines
 -Metadata extraction via spaCy / regex
 -Summarization using extractive methods
 -Semantic search embeddings using SentenceTransformers + FAISS
- **Database:** SQLite for metadata, logs, and user management
- **Deployment:** Docker / Localhost (hackathon demo)

---

## 🔌 API Endpoints
### 1️⃣ Upload Document
`POST /upload`
**Body (FormData):**
```json
{
  "file": "document.pdf",
  "uploader": "username"
}
```
**Response:**
```json
{
  "status": "success",
  "message": "Document uploaded successfully",
  "metadata": { "title": "...", "author": "...", "category": "..." }
}
```

###2️⃣ Document Classification

`POST /classify`
**Body (JSON):**
```json
{
  "document_id": "123"
}
```
**Response:**
```json
{
  "category": "Finance",
  "confidence": 0.93
}
```

###3️⃣ Semantic Search

`POST /search`
**Body (JSON):**
```json
{
  "query": "Quarterly financial report"
}
```

**Response:**
``` json
[
  { "title": "Q2 Finance Report", "relevance": 0.92, "id": "123" },
  { "title": "Budget Analysis", "relevance": 0.89, "id": "124" }
]
```

## 🚀 Installation & Setup
### 🔧 Backend (FastAPI)
#### Clone the repo
- 1. git clone https://github.com/yourusername/document-classification.git
- 2. cd document-classification


# Create virtual environment
python -m venv venv

# Activate environment
# Linux/Mac:
source venv/bin/activate
# Windows:
venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Run server
uvicorn main:app --reload

## 🎨 Frontend (React)
- cd frontend
- npm install
- npm start

##🧪 Usage
-Open the frontend dashboard.
-Upload documents (PDF, DOCX, TXT).
-Documents are classified automatically and metadata extracted.
-Use semantic search to find documents based on meaning
-Access restricted based on user role; HR sees HR documents, Finance sees Finance documents.

## 🎯 Future Scope
.🌍 Multi-language document support
.📹 Real-time video and audio content classification
.📊 Analytics dashboard for document insights
.🤖 Integration with secure/private LLMs for advanced processing

## 📜 License
Open-source / Hackathon use
