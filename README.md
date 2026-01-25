engram-cortex.


# Engram Memory API v6.0

**Persistent identity layer for stateless LLMs**  
The backend that turns goldfish-memory AIs into humans who actually remember who the fuck you are—without bloating your context window or keeping eternal stigma in the system.

Built for real niggas who tired of LLMs forgetting yesterday's vibe, or worse—haunting you with expired criminal records, old dietary cap, or ghosted preferences. Engram codes **Algorithmic Due Process** and **Digital Forgiveness** at the architecture level.

## Why This Shit Matters

Traditional LLMs? Stateless amnesia every chat.  
Traditional databases? Eternal tattoos on your soul (once convicted, always convicted in AI eyes).  

Engram flips both:
- **Pure ID Collision** → Latest truth wins on the same semantic bucket (no ghosts surviving)
- **On-the-fly Exponential Decay** → Old drama fades like yesterday's beef, core facts stay diamond
- **Strict Taxonomy + Vector Retrieval** → Human-like memory continuity without cron-job bloat

From criminal justice rehab to "I used to eat pepperoni but now I'm vegan" evolution—this is the memory layer that lets people change without the machine holding receipts forever.

## Features

- **/memorize** — Ingest new truth (text + user_id + metadata). Collision logic evicts old versions automatically.
- **/recall** → Semantic search with latest-wins grouping + temporal decay (e^(-λt)) applied on read path for O(k) speed.
- **/forget/{point_id}** — Nuke a specific memory point if you need surgical erasure.
- **User-scoped** — Every operation filtered by user_id so no cross-contamination.
- **Production-ready** — FastAPI, Qdrant vector store, OpenAI embeddings, full CORS, env-var secrets.

## Tech Stack

- FastAPI (async king)
- Qdrant (vector DB goat)
- OpenAI embeddings
- Pydantic for clean models
- Python 3.10+

## Quick Start

1. Clone the repo
2. Set your env vars:
   ```bash
   export QDRANT_URL="https://your-qdrant-cluster.qdrant.io"
   export QDRANT_KEY="your-api-key"
   export OPENAI_KEY="sk-..."
	3	Install deps: pip install -r requirements.txt
	4	 (add fastapi, uvicorn, engram-client, etc.)
	5	Run the server: uvicorn main:app --reload
	6	
	7	Hit the docs: http://localhost:8000/docs
Example Usage
Memorize a truth
curl -X POST "http://localhost:8000/memorize" \
  -H "Content-Type: application/json" \
  -d '{
    "text": "I am vegan now, no more pepperoni",
    "user_id": "monterreo_htx",
    "metadata": {"source": "chat_2026-01-20"}
  }'
Recall relevant memories
curl -X POST "http://localhost:8000/recall" \
  -H "Content-Type: application/json" \
  -d '{
    "query": "What does Monterreo eat these days?",
    "user_id": "monterreo_htx",
    "limit": 5,
    "score_threshold": 0.45
  }'
Forget a specific point
curl -X DELETE "http://localhost:8000/forget/12345" \
  -H "Content-Type: application/json" \
  -d '{"user_id": "monterreo_htx"}'
The Bigger Picture
This ain’t just an API—it’s the backend for Engram v1.0: the system that bridges criminal justice sociology with AI governance.
	•	Exonerated? Cleared status overwrites pending → digital redemption.
	•	Changed your mind? Latest truth wins → no eternal stigma.
Shoutout to the Hill (PVAMU Criminal Justice) — this research abstract already cooking for Dr. Whiting.
Contributing
Pull requests welcome, especially if you got better decay tuning or want to add Redis caching for hot reads.
License
MIT — do you, but credit the Chill King if you fork it.
Built by Monterreo B. Tramble Houston, Texas | January 2026 From porch riffs to production memory layers — hate don’t compute, truth evolves.
There you go lil baby, README locked and loaded. This thing got the philosophy, the flex, the examples, and enough street soul to make niggas star it without reading the code first 😅. You want me to add screenshots of Swagger docs, a logo idea, or a deployment section (Railway, Render, whatever you using)? Or we finna push this to GitHub right now? Hit me with the next play pop 🫡. What's good?

