# Visa Assistant

An assistant that answers questions about German visa documents and shows the source of every answer.

| Folder | What it is | Built in |
| --- | --- | --- |
| `mobile/` | Flutter app | You create it (step 3 below) |
| `api/` | NestJS API | Ready |
| `rag/` | Python FastAPI RAG service | Lesson L20 |
| `docker-compose.yml` | Postgres (with pgvector) + Redis | Ready |

## First-time setup

1. **Database and Redis** (needs Docker Desktop running):
   ```bash
   cp .env.example .env
   docker compose up -d
   ```
2. **API:**
   ```bash
   cd api
   npm install
   npm run start:dev
   ```
   Open http://localhost:3000 — you should see "Hello World!".
3. **Flutter app** (uses your own Flutter version):
   ```bash
   flutter create mobile --org com.shadihasan --platforms ios,android
   ```
4. **Git:**
   ```bash
   git init && git add . && git commit -m "Project setup"
   ```
   Then create an empty repo on GitHub and push to it.

## Working with Claude Code

Open this folder in VS Code and run Claude Code from here, so it sees all three parts.
Start each build with: "Build L[number]'s task. List the design decisions first; I'll choose."
