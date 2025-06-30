## 📋 Codex Tasks for External Knowledge Plugin (Node.js)

### 🔹 Phase 1: Basic Structure and Server

1. **Initialize the Node.js Project**
   - Setup `package.json`.
   - Install dependencies: `express`, `axios`, `dotenv`.
   - Create base `server.js` with Express.

2. **Plugin Routes and Logic**
   - `GET /query?source=&topic=` — fetch article.
   - `GET /recommend?source=&type=` — fetch curated list.
   - `POST /store` — save fetched content.
   - `POST /train` — sync or update knowledge source.


### 🔹 Phase 2: External Source Integration

1. **DevDocs / MDN Integration**
   - Access DevDocs (locally or via API).
   - Filter by topic / keyword.

2. **StackOverflow Integration**
   - Use StackExchange API.
   - Fetch top-rated answers for keyword/topic.

3. **(Optional) GitHub Gists / Trending Snippets**
   - Search & parse code snippets.
   - Filter by language/library/task.


### 🔹 Phase 3: Knowledge Storage

1. **Local Caching / Save Format**
   - Store content in Markdown format.
   - Create `external_index.json` for fast access.

2. **Training Mode**
   - Re-check and refresh from external sources.
   - Remove outdated entries.


### 🔹 Phase 4: Security & Environment

1. **Environment Config**
   - Use `.env` for API keys.
   - Support for StackExchange key, limits.

2. **CORS + Whitelisting**
   - Limit access to Sofia only.
   - Implement usage throttling.


### 🔹 Phase 5: Integration with Sofia

1. **Plugin Integration**
   - Allow Sofia to call plugin methods.
   - Parse and present results in replies.

2. **Output Formatting**
   - Every result should include:
     - Source
     - Timestamp
     - Topic + Summary