# Technology and verification

The server is Flask with Python modules under `core/`. The browser client lives
under `templates/` and `static/`. Retrieval uses Chroma and multilingual sentence
transformer embeddings. Groq provides chat generation and Gemini optionally
screens leaf photographs.

Use the repository virtual environment for Python checks. Start with focused
tests for changed behavior, then run the offline suite documented in `AGENTS.md`.
Keep secrets in process environment settings and keep generated databases,
audio, feedback records, and credentials out of Git.
