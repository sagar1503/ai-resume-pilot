# Candidate Profile & Anti-Hallucination Rules
# Edit this file to establish your ground-truth career history, verified metrics, and application boundaries.
# The AI agent MUST consult this file before generating any resume, cover letter, or application text.

---

## 1. ANTI-HALLUCINATION POLICY (STRICT)

Every metric, percentage, scale number, tool, and date written into a resume or cover letter must originate from:
1. `CV_Base.tex` (your master resume)
2. The **Verified Metrics Bank** in this file below
3. Explicit confirmation provided by the user in conversation

**NEVER:**
- Invent hypothetical metrics (e.g. "increased throughput by 65%") without backing data.
- Add vague intensifiers like "significantly", "dramatically", "substantially" to disguise missing numbers.
- If a metric is unknown, conservative qualitative impact is preferred, or ask the user:
  > *"Can you confirm approximately how many records/users/hours this affected? I want to make sure every metric on your resume is 100% interview-defensible."*

---

## 2. VERIFIED METRICS BANK (CUSTOMIZE THIS FOR YOUR FIELD)

Add your proven achievements here. When tailoring, the AI selects and reorders from this bank:

### Example Data Engineering / Technical Metrics:
- **Throughput / Volume**: Scaled distributed streaming pipeline to ingest 2.5TB+ daily events with 99.9% uptime.
- **Latency / Performance**: Reduced batch query latency by 45% (from 4 hours to 2.2 hours) through partitioning and cluster tuning.
- **Cost Savings**: Optimized cloud data warehouse spend, saving £32,000 / $45,000 annually in compute instances.
- **Data Quality**: Automated schema validation and anomaly checks, catching 98% of upstream schema drifts before downstream loading.
- **Operational Scale**: Designed self-serve data models used by 60+ analysts and cross-functional teams.

---

## 3. EMPLOYMENT HISTORY (GROUND TRUTH)

List your exact titles, companies, and date boundaries so the AI never alters dates or creates gaps:

| Company | Official / Functional Title | Exact Dates | Key Focus Areas |
|---|---|---|---|
| **Tech Corp / Global Finance** | Senior Data Engineer / Software Engineer | Mar 2023 – Present | Cloud ETL, PySpark, Airflow, Snowflake |
| **Data Solutions Ltd** | Data Engineer / Analytics Engineer | Feb 2021 – Mar 2023 | SQL pipelines, dbt, PostgreSQL, Data modeling |

---

## 4. EDUCATION & CERTIFICATIONS

| Degree / Credential | Institution / Issuer | Dates | Status / Grade |
|---|---|---|---|
| MSc / BSc (e.g. Data Science / CS) | University Name | 2024 – 2025 | Completed / First Class |
| Professional Cloud Architect / DE | AWS / GCP / Azure | 2023 | Active |

---

## 5. WORK AUTHORIZATION & VISA LANGUAGE

Define your exact status phrasing:
- **Recommended standard**: `Right to Work: Full UK work authorisation — no sponsorship required`
- **Rule**: Do not use phrasing that flags visa bureaucracy unless requested. Keep it positive and clear.

---

## 6. JOB FEASIBILITY & DEALBREAKER CRITERIA

Define requirements that should trigger an automatic **SKIP** instead of generating a non-viable CV:

| Requirement Filter | Candidate Status | Action if Mandatory in JD |
|---|---|---|
| **Security Clearance (SC / DV / Top Secret)** | Ineligible (requires 5+ years residency) | SKIP (Log in Tracker) |
| **Foreign Languages** | English (Fluent) only | SKIP if hard requirement |
| **Regional Driving Licence** | Does not hold one | SKIP if role requires car/driving |

---

## 7. COVER LETTER STYLE GUIDELINES

- **Word count**: 280–360 words, 3 to 4 clear paragraphs.
- **Tone**: Professional, direct, human.
- **Ban AI clichés**: Avoid phrases such as:
  - *"At the intersection of..."*
  - *"I thrive in fast-paced environments..."*
  - *"I would welcome the opportunity to discuss..."*
  - *"In today's data-driven world..."*
- **Sign-off**: Use region-appropriate closings (e.g., `Kind regards` in UK/Europe, `Sincerely` in US).

