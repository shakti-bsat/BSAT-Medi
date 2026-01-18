#  BSAT-Medi

**Intelligent Prescription Assistant**

BSAT-Medi is an AI-powered healthcare assistant that helps users understand their medical prescriptions and verify the safety of over-the-counter (OTC) medicine purchases.

---

##  Features

###  Prescription Analysis
- **OCR & Extraction:** Upload handwritten or printed prescriptions (PDF/Image) and get structured data extraction using Google Gemini Vision.
- **Interactive Chat:** Ask questions about your prescription like *"When should I take this medicine?"* or *"What are the side effects?"*
- **Context Memory:** The AI remembers your conversation history for natural follow-up questions.

###  OTC Safety Checker
- **Vector-Powered Search:** Uses Pinecone semantic search to find medicine matches efficiently.
- **AI Verification:** LLM-based confirmation ensures accurate categorization.
- **Clear Results:** Medicines are classified as:
  -  **Safe to Buy** - Available OTC
  -  **Consult Doctor** - Requires professional advice

##  Project Structure

```
bsat-medi/
├── app.py                 # Main Streamlit application
├── requirements.txt       # Python dependencies
├── .env                   # Environment variables (not tracked)
│
├── src/
│   ├── auth.py            # User authentication (MongoDB + bcrypt)
│   ├── config.py          # Configuration & environment loading
│   ├── extractor.py       # Prescription OCR using Gemini Vision
│   ├── graph.py           # LangGraph RAG pipeline
│   ├── ingestion.py       # File processing utilities
│   ├── memory.py          # Chat history & session management
│   ├── otc_data.py        # OTC medicines list (structured data)
│   ├── otc_manager.py     # OTC verification engine
│   ├── utils.py           # Helper functions & logging
│   └── vector_store.py    # Pinecone vector database interface
│
├── data/
│   ├── input/             # Uploaded prescription files
│   └── processed/         # Processed outputs
│
└── tests/
    └── test_otc_check.py  # OTC verification tests
```

---

##  Getting Started

### Prerequisites
- Python 3.10+
- MongoDB Atlas account (or local MongoDB)
- Pinecone account
- Google Cloud account (Gemini API) (prefer gemini 2.5 flash lite, cheapest and fastest model out there with good accuracy )
- if you want run locally i prefer gemma 3 4 billion model using ollama.

