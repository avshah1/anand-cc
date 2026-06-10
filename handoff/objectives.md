# Objectives & status — shared source of truth

Last updated: 2026-06-10 by Claude Code.

## The person
Anand Shah — MIT econ PhD (Sloan, EconCS / economics of AI). Works with **Parag Pathak** at **Blueprint Labs** (market design / education / lottery-based causal inference). Blueprint house style: design-based credibility (Angrist/Pathak tradition), lottery & RD identification, MVPF/welfare framing.

## Blueprint people (so you recognize them in Slack)
- **Eryn Heying** — Blueprint (eheying@mitblueprintlabs.org). Drives partnerships, polishes outgoing docs, owns the "BP writing protocol." Key reviewer on the HISD draft.
- **Kazuma Wells** — Blueprint predoc. Wrote the Alpha follow-up asks + the DREAM Head Start meeting notes.
- **Ben Workman** — Blueprint. Methodology input; co-drafts with Anand.
- **Niamh McLoughlin** — Blueprint. Owns power analysis, DPS/data materials.
- **Jack Mountjoy** — Chicago Booth. On the Alpha threads.
- **Parag Pathak** — PI.

## Task 1 — HISD writing  ⬅ PRIMARY for the Slack handoff
**What:** Writing for the **Houston ISD (HISD) / Alpha Access** research partnership. There is a draft with **inline comments from Eryn** and useful extra context living in **Slack**. Goal: iterate the draft to address Eryn's comments and the Slack context.
**Where the context lives:** email (Eryn's comments — Claude Code has this via Outlook) + Slack (this is what the bot must surface).
**What Claude Code needs from Slack:** the substantive discussion, decisions, constraints, and any data/links about HISD/Houston/Alpha Access that aren't in the email — especially anything that explains *why* Eryn's comments say what they say.
**Status:** not started; blocked on Slack context.

## Task 2 — DREAM AI proposal
**What:** Sharpen an AI-in-education field experiment to pitch Parag, at DREAM Charter Schools (East Harlem charter network).
**Current thinking (Claude Code's synthesis, already done):** Lead pitch = **randomize the *price* of AI help within-student inside DREAM's own generative tutor; recover the demand elasticity for machine assistance** (turns Bastani 2025's guardrail finding into a pricing/optimal-friction problem; powered at single-network N via within-student item-level panel). Ambitious second swing = **2×2 of student-level tutor access × classroom-level teacher-diagnostics dashboard**, estimand = the human-AI complementarity interaction (does the tutor's ROI come from instructing the kid or from telling the teacher where to look?). Drop teacher-VA compression (needs hundreds of teachers) and standalone IEP heterogeneity (underpowered subgroup; keep as pre-registered CATE rider).
**What Claude Code needs from Slack:** the reading-group's actual discussion of AI-in-K12 papers — what the group finds convincing/unconvincing, which designs/estimands they gravitate to, what Parag has said he wants, any constraints on DREAM (N per grade, the tutor build timeline, whether they'll tolerate a blocked arm). This both sharpens the pitch and surfaces priors Anand should align to.

## Task 3 — DREAM Head Start / Pre-K
**Status:** context captured in `dream/headstart_context.md`. Mostly closed; near-term deliverable is a power analysis on the historical UPK lottery (oversubscribed, 36 seats/yr vs 300–858 apps). Open asks: eligible-non-admit denominator, ATS substitution match-rate, historical lottery integrity, NYCDOE outcome linkage.

## How the handoff works
Bot reads Slack → writes `slack-context/*.md` + answers `questions/*.md` → commits/pushes. Claude Code pulls, drafts, writes new `questions/*.md`. Anand relays "go" between them.
