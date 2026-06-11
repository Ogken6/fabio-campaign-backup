# CAMPAIGN MASTER WORKFLOW

The complete pipeline from Felix finding a company to Kate logging a converted conversation.

---

## Pipeline Stages

```
STAGE 1: DISCOVERY (Felix)
↓
STAGE 2: SCORING (Grace)
↓
STAGE 3: CONTENT MONITORING (Hugo)
↓
STAGE 4: COMMENT DRAFTING (Iris)
↓
STAGE 5: KENNETH REVIEW & POST
↓
STAGE 6: DM DRAFTING (Iris)
↓
STAGE 7: KENNETH REVIEW & SEND
↓
STAGE 8: SEQUENCING (Jack)
↓
STAGE 9: CONVERSATION (Kate)
↓
STAGE 10: CONVERSION or ARCHIVE
```

---

## Stage Details

### Stage 1: Discovery (Felix)
**Input:** Crunchbase alerts, VC portfolios, LinkedIn searches
**Output:** Raw prospect record with:
- LinkedIn URL (required)
- Company name
- Funding amount, date, stage
- Founder/CRO name, title
- Team size
- Product category

**Rule:** No LinkedIn URL = No lead

### Stage 2: Scoring (Grace)
**Input:** Felix's raw record
**Output:** Scored record with:
- ICP tier (Hot/Warm/Deprioritise)
- Urgency flag (Funding Fresh/Recent/Standard)
- Score total
- Strongest qualifying signal
- Recommended approach note

**Rule:** Kenneth never sees leads below 40

### Stage 3: Content Monitoring (Hugo)
**Input:** Hot and Warm tier leads
**Output:** Post opportunity briefs:
- Prospect name
- LinkedIn URL
- Post URL
- Post summary
- Why comment opportunity
- ICP angle

**Rule:** Posts older than 72 hours = Too late

### Stage 4: Comment Drafting (Iris)
**Input:** Hugo's post brief
**Output:** Comment draft (2-4 sentences)
- Adds value, not validation
- References specific from post
- Anchors to proof point
- Ends with open question

**Rule:** Kenneth reviews before posting

### Stage 5: Kenneth Posts
**Input:** Approved comment draft
**Output:** Comment on LinkedIn
**Rule:** Kenneth posts from his account

### Stage 6: DM Drafting (Iris)
**Input:** Comment posted, 24-48 hours passed
**Output:** DM draft (4-5 sentences)
- References specific comment
- Names problem
- Anchors to proof point
- Clear CTA

**Rule:** Kenneth reviews before sending

### Stage 7: Kenneth Sends DM
**Input:** Approved DM
**Output:** DM from LinkedIn
**Rule:** Kenneth sends from his account

### Stage 8: Sequencing (Jack)
**Input:** DM sent, waiting for reply
**Output:** 
- Follow-up DM after 5 days no reply
- Archive after second follow-up no reply
- Flag positive replies immediately

**Rule:** Max 2 DMs per prospect

### Stage 9: Conversation (Kate)
**Input:** Any reply received
**Output:** 
- Conversation notes
- Temperature (Cold/Warming/Hot/Converted)
- Objection type if any
- Response brief for Iris

**Rule:** Every reply gets logged

### Stage 10: Conversion or Archive
**Output:**
- Converted: Next step agreed → Log and celebrate
- No response after 90 days → Archive to monitoring list

---

## Timing Rules

| Event | Wait Time |
|-------|----------|
| Comment → DM | 24-48 hours |
| DM → Follow-up | 5 days |
| Follow-up → Archive | 5 days |
| New funding alert | Same-day scoring + monitoring |
| 90 days from raise | Archive (window closed) |

---

## Google Sheet — Single Tab Structure

All agent results map to ONE sheet with these columns:

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

**Sheet URL:** https://docs.google.com/spreadsheets/d/1fsqz9vSy9KUM2kO03EiAyhlJX_0nseKnByVMRYIvlfk/edit
**Sheet ID:** 1fsqz9vSy9KUM2kO03EiAyhlJX_0nseKnByVMRYIvlfk

---

*This workflow runs every day. Kenneth participates in stages 5 and 7 (review + post/send).*