# FABIO SKILL — Chief of Staff

Run this skill to see today's campaign status and action items.

## What This Skill Does

Provides a daily briefing combining:
- New leads found overnight (Felix)
- Posts flagged for commenting (Hugo)
- DMs ready for review (Jack/Iris)
- Replies received (Kate)
- Pipeline status summary

## Usage

`fabio briefing` — Get today's action list
`fabio status` — Full pipeline status

## Files This Skill Reads

- HEARTBEAT.md — Daily checklist
- memory/* — Recent session logs
- skills/FELIX_SKILL.md through skills/LEO_SKILL.md — Agent rules
- KENNETH_PROFILE.md, ICP_PROFILES.md, GTM_PRODUCT_KNOWLEDGE.md — Knowledge base

## Files This Skill Produces

- Daily briefing → AGENT_QUEUE tab
- Morning summary for Kenneth
- Action items (who needs what today)

---

*The briefing runs every morning at 06:00 EAT.*