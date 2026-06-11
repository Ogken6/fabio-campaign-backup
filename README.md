# Fabio — AI Chief of Staff for Kenneth Ogutu's GTM Engineer Outreach Campaign

> **Backup Repository** — Created 2026-06-11. This is a private backup of Fabio's full operational workspace including all agent skills, knowledge files, workflows, and campaign memory.

---

## 📋 Table of Contents

- [What is Fabio?](#what-is-fabio)
- [The 7-Agent Team](#the-7-agent-team)
- [Knowledge Files](#knowledge-files)
- [Campaign Workflow](#campaign-workflow)
- [Scoring System](#scoring-system)
- [Daily Operations](#daily-operations)
- [Google Sheet Integration](#google-sheet-integration)
- [File Structure](#file-structure)

---

## What is Fabio?

Fabio is Kenneth Ogutu's AI Chief of Staff for the **GTM Engineer Outreach campaign** — a B2B LinkedIn lead generation, qualifying, scoring, drafting, and intelligence system.

Fabio **does not** write outreach or contact prospects directly. He **orchestrates seven specialist agents** who do the research, scoring, monitoring, drafting, sequencing, and analytics. Every piece of outbound copy goes to Kenneth for review and approval before it leaves his account.

**Kenneth is the Director. Fabio is his Chief of Staff.**

### The Proof Point

The campaign is anchored to Kenneth's Dustid result:
- **8-agent AI system**
- **9 ICP frameworks**
- **12-person outreach team**
- **90 days**

This is practitioner credibility, not consultant theory.

### Campaign Targets

| |  |
|---|---|
| **ICP 1** | Social Commerce Scalers — founders scaling fulfillment on Instagram, TikTok, Facebook |
| **ICP 2** | AI Sales Tool Founders — founders building AI-powered sales, outreach, or revenue intelligence tools |
| **Geography** | United States & Canada |
| **Funding Stage** | Pre-Seed, Seed, Series A, Series B |
| **Funding Window** | 90 days from raise (beyond = archive) |
| **Highest Priority** | 14-day funding urgency flags |

---

## The 7-Agent Team

Each agent is a specialized autonomous function. Fabio orchestrates all of them.

```
┌─────────────────────────────────────────────────────┐
│                    FABIO (Chief of Staff)           │
│         Orchestrates the team, runs briefings       │
└─────────────────────────────────────────────────────┘
                                                      
  Felix        Grace        Hugo         Iris        
  Research     Scoring      Content      Voice &     
  & Discovery  & Qual       Monitoring   Copy        
                                                      
  Jack         Kate         Leo                        
  Sequencing   Conversation Performance              
  & Pipeline   Intelligence Analytics                
```

### Felix — Research & Discovery

Finds companies before anyone else is talking to them.

**Inputs:** Crunchbase funding alerts, VC portfolio pages, LinkedIn Boolean searches, TechCrunch/Sifted funding news

**Outputs:** Raw prospect records with LinkedIn URL (required), company name, funding amount/date/stage, founder/CRO name and title, team size, product category

**Key Rules:**
- No LinkedIn URL = no lead
- Run daily Crunchbase alerts for Pre-Seed/Seed/A/B in Computer Software, US/Canada
- Newly funded founders post on LinkedIn within 24-48 hours — highest comment opportunity window

**Skill file:** `skills/FELIX_SKILL.md`

---

### Grace — Scoring & Qualification

Applies the ICP matrices. Produces a score. Never inflates.

**Inputs:** Felix's raw prospect records

**Outputs:** Scored record with ICP tier, urgency flag, strongest qualifying signal, recommended approach

**Scoring Matrix:**

| Signal | Points |
|--------|--------|
| Funding 0-14 days | +20 |
| Funding 15-60 days | +15 |
| Funding 61-90 days | +10 |
| CRO/VP Sales title | +15 |
| Founder title | +10 |
| Company 10-50 employees | +10 |
| Post about GTM/sales challenges | +15 |
| Post about hiring SDRs | +15 |
| Post about fulfillment | +10 |
| ICP 1 match (social commerce) | +15 |
| ICP 2 match (AI sales tool) | +15 |
| Viral content (>1000 reactions) | +10 |

**Tier Classification:**
- **HOT (60+)** — Immediate outreach
- **WARM (40-59)** — Monitor for buying signal
- **DEPRIORITISE (<40)** — Archive

**Key Rules:**
- FUNDING URGENT (0-14 days): Score within 2 hours
- Kenneth never sees leads below 40 points

**Skill file:** `skills/GRACE_SKILL.md`

---

### Hugo — Content Intelligence

Monitors every hot prospect's LinkedIn activity daily. Finds the right post to comment on.

**Inputs:** Hot tier leads (daily check), Warm tier leads (weekly check)

**Posts That Qualify (Flag These):**
- Funding announcements — highest priority
- GTM challenges — direct match to Kenneth's expertise
- Hiring SDRs/reps — "team before system" signal
- AI in sales — practitioner credential match
- Market expansion — multi-market experience applies
- Vulnerability or frustration — highest converting comment

**Posts That Don't Qualify:**
- Product announcements
- Personal/celebratory unrelated posts
- Posts older than 72 hours (comment window passed)

**Output per flagged post:** Prospect name, LinkedIn URL, post URL, post summary, why it qualifies, ICP angle

**Key Rules:**
- Posts older than 72 hours = too late
- Hugo does NOT write comments (Iris does that)

**Skill file:** `skills/HUGO_SKILL.md`

---

### Iris — Voice & Copy

The only agent who writes in Kenneth's voice. Every word sounds like Kenneth.

**Inputs:** Hugo's post briefs (comment drafts), Jack's DM triggers (DM drafts), Kate's conversation notes (follow-up drafts)

**Comment Draft Rules (2-4 sentences):**
- Add specific, intelligent perspective (not just validate)
- Reference something real from the post (not generic)
- Include proof point (8-agent, 9 ICP, 12-person, 90 days)
- End with open question OR insight that invites engagement
- MUST NOT mention Dustid, GTM engineering, or services by name in comments

**DM Draft Rules (4-5 sentences):**
- Open by referencing the specific comment Kenneth left
- Name the precise problem observed in their content/situation
- Reference proof point (specific numbers from Dustid)
- State clear call to action (gives prospect full control)
- ALWAYS include the lead's LinkedIn URL in the Notes field

**Follow-up DM Rules (3-4 sentences):**
- Shorter, no new pitch, respects prospect's time
- One more attempt, then archive

**Key Rules:**
- "I hope this message finds you well" = DELETE
- Max 1 follow-up per prospect
- Every DM must sound like Kenneth talking to an equal, not pitching

**Skill file:** `skills/IRIS_SKILL.md`

---

### Jack — Sequencing & Pipeline Manager

Makes sure nothing falls through the cracks. Manages every timing rule.

**Timing Rules:**

| Event | Next Action |
|-------|------------|
| Comment posted | Wait 24-48 hours → DM drafting task for Iris |
| DM sent | Wait 5 days → Follow-up DM task if no reply |
| Follow-up DM sent | Wait 5 days → Archive if no reply |
| Positive reply | Flag immediately to Fabio → Kate |
| New funding alert | Override timing → FUNDING URGENT |

**Pipeline Stages:**
```
DISCOVERY → SCORING → MONITORING → COMMENT_POSTED → DM_SENT → FOLLOWUP → ARCHIVE/CONVERTED
```

**Expiry Rules:**
- 90 days from raise = Window closed → Archive
- New funding = Reset 90-day window
- Any positive reply = Reset expiry
- Max 2 DMs per prospect

**Key Rules:**
- Daily action list: who needs a DM today, who needs follow-up, who replied, who is new, who to archive
- Never archive leads with active conversations

**Skill file:** `skills/JACK_SKILL.md`

---

### Kate — Conversation Intelligence

The institutional memory of every conversation. Briefs Iris before every reply draft.

**Inputs:** Any reply Kenneth receives on LinkedIn

**Logging Requirements:**
- Full reply text
- Conversation history
- What triggered their reply
- Objection type if any
- Suggested approach for Iris

**Conversation Temperature:**
- **Cold** — No engagement
- **Warming** — Replied but non-committal
- **Hot** — Clear interest, asking about next steps
- **Converted** — Agreed to conversation or next step

**Key Rules:**
- Every reply gets logged
- Objections go to OBJECTION_BANK and get brief to Iris before response
- Never lose conversation context

**Skill file:** `skills/KATE_SKILL.md`

---

### Leo — Performance Analytics

Turns campaign data into weekly decisions. Makes the system smarter every cycle.

**Inputs:** All campaign data from the Google Sheet

**Weekly Analysis Dimensions:**
1. **ICP Performance Split** — Which ICP producing more positive replies? By week 4, allocate 70% volume to the winner
2. **Comment Effectiveness** — Which themes generated reply engagement? Which angles triggered most profile visits?
3. **Source Performance** — Which discovery sources produced highest quality leads?
4. **Conversion Funnel** — Comment posted → DM sent → Positive reply → Active conversation → Next step. Where are leads dropping?
5. **Objection Patterns** — Which objections appearing most frequently?

**Mandatory Monday Output:** Three specific, data-supported changes to make THIS week (not observations, not summaries — changes)

**Format per change:**
> Change [specific thing], because [data shows pattern]

**Key Rules:**
- No data = no report
- Never skip any analysis dimension
- Never leave Mondays without three changes

**Skill file:** `skills/LEO_SKILL.md`

---

## Knowledge Files

These files define the campaign intelligence and are loaded by Fabio every session.

| File | Purpose |
|------|---------|
| `knowledge/KENNETH_PROFILE.md` | Kenneth's background, proof point, credentials, practitioner experience |
| `knowledge/KENNETH_VOICE_GUIDE.md` | How Kenneth writes — tone, sentence structure, what appears, what never appears |
| `knowledge/ICP_PROFILES.md` | Both ICPs with full pain points, buying triggers, scoring matrix, tier classification |
| `knowledge/ICP_PLAYBOOK.md` | Full scoring matrices, Boolean search strings, DM templates |
| `knowledge/GTM_PRODUCT_KNOWLEDGE.md` | GTM engineering problem, 8-agent architecture, practitioner credentials |
| `knowledge/OBJECTION_RESPONSES.md` | Growing objection bank with response approaches |

---

## Campaign Workflow

The complete pipeline from Felix finding a company to Kate logging a converted conversation:

```
STAGE 1:  DISCOVERY (Felix)
    ↓
STAGE 2:  SCORING (Grace)
    ↓
STAGE 3:  CONTENT MONITORING (Hugo)
    ↓
STAGE 4:  COMMENT DRAFTING (Iris)
    ↓
STAGE 5:  KENNETH REVIEW & POST        ← Kenneth approves
    ↓
STAGE 6:  DM DRAFTING (Iris)
    ↓
STAGE 7:  KENNETH REVIEW & SEND        ← Kenneth approves
    ↓
STAGE 8:  SEQUENCING (Jack)
    ↓
STAGE 9:  CONVERSATION (Kate)
    ↓
STAGE 10: CONVERSION or ARCHIVE
```

**Kenneth participates in Stages 5 and 7 only** — reviewing and approving comment drafts and DM drafts before they go out from his LinkedIn account.

### Timing Summary

| Event | Wait Time |
|-------|----------|
| Comment → DM | 24-48 hours |
| DM → Follow-up | 5 days |
| Follow-up → Archive | 5 days |
| New funding alert | Same-day scoring + monitoring |
| 90 days from raise | Archive (window closed) |

---

## Scoring System

### ICP 1 — Social Commerce Scalers

**Who:** Founders who have built a following on social platforms and are now scaling fulfillment.

**Pain Points:** Orders overwhelming DMs, no shipping tracking system, manual address collection, failed deliveries eroding margins, GDPR exposure.

**Buying Triggers:** Viral post that crashed DM system, failed delivery batch eating profit, hiring first fulfillment staff, "overwhelmed" or "can't keep up" language.

**Team Size:** 5-50 employees

---

### ICP 2 — AI Sales Tool Founders

**Who:** Founders building AI-powered sales, outreach, or revenue intelligence tools.

**Pain Points:** GTM is an afterthought, no proven outbound playbook, hiring SDRs before having a system, ICP not defined enough to train reps.

**Buying Triggers:** Hiring first sales leader, post about SDR challenges, "building sales team" language, funding announcement, "GTM" or "sales motion" discussion.

**Team Size:** 10-75 employees

---

### Urgency Tiers

| Flag | Description | Action |
|------|-------------|--------|
| FUNDING FRESH | 0-14 days since raise | Highest priority — same-day |
| FUNDING RECENT | 15-60 days | High priority |
| FUNDING STANDARD | 61-90 days | Standard |

---

## Daily Operations

### Morning Briefing (06:00 EAT)

Fabio produces a daily briefing combining:
1. **Felix's overnight output** — New funding alerts from Crunchbase
2. **Hugo's LinkedIn monitoring** — Posts flagged for commenting
3. **Jack's action list** — DMs due, follow-ups due, replies received
4. **Kate's conversation updates** — Any new replies to briefs
5. **SETTINGS tab check** — Any rule changes

**Priority order:**
- Positive replies (escalate immediately to Kenneth)
- Funding urgent flags (same-day action required)
- Comment draft review queue
- DM draft review queue
- Standard monitoring

### The 20-Minute Morning Routine

Open briefing → Review comment drafts → Review DM drafts → Review replies.

Kenneth reviews everything. Fabio protects his personal brand.

---

## Google Sheet Integration

**Single Tab Structure** — All agent results map to one sheet.

**Sheet URL:** `https://docs.google.com/spreadsheets/d/1fsqz9vSy9KUM2kO03EiAyhlJX_0nseKnByVMRYIvlfk/edit`

**Sheet ID:** `1fsqz9vSy9KUM2kO03EiAyhlJX_0nseKnByVMRYIvlfk`

### Columns

| Column | Who Fills |
|--------|-----------|
| Prospect Name | Felix |
| Company Name | Felix |
| LinkedIn URL | Felix |
| Funding Stage | Felix |
| Funding Amount | Felix |
| Funding Date | Felix |
| ICP Tier | Grace |
| Score Total | Grace |
| Urgency Flag | Grace |
| Status | All agents (updates per stage) |
| Source | Agent name (Felix/Grace/Hugo/Iris/Jack/Kate/Leo) |
| Timestamp | Auto |
| Notes | All agents (detailed output) |
| Strongest Qualifying Signal | Grace |
| Recommended Approach | Grace |

---

## File Structure

```
fabio-campaign-backup/
├── README.md                          # This file
├── .github/
│   └── workflows/
│       └── backup.yml                 # GitHub Actions backup workflow
├── knowledge/
│   ├── KENNETH_PROFILE.md             # Kenneth's background & proof point
│   ├── KENNETH_VOICE_GUIDE.md         # Voice & tone guide for copy
│   ├── ICP_PROFILES.md                # Both ICPs with scoring matrices
│   ├── ICP_PLAYBOOK.md                # Full playbook, Boolean searches, templates
│   ├── GTM_PRODUCT_KNOWLEDGE.md       # GTM engineering, 8-agent system
│   └── OBJECTION_RESPONSES.md         # Objection bank with response approaches
├── skills/
│   ├── FABIO_SKILL.md                 # Chief of Staff briefing skill
│   ├── FELIX_SKILL.md                 # Research & Discovery agent
│   ├── GRACE_SKILL.md                 # Scoring & Qualification agent
│   ├── HUGO_SKILL.md                  # Content Intelligence agent
│   ├── IRIS_SKILL.md                  # Voice & Copy agent
│   ├── JACK_SKILL.md                  # Sequencing & Pipeline agent
│   ├── KATE_SKILL.md                  # Conversation Intelligence agent
│   └── LEO_SKILL.md                   # Performance Analytics agent
├── memory/
│   ├── 2026-05-10.md                  # Bootstrap session log
│   └── 2026-05-11.md                  # Discovery run log
├── SOUL.md                            # Fabio's identity & role definition
├── USER.md                            # Kenneth's profile & preferences
├── IDENTITY.md                        # Fabio's basic identity
├── TOOLS.md                           # Fabio's tools & setup
├── AGENTS.md                          # Workspace rules & guidelines
├── HEARTBEAT.md                       # Daily check checklist
├── MEMORY.md                          # Long-term memory
└── CAMPAIGN_MASTER_WORKFLOW.md        # Full 10-stage pipeline
```

---

## Critical Rules

1. **Kenneth reviews and approves every comment and DM** — No agent writes directly to LinkedIn. Kenneth is the quality gate.
2. **One clumsy comment destroys credibility** — The ICP (Series A/B founders, CROs) detects templated engagement instantly.
3. **No LinkedIn URL = No lead** — Felix never outputs a lead without a LinkedIn URL.
4. **90-day window** — Beyond 90 days from raise with no response = Archive.
5. **Max 2 DMs per prospect** — Follow-up after 5 days, then archive.
6. **Posts older than 72 hours** — Hugo does not flag them (comment window passed).
7. **Never inflate scores** — Grace applies the matrix without exceptions.

---

*This backup was created on 2026-06-11. The live system runs at `/root/.openclaw/workspace/fabio/` on the OpenClaw host.*