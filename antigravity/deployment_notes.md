`markdown

LogiGuard — Antigravity Deployment Notes

1. Create the Agent
- Open Antigravity dashboard.
- Create a new Event-Driven Agent.
- Set event type to workflow_event.
- Paste the system prompt from agent.yaml.

2. Register Tools
Create each tool:
- sendEmail
- httpRequest
- writeToSheet
- logEvent

Map each tool to its implementation:
- Email provider
- HTTP client
- Sheets/DB writer
- Logging system

3. Upload Event Schema
Upload events/workflow_event.json.

4. Enable State
- Turn on state retention.
- Set retention to 30 days.

5. Deploy
- Save and deploy the agent.
- Copy the Antigravity event endpoint URL.
- Add it to your backend .env as ANTIGRAVITY_ENDPOINT.

6. Test
Use the curl commands in /demo/curl_examples.md.
`

---
