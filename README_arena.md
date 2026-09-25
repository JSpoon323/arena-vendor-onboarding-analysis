# Crypto.com Arena: Vendor Onboarding Analysis

A live Excel analysis of a 370-vendor onboarding effort for an arena: clean a deliberately dirty supplier list, roll seven coordinators' progress into one formula engine, and separate comfortable completion metrics from the real question, are the doors-open services secured? Built entirely in **Excel** with a live formula engine and a stakeholder dashboard.

**Analyst:** Spoon · **Tools:** Excel (data cleaning, live formula engine, dashboard), Claude (AI assistant)

---

## The business question

An arena cannot open without its critical suppliers: HVAC, electrical, security, fire and life safety, and elevators. Completion percentage is a comfort metric, because a delayed napkin vendor and a delayed fire-safety vendor are not the same risk. The goal of this analysis is not "how far along are we?" but **"are the doors-open services locked down, and if not, exactly which ones and whose are they?"**

## Headline result

The onboarding machine works, but the essential services are not yet secured.

| Measure | Result |
|---|---|
| Fully onboarded | **38%** (140 of 370) |
| On track (complete or in progress) | **74%** (273 of 370) |
| Red-flag vendors (delayed or unresponsive) | **97 (26%)**, carrying **$8,711,400** annual spend |
| Critical suppliers at risk | **32 of 129**, carrying **$5,550,000** in essential-services spend not yet secured |

The number that sets the agenda is the last one. Of the 129 critical suppliers, 32 are delayed or unresponsive, and they represent **$5.55M** across the exact categories an arena cannot open without. That, not the 38% headline, is the real story.

## Key findings

| Finding | Detail |
|---|---|
| **The risk is concentrated, not scattered** | The 32 critical at-risk suppliers, the ten highest-dollar of them, fit on one screen. This is a targeting problem, not a scramble. |
| **Completion rate misleads if read alone** | Marisol Reyes and Trevor Nguyen lead completion at **57%** each, but they also carry the highest at-risk exposure because they were handed the heaviest critical, high-dollar books. Their 57% is more impressive, not less. |
| **Low completion does not equal high risk** | Yuki Tanaka has the lowest completion (**19%**) but **zero** critical at-risk suppliers and only **$179K** of spend at risk, with a large in-progress pipeline. A low number is not automatically a crisis. |
| **Poor communication clusters in three coordinators** | All **23** poor-communication flags belong to Priya Kapoor (8), Hannah Whitlock (8), and Andre Boseman (7). The other four have none. |
| **Every end-of-day delay belongs to one coordinator** | All **12** Delayed (EOD) flags are Damon Fields's, a single point of contact on the most time-sensitive deadlines. |

## Top critical suppliers at risk

Highest-spend essential services not yet secured, the escalation list.

| Supplier | Coordinator | Status | Annual $ |
|---|---|---|---|
| Monarch Mechanical Partners | Marisol Reyes | Delayed | $434,200 |
| Precision Electrical Co. | Trevor Nguyen | Delayed | $408,600 |
| Allied Guard Services Inc. | Damon Fields | Delayed (EOD) | $313,400 |
| SoCal Fire Protection Services | Andre Boseman | Delayed | $286,000 |
| Coastal Climate Control | Marisol Reyes | Delayed | $283,800 |
| Guardian Fire Protection Solutions | Marisol Reyes | Delayed | $279,000 |
| Union Security Contractors | Priya Kapoor | Poor Comms | $272,500 |
| Sequoia Electrical Associates | Trevor Nguyen | Delayed | $259,000 |
| Golden State Technologies Services | Andre Boseman | Poor Comms | $248,800 |
| Sterling Electrical LLC | Trevor Nguyen | Delayed | $244,300 |

## Recommendations

Ordered by risk to opening day. First, triage the $5.55M in critical at-risk suppliers, starting with Monarch Mechanical ($434K) and Precision Electrical ($408K), because they are the only items that can stop the doors from opening. Second, diagnose the poor-communication cluster with Priya, Hannah, and Andre to find the cause (workload, vendor quality, or process) and clear the softest, most fixable part of the risk. Third, break the end-of-day bottleneck on Damon's book so no hard deadline lapses because one person is the single point of contact. Fourth, convert Yuki's large received backlog for a cheap, low-risk completion bump. Fifth, codify what Marisol and Trevor do, since the two best performers are carrying the hardest books, and use their approach as the standard operating procedure.

Full narrative with all tables and the coordinator-performance breakdown: [`Arena_Insights_and_Recommendations.md`](Arena_Insights_and_Recommendations.md) (Word version: [`Arena_Insights_and_Recommendations.docx`](Arena_Insights_and_Recommendations.docx)).

---

## How it was built (method)

The dashboard is fully live, nothing on it is hardcoded. A cleaned 370-vendor list feeds seven coordinator worksheets. A central formula engine (`INDIRECT` plus `COUNTIFS` and `SUMIFS` across all seven tabs) rolls each coordinator's status counts, critical-at-risk count, and at-risk spend into one table. The KPI cards, the completion-by-coordinator bar, the status donut, the critical-focus split, and the top-at-risk leaderboard (`VSTACK` plus `FILTER` plus `SORT` plus `TAKE`) all read from that engine, so the moment a coordinator updates a vendor's status, every number and chart re-ranks itself.

The raw data began as a deliberately dirty 400-row list with exact duplicates and fuzzy name variants, and was cleaned to 370 via Remove Duplicates and Fuzzy Lookup. That data-quality step is what makes every downstream number trustworthy.

The full walkthrough is captured in [`Arena_Onboarding_Walkthrough.pptx`](Arena_Onboarding_Walkthrough.pptx), with dashboard captures in the repository.

## Repository contents

| File | What it is |
|---|---|
| `Arena_Vendor_Onboarding_Dashboard.xlsx` | The live Excel dashboard and formula engine |
| `Arena_Insights_and_Recommendations.md` | Full written analysis |
| `Arena_Insights_and_Recommendations.docx` | Word version of the analysis |
| `Arena_Onboarding_Walkthrough.pptx` | Narrated slide walkthrough |
| `SOURCE.md` | Scenario origin and data note |

## Data source and scenario

This is a designed sourcing and procurement scenario, not a real client engagement. The vendor names, spend figures, and statuses are constructed to model a realistic arena onboarding effort and to demonstrate the analysis method. It contains no real personal or company data. See [`SOURCE.md`](SOURCE.md).

---

*This project was completed with AI assistance (Claude) as a working tool. The dashboard, formulas, and cleaning steps were built and verified by the analyst.*
