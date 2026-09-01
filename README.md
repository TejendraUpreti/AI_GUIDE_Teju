# AI Guide — Complete Flow + AI Assistant

## Frontend
Open `index.html` or deploy the root files to GitHub Pages.

## Real AI backend
The included `backend/` keeps the API key off the frontend. Deploy it to a Node hosting service, set `OPENAI_API_KEY` as a secret/environment variable, and expose `POST /api/chat`.

Then either serve the frontend from the same domain or change the fetch URL in `ai.js` from `/api/chat` to your deployed backend URL.

Environment variables:
- `OPENAI_API_KEY` — required
- `OPENAI_MODEL` — optional (set to a model available to your account)
- `PORT` — optional

Run locally:
```bash
cd backend
npm install
OPENAI_API_KEY=your_key npm start
```

The assistant includes chat history in browser localStorage and quick prompts. Do not put an API key in `index.html` or `ai.js`.
