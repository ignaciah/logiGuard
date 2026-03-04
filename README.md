logiguard/
  README.md
  LICENSE
  .gitignore

  agentdesignai_studio/
    system_prompt.txt
    tools_prototype.json
    sample_events.json
    reasoning_tests.md
    output_schema.md

  antigravity/
    agent.yaml
    tools/
      sendEmail.yaml
      httpRequest.yaml
      writeToSheet.yaml
      logEvent.yaml
    events/
      workflow_event.json
    deployment_notes.md

  backend_forwarder/
    index.js
    package.json
    .env.example
    README.md

  demo/
    demoscriptantigravity.md
    pitchscript60s.md
    curl_examples.md
    screenshots/
      aistudiotests.png
      antigravity_console.png
      event_flow.png

  assets/
    architecturediagramprompt.txt
    branding_notes.md
    submission_answers.md
    logo_prompt.txt

  docs/
    architecture_overview.md
    workflow_lifecycle.md
    toolexecutionflow.md
    eventschemareference.md
`

`markdown

LogiGuard — Antigravity AI Workflow Guardian

LogiGuard is a hybrid AI Studio + Antigravity Live Agent that monitors workflow events, interprets them using Gemini reasoning, identifies root causes, and takes action using tools such as email, HTTP callbacks, Sheets, and logging.

It turns noisy logs into clear, actionable narratives and helps workflows become self-healing.

---

Features

- Event-driven Live Agent
- Structured JSON output
- Tool orchestration (email, HTTP, Sheets, logs)
- 30-day agent state retention
- Thin backend forwarder
- AI Studio prompt design + Antigravity runtime
- Judge-ready demo and pitch

---

Architecture

See /docs/architectureoverview.md and /assets/architecturediagram_prompt.txt.

High-level flow:

1. Workflows send JSON events → /backend_forwarder
2. Backend forwards events → Antigravity agent
3. Agent interprets event → produces structured JSON
4. Agent optionally calls tools
5. Event + agent response stored in DB (optional)
6. Demo uses curl + Antigravity console

---

Running Locally

Backend

`bash
cd backend_forwarder
npm install
cp .env.example .env
npm start
`

Trigger events

Use the curl commands in /demo/curl_examples.md.

---

Deploying

- Deploy backend to Cloud Run, Firebase Functions, or Vercel.
- Deploy agent + tools to Antigravity.
- Connect backend to Antigravity endpoint.

---

Demo

See /demo/demoscriptantigravity.md.
