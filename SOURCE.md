# Data Source and Scenario

**Scenario:** Crypto.com Arena vendor onboarding (designed sourcing and procurement case study)
**Scope:** 370 vendors, 7 onboarding coordinators, one onboarding-status snapshot

Each row is one supplier that services the arena, with an assigned onboarding coordinator, an onboarding status, a critical-supplier flag (whether the arena can open without them), and an annual spend figure.

This is a **constructed scenario**, not a real client engagement. The vendor names, coordinators, spend figures, and statuses were designed to model a realistic arena onboarding effort and to demonstrate the analysis and dashboard method. It contains no real personal or company data.

**Data-quality note:** The raw list began as a deliberately dirty 400-row file containing exact duplicates and fuzzy name variants (the same supplier entered under slightly different names). It was cleaned to 370 unique vendors using Remove Duplicates and Fuzzy Lookup before any analysis. Every number on the dashboard reads from that cleaned list through a live formula engine, so nothing is hardcoded.
