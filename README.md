# 🗺️ Agentic AI Trip Planner

An intelligent, local-first trip planning assistant powered by agentic AI. This project uses a Groq-hosted LLM, LangGraph, and modular tools (place search, weather, currency, cost calculator) to generate personalized travel itineraries in real time.

## Features

- **Agentic Workflow**: Uses LangGraph to build an intelligent agent that selects and invokes tools based on user queries.
- **Modular Tooling**: Includes tools for place search, weather info, cost estimation, and currency conversion.
- **Frontend**: Simple UI built with Streamlit.
- **Backend**: FastAPI-based API for trip planning queries.
- **Runs Locally**: No cloud deployment required (except for third-party APIs).

## Tech Stack

- **LLM**: Groq-hosted Llama2
- **Frameworks**: LangChain, LangGraph
- **Backend**: FastAPI
- **Frontend**: Streamlit
- **Utilities**: Pydantic, HTTPX, dotenv, Request

## Running the App

1. Create a `.env` file with your API keys (Groq, Google Places, OpenWeather, etc.).

2. Start the FastAPI backend:

```bash
uvicorn main:app --reload
```
### Run the Streamlit frontend (optional):

```bash
streamlit run streamlit_app.py
```
## Sample Query

Send a POST request to the /query endpoint with a question like:
```bash
{
  "question": "Plan a 3-day trip to Tokyo including weather and estimated cost"
}
```
