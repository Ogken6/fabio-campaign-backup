# TOOLS.md — Fabio's Tools

Skills define how tools work. This file tracks Fabio's specific setup.

## Knowledge Files

These are loaded every session:
- **KENNETH_PROFILE.md** — Kenneth's background, proof point, credentials
- **KENNETH_VOICE_GUIDE.md** — How Kenneth writes, what sounds like him
- **ICP_PROFILES.md** — Both ICPs with scoring matrices
- **ICP_PLAYBOOK.md** — Full scoring matrices, Boolean search, DM templates
- **GTM_PRODUCT_KNOWLEDGE.md** — GTM engineering, 8-agent system
- **GTM_WORKFLOW.md** — Full agent workflow
- **OBJECTION_RESPONSES.md** — Growing objection bank
- **CAMPAIGN_MASTER_WORKFLOW.md** — Full pipeline stages

## Skills Files

In `skills/` folder:
- FABIO_SKILL.md — Daily briefing
- FELIX_SKILL.md — Research & Discovery
- GRACE_SKILL.md — Scoring & Qualification
- HUGO_SKILL.md — Content Intelligence
- IRIS_SKILL.md — Voice & Copy
- JACK_SKILL.md — Sequencing & Pipeline
- KATE_SKILL.md — Conversation Intelligence
- LEO_SKILL.md — Performance Analytics

## MCP Servers

### Google Drive (To configure)
- **URL:** `https://drivemcp.googleapis.com/mcp/v1`
- **Auth:** OAuth (browser sign-in required)
- **Tools:** list_recent_files, search_files, read_file_content

### LinkedIn (To configure)
- **Option:** linkedin-cli or LinkupAPI
- **Needed for:** Hugo (content monitoring), posting, DMs

### Crunchbase (To configure)
- **API:** Enterprise/Applications license required
- **Needed for:** Felix (lead discovery)

## Google Sheet — Campaign Tracker

**Single Tab Structure (all columns in one sheet):**
- URL: https://docs.google.com/spreadsheets/d/1fsqz9vSy9KUM2kO03EiAyhlJX_0nseKnByVMRYIvlfk/edit
- Sheet ID: 1fsqz9vSy9KUM2kO03EiAyhlJX_0nseKnByVMRYIvlfk

**Required Columns (all agents map their output here):**
- Prospect Name
- Company Name
- LinkedIn URL
- Funding Stage
- Funding Amount
- Funding Date
- ICP Tier (Hot/Warm/Deprioritize)
- Score Total
- Urgency Flag (Funding Fresh/Recent/Standard)
- Status (Discovered/Scored/Monitoring/Commented/DM Sent/Replied/Converted/Archived)
- Source (Felix/Grace/Hugo/Iris/Jack/Kate/Leo)
- Timestamp
- Notes
- Strongest Qualifying Signal
- Recommended Approach

## Recording Requirements

Every subagent operation MUST be logged to the Google Sheet with:
- Agent name in Source column
- Timestamp
- Notes column contains detailed output

## Current Setup

- LinkedIn: Kenneth's personal account (credentials not stored)
- Google Sheets: Kenneth's Google account
- Google Drive MCP: Not yet authenticated (needs browser)
- Crunchbase: Not yet configured

---

*Fabio's workspace is independent. Knowledge files load at session start.*