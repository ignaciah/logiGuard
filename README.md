`markdown

LogiGuard — AI Studio Design Environment

This folder contains the design‑time version of the LogiGuard agent.  
AI Studio is used as a safe, flexible environment to prototype reasoning, test event inputs, and refine the agent’s behavior before syncing stable updates to Antigravity.

---

Purpose of This Folder

- Experiment with LogiGuard’s reasoning
- Test workflow events in a controlled environment
- Validate JSON output structure
- Iterate quickly without affecting the production agent
- Keep prompts and test events organized for judges and collaborators

This folder does not contain tools or YAML.  
It is intentionally lightweight so AI Studio never crashes.

---

Files in This Folder

1. system_prompt.txt
The exact prompt you paste into the System Prompt box in AI Studio.  
This version is:
- flexible  
- JSON‑safe  
- tool‑free  
- AI Studio‑friendly  

2. sample_events.json
A collection of ready‑to‑use test events.  
Copy one event at a time into the User Message box in AI Studio.

3. reasoning_tests.md
A checklist of expected behaviors for:
- error events  
- warning events  
- success events  

Use this to verify LogiGuard is behaving correctly.

4. output_schema.md
The JSON contract that LogiGuard must follow in AI Studio.

---

How to Use This Folder in AI Studio

1. Create a new Prompt project
- Open AI Studio  
- Click New → Prompt  
- Name it: LogiGuard (AI Studio)

2. Paste the system prompt
Open system_prompt.txt and paste the entire contents into the System Prompt box.

3. Paste a test event
Open sample_events.json and copy one event into the User Message box.

4. Run and verify
Check that the output matches the structure in output_schema.md.

---

Important Notes

- This prompt is only for AI Studio.  
- Do not paste the Antigravity prompt here — it will crash AI Studio.  
- AI Studio is your design lab, not your production environment.  
- The production prompt lives in antigravity/agent.yaml.

---

Syncing With Antigravity

When you improve LogiGuard’s reasoning in AI Studio:

1. Update system_prompt.txt  
2. Test with sample_events.json  
3. Confirm behavior using reasoning_tests.md  
4. Copy improvements into the Antigravity prompt only when stable

This keeps your production agent predictable and your design environment flexible.

---

Summary

This folder is your clean, stable, judge‑friendly workspace for designing LogiGuard’s intelligence.  
Everything here is optimized for AI Studio’s behavior and avoids the formatting issues that can cause crashes.

`

