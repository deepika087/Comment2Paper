# Comment2Paper
Comment2Paper is an intelligent agent workflow that bridges the gap between YouTube audience requests and academic research. It scrapes community comments, filters for specific learning requests using NLP, and automatically retrieves relevant peer-reviewed papers from ArXiv to jumpstart the content creation process.

# What do you mean by Agent workflow? 
At no point have I explicitly told the Agent what tool/function to invoke. It is all driven by GOAL_PROMPT

# what do you need in order to run it? 
Youtube API key + OAuth Access token <- Place holder at the very first box.  
Open AI key
No token is required for Arxiv

# 🛠️ How It Works
The pipeline utilizes a multi-stage Agentic workflow:

Extraction: Scrapes metadata and comments from top-performing videos in a specific niche via the YouTube Data API.

Intent Classification: An LLM-powered agent filters comments to isolate "User Asks" and specific technical queries (e.g., "Explain Corrective RAG").

Synthesis: The agent clusters these requests into broad research themes.

Academic Retrieval: The system generates optimized search queries for the ArXiv API, returning a curated list of research papers to serve as the foundation for the next video script.

# 🧰 Tech Stack
Language: Python 3.10+

Orchestration: LangChain

LLM: GPT-4o

APIs: YouTube Data API v3, ArXiv API

Data Handling: Mostly JSON
