# DREAM AI experiment — AI access × incentive scheme (design v1)

For Parag. Date 2026-06-18. Status: design draft for discussion.

## What Parag liked (from the call)
- **AI access toggled at the CLASSROOM level** — block ChatGPT / Gemini / Claude (and similar) on school WiFi for some classrooms, allow for others.
- **Toggle different incentive / grading schemes** crossed with that.

So the design is a **2×2 (or 2×k): AI-access {blocked, allowed} × incentive-regime {status quo, alternative}.**

## The core question (the publishable object)
Not "does AI hurt learning" (Bastani 2025 answered the sign: vanilla GPT −17% on unassisted exam). The contribution is:
**Given AI is available, what assessment/incentive regime preserves skill formation?** The interaction — *does the incentive fix matter MORE when AI is accessible?* — is the novel estimand. AI-access is the treatment; the incentive scheme is the policy response a school actually controls.

## The incentive arm: which scheme?
The clean, theory-grounded one (Holmström-Milgrom multitasking):
- **Status quo:** homework-heavy grading (homework is now AI-gameable → a corrupted measure of skill).
- **Alternative:** exam-heavy / proctored-mastery grading (weight shifts to the measure AI can't corrupt).
- Logic: when one task's measure becomes uncheckable, optimal contract mutes incentives on it and loads the verifiable one. The behavioral test: does exam-weighted grading under AI restore *unassisted* proctored mastery?

(NOT the group/pizza-party scheme — that's a separate, riskier paper and likely backfires via Bursztyn-Jensen "hide-effort" / Fryer-Torelli "acting white." Keep it out of this design.)

## ⚠️ The binding constraint: classroom-level = cluster randomization = power problem
Classroom-level assignment means **cluster-randomized**, so you pay the ICC (intra-class correlation) tax. At ~25 kids/class, ICC 0.10–0.20, ANCOVA R²≈0.5:

| Classrooms (total) | Main-effect MDE | Interaction MDE (~2×) |
|---|---|---|
| 24 | ~0.30–0.39 SD | ~0.6–0.8 SD |
| 32 | ~0.26–0.34 SD | ~0.5–0.7 SD |
| 40 | ~0.23–0.30 SD | ~0.5–0.6 SD |
| 60 | ~0.19–0.25 SD | ~0.4–0.5 SD |

DREAM realistically has ~20–50 math classrooms network-wide (grades 3–10, few schools).

**Takeaways:**
- A **MAIN effect** (AI on/off; or grading scheme) is detectable (~0.2–0.35 SD) — Bastani's effect was ~0.3–0.5 SD, so this is in range.
- The **2×2 INTERACTION** — the actual novel contribution — is **likely underpowered** at single-network classroom counts (needs ~0.5 SD to detect; implausibly large).

## The fix: don't randomize access at the classroom level if you can avoid it
Three options, best first:
1. **Student/section-level access randomization within classroom** (if per-account/per-device WiFi blocking is possible on managed Chromebooks). Differences out classroom & teacher effects → no ICC tax → MDE ~0.05–0.12 SD, interaction becomes feasible. **This is the design that works.** Requires: per-ACCOUNT blocking, not just network-wide.
2. **Classroom-level access × within-classroom incentive variation** (hybrid): randomize AI at the room level (where enforcement is natural) but vary incentives within-student across assignments (where power lives). Recovers the interaction on the within-student margin.
3. **Pure classroom-level 2×2** (what was floated): only powered for main effects; pre-register the interaction as exploratory and lean on the within-student item-level panel for the mechanism.

## THE load-bearing feasibility question for DREAM IT
**Can AI domains be blocked per-account / per-device, or only network-wide for the whole building?**
- Per-account → student-level randomization → powered interaction → real paper.
- Network-wide only → everyone in the building is treated identically → no within-school control → forced to classroom-level → underpowered interaction.
This single fact determines whether this is a strong study or a main-effects replication. Ask DREAM IT first.

## Other design notes
- **Leakage defines the estimand, not contaminates it.** Phones on cellular + home use mean you identify the effect of *school-sanctioned* AI access, not total exposure. Measure ambient use by survey in all arms. First stage strongest in MIDDLE school (less LTE/VPN savvy).
- **Outcomes:** unassisted proctored math (the Bastani-style transfer test) + item-level BigQuery panel + state assessments (NY grades 3-8). The proctored-unassisted gap IS the result.
- **Riders (free):** Legenda age-24 consent on treated cohorts; peer-network surveys (for the separate peer-effects paper later); IEP CATE pre-registered.
- **Theory framing (intro only, don't claim to test):** Acemoglu-Kong-Ozdaglar "Knowledge Collapse" (NBER w34910) motivates why AI-substituted effort degrades skill formation. It's a GE/societal claim — cite as motivation, the RCT doesn't test it directly.

## What to take to Parag
1. The clean design is **AI-access × Holmström-Milgrom grading**, interaction = the contribution.
2. **Classroom-level randomization underpowers the interaction** — push for per-account/student-level blocking; that's the make-or-break feasibility ask to DREAM IT.
3. Keep group/peer incentives as a separate later paper (warn: likely backfires as a group prize).
