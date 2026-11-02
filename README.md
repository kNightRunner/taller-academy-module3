# Taller Academy — Module 3: Audit Your Own Trail

**Lab:** The Signal System — Audit Your Own Trail  
**Sprint duration:** Two weeks  
**Total effort:** Approximately 80 hours  
**Scope:** Public, sanitized reflection; no client identifiers, internal ticket links, secrets, or proprietary code.

## Exercise 1 — Audit the last completed sprint

### Reconstruction and classification

The inventory below splits the ten initial work categories into twelve separate activities. In particular, the original 14 hours of query work are split into 6 hours of implementation and 8 hours of response-time auditing; the original 8 hours of external-service investigation are split into 5 hours of failure analysis and 3 hours of dependency investigation. **These subdivisions are an estimated allocation for the audit, not independently verified time entries.** The total remains 80 hours.

| # | Activity | Category | Approx. hours | Jira visibility |
|---|---|---|---:|:---:|
| 1 | GraphQL query implementation | feature | 6 | V |
| 2 | GraphQL query response-time audit | investigation | 8 | V |
| 3 | GraphQL mutation implementation | feature | 12 | V |
| 4 | External service failure analysis | investigation | 5 | V |
| 5 | External service dependency investigation | troubleshooting | 3 | V |
| 6 | Bug fixes and integration troubleshooting | bug | 8 | V |
| 7 | Query and mutation validation using Apollo | feature | 8 | V |
| 8 | QA environment validation | bug | 8 | V |
| 9 | Pull request reviews | review | 6 | V |
| 10 | Daily standup meetings | meeting | 5 | V |
| 11 | Other technical meetings | meeting | 5 | V |
| 12 | Jira documentation and progress tracking | documentation | 6 | V |
| | **Total** | | **80** | |

**Visibility definitions:**
- **V (visible):** A record exists and someone outside the immediate team could understand the work and its outcome.
- **P (partial):** A ticket exists, but the result or reasoning is insufficiently documented.
- **X (missing):** No discoverable tracking record exists.

**Audit basis:** I report that all listed activities were documented in Jira. I also checked two representative records in detail (an external-service investigation and a pull request review), and found both contained context and conclusions. This is a self-reported audit; the public repository does not expose client Jira records.

### Coverage by time

- Hours classified V: **80**
- Hours classified P: **0**
- Hours classified X: **0**
- Total hours: **80**

**Estimated coverage by time = (80 / 80) × 100 = 100%.**

The 100% figure reflects my reported assessment of Jira visibility. It is **not** a claim that an external reviewer independently accessed every Jira record.

### Top two signal leak categories

**No P or X categories were identified in this audit.** Therefore there are no two actual leak categories to rank by missing/partial hours (0 hours identified). I will continue checking code reviews, technical meetings, and unplanned investigations, as they are common sources of missing context in engineering teams.

**What a new client manager could conclude I am good at:** Implementing and testing GraphQL integrations, investigating external dependencies, and recording technical work clearly.

**What the record alone might not fully convey:** The broader reasoning behind some technical discussions and how collaboration affects priorities; this is an area to keep evaluating even when Jira entries are complete.

## Exercise 2 — Two record-repair walkthroughs

### Actual audit outcome

I checked two existing Jira records: an external service investigation and a pull request review. Both already contained sufficient context and conclusions. **No real Jira record needed modification (0 actual repairs; 2 records reviewed).**

To demonstrate how I would handle missing or partial signals, the following are **two hypothetical before-and-after repair examples** based on generalized backend work. They are educational samples, not claims that these Jira changes were carried out.

### Simulation A — Repairing an incomplete external-service investigation ticket (P → V)

**Example before — partial ticket:**

> Title: Investigate GraphQL integration error  
> Status: Done  
> Comment: Checked backend issue.

A reader cannot tell which dependency failed, what was investigated, whether the integration is functioning, or who owns the next action.

**Example after — proposed closing comment:**

> **Context:** An external service required by a GraphQL integration returned errors, blocking completion of integration validation.  
> **What I did:** Reproduced the failure, identified the affected request pattern, documented the observable responses, and shared a sanitized summary with the responsible team through the established channels. The fix to the external dependency was outside my scope.  
> **Result:** The issue became actionable for the service owner: the failing interaction, integration impact, and dependency were recorded. The underlying external failure is **not claimed to be resolved**.  
> **Notes for whoever is next:** Confirm the service-owner resolution and rerun the affected integration test in QA before declaring the integration unblocked. Keep internal request details in the restricted Jira ticket.

**Signal repaired in the simulation:** The ticket now distinguishes the investigation outcome from the unresolved external defect and names a clear follow-up. Its hypothetical visibility changes from **P to V**.

### Simulation B — Repairing an unrecorded pull request review (X → V)

**Example before — missing record:**

> A substantive code review took place, but its findings and follow-up were only discussed in a temporary chat thread. The related ticket contains no trace of the review.

**Example after — proposed comment on the related ticket:**

> **Context:** A GraphQL resolver change required review to confirm that response behavior remained compatible with its consumers.  
> **What I did:** Examined resolver behavior, considered duplicate backend calls and edge cases, and recorded review observations for the author. This is a hypothetical example; it does not assert that specific defects were found in the real PR.  
> **Result:** The review and its rationale would become discoverable in the related Jira ticket, allowing the team to see what was assessed and what questions remain.  
> **Notes for whoever is next:** Link the actual PR and its approved or requested changes in the restricted ticket. Confirm tests and any requested follow-ups before closure.

**Signal repaired in the simulation:** A previously invisible review would have a durable, findable record. Its hypothetical visibility changes from **X to V**.

### Evidence boundary

| Measure | Actual sprint audit | Educational repair examples |
| --- | --- | --- |
| Jira records reviewed | 2 | Not applicable |
| Jira records modified | 0 | 0 — examples only |
| Reported sprint coverage | 100% estimated | Not included in real coverage |
| Visibility changes | None required | Illustrative P → V and X → V |

These examples show the **repair method** requested by the lab without inventing missing work, falsifying Jira history, or altering the declared coverage calculation.

## Exercise 3 — One routine, one question

### Four-week commitment

**For the next four weeks I will:** spend **two minutes at the end of each workday** checking whether investigations, code reviews, and technical decisions lasting more than an hour have an appropriate Jira record. **Every Friday**, I will spend **ten minutes** reviewing the week's work and recording outcomes, blockers, and decisions where they are most findable.

### Question to my technical lead

**Question:** “What would you want to be able to see in Jira that you currently cannot?”

**Feedback received:** My technical lead told me that I was already doing a good job documenting and communicating my work. No specific gap was identified in that feedback.

**Action:** Maintain existing documentation quality and periodically recheck whether someone unfamiliar with the work can reconstruct the context, decision, and result.

## Self-check

- [x] Reconstructed the sprint with 12 activity lines and approximately 80 hours.
- [x] Classified Jira visibility and calculated estimated time coverage.
- [x] Reviewed potential leakage, including review work and meetings.
- [x] Verified two high-value Jira records; neither required an actual repair.
- [x] Documented two clearly labeled educational record-repair examples.
- [x] Defined a four-week routine with daily and weekly triggers.
- [x] Asked my technical lead for feedback and documented the response.
- [ ] Independently cross-checked each time allocation against calendar, message, and pull-request history (optional follow-up for greater precision).

**Confidentiality:** This repository contains only generalized descriptions and the author's reported audit findings.
