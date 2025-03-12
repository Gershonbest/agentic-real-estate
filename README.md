# Agentic Real Estate Chatbot

## Overview
This project is an **Agentic Real Estate Chatbot** built with **FastAPI, LangChain, and LangGraph**. It allows users to search for properties, estimate prices, and handle real estate-related queries using AI-powered agents.

## Features
- 🌍 **Property Search**: Fetch real estate listings based on user preferences.
- 💰 **Price Estimation**: Predict property values using an external ML model.
- 🏗 **Modular Architecture**: Uses an extendable adapter pattern for integrating new services.
- 🚀 **Agentic AI**: Powered by LangChain and LangGraph for reasoning and decision-making.
- ⚡ **FastAPI Backend**: Lightweight and high-performance API for chatbot interactions.
- 📥 **ETL & Data Management**: Handles data ingestion, transformation, and storage in a vector database for RAG-based retrieval.

## Project Structure
```
agentic_real_estate/
│── app/
│   ├── main.py                 # FastAPI entry point
│   ├── routes.py               # API endpoints
│
│── agents/
│   ├── agent.py                # AI agent with LangGraph
│   ├── tools.py                # Tools for agent tasks
│
│── models/
│   ├── property.py             # Property listing model
│   ├── user.py                 # User query model
│
│── services/
│   ├── property_service.py      # Adapter for fetching properties
│   ├── price_service.py         # Adapter for price estimation
│
│── etl/
│   ├── __init__.py             # ETL module initialization
│   ├── data_ingestion.py       # Fetch and clean property data
│   ├── vector_db.py            # Manage vector database for RAG
│
│── config/
│   ├── settings.py             # Configuration file
│
│── tests/
│   ├── test_agent.py           # Tests for chatbot
│   ├── test_services.py        # Tests for service integrations
│   ├── test_etl.py             # Tests for ETL and vector DB
│
│── requirements.txt            # Project dependencies
│── README.md                   # Documentation
```

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/agentic-real-estate.git
   cd agentic-real-estate
   ```
2. Create a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate   # On Windows use: venv\Scripts\activate
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Running the Project
Start the FastAPI server:
```bash
uvicorn app.main:app --reload
```
The API will be available at: [http://127.0.0.1:8000](http://127.0.0.1:8000)

## API Endpoints
| Method | Endpoint     | Description          |
|--------|-------------|----------------------|
| POST   | `/chat`     | Chat with the agent |

## Extending the Project
To add a new tool, implement the `ToolAdapter` pattern and register it inside `agents/tools.py`.

## ETL & Vector Database Management
- **Data Ingestion**: Collects real estate data from APIs and other sources.
- **Data Transformation**: Cleans and structures data for AI model consumption.
- **Vector Database**: Stores property descriptions for efficient retrieval in a RAG-based system.

## Contributing
Feel free to fork the repository and submit pull requests!

## License
MIT License © 2025 Your Name

