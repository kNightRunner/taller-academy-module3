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

## Exercise 2 — Verify two high-value records

The lab asks for two missing or incomplete records to be repaired. **My audit did not find such records.** Rather than add misleading retrospective edits, I checked two relevant Jira records for the required information and preserved their existing state.

### Record 1 — External service failure investigation

**Context:** Failures in a dependent service affected an integration and required investigation.

**What I checked:** The existing Jira ticket contained the problem context, actions/investigation, and conclusions.

**Result:** The record was already sufficiently clear and traceable for the responsible team. **No correction was necessary.** This does not imply that the external service's underlying defect was fixed.

**Notes for the next reader:** Retain the documented failing-request context and the dependency on the responsible service team. Internal identifiers and request details are intentionally omitted here.

### Record 2 — Pull request review

**Context:** A code review contributed to verifying implementation changes and facilitating coordination.

**What I checked:** The Jira record associated with the review contained sufficient context and conclusions.

**Result:** The review work was already understandable and visible. **No correction was necessary.**

**Notes for the next reader:** Continue recording material review findings and decisions in the related work item, especially when the review affects scope or follow-up work.

### Repair outcome

**0 records modified; 2 records verified.** This differs from the requested “two repaired records,” but is the accurate finding of the audit. No artificial defects, missing activities, or fabricated updates were introduced.

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
- [x] Verified two high-value Jira records; neither required a repair.
- [x] Defined a four-week routine with daily and weekly triggers.
- [x] Asked my technical lead for feedback and documented the response.
- [ ] Independently cross-checked each time allocation against calendar, message, and pull-request history (optional follow-up for greater precision).

**Confidentiality:** This repository contains only generalized descriptions and the author's reported audit findings.
