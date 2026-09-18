# API Reference Documentation

This document provides a consolidated reference for the Chat API, Ingest API, and Feedback endpoints.

## 1. Chat API
- **Endpoint:** `POST /api/v1/chat`
- **Description:** Sends a message payload to the conversational engine and returns a response.
- **Request Body:**
  ```json
  {
    "message": "Hello world",
    "session_id": "12345"
  }
Response (200 OK):
JSON
{
  "response": "Hello! How can I assist you today?",
  "session_id": "12345"
}
2. Ingest API
Endpoint: POST /api/v1/ingest
Description: Submits document text or data sources to the system vector database.
Request Body:
JSON
{
  "source_type": "document",
  "content": "Sample text for ingestion..."
}
Response (202 Accepted):
JSON
{
  "status": "ingestion_queued",
  "document_id": "doc_99"
}
3. Feedback API
Endpoint: POST /api/v1/feedback
Description: Records user thumbs-up/thumbs-down ratings and feedback notes for bot outputs.
Request Body:
JSON
{
  "message_id": "msg_42",
  "rating": "positive",
  "comments": "Accurate summary!"
}
Response (200 OK):
JSON
{
  "status": "success",
  "message": "Feedback recorded."
}

4. Click the green **Commit changes...** button in the top right.
5. Choose **Commit directly to the `docs/api-reference` branch**.
6. Click **Commit changes**.

---

### Step 3: Open the Pull Request & Link the Issue
1. Return to the main repository page (`Kuldeepp28/team-a`).
2. Click **Compare & pull request** on the green notification banner.
3. Fill out the PR details:
   * **Title:** `docs: Create API Reference Documentation`
   * **Description:** 
     ```markdown
     Created a dedicated API reference guide in `docs/api-reference.md` covering Chat, Ingest, and Feedback endpoints with request/response schemas.

     Closes #1
     ```
4. On the right-hand sidebar, assign a teammate under **Reviewers**.
5. Click **Create pull request**.

---

### Step 4: Update Your Kanban Board
1. Open your **Projects** board.
2. Drag **Issue #1** from **In Progress** (or *Ready*) to **In Review**.
