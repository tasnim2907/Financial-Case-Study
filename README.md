# Financial-Case-Study

## Overview

This repository includes SQL case study within two practical domains—**Insurance** and **Banking**—and strengthen core SQL concepts such as aggregation, filtering, joins, subqueries (including correlated subqueries), and conditional logic. Each scenario mirrors real stakeholder questions (claims, premiums, agent performance, customer onboarding, transaction flows, and branch KPIs).

## Key Features

* Domain-focused exercises across **Insurance** and **Banking**, mirroring real reporting and analytics tasks.
* Clear mapping from business questions to SQL solutions using joins, grouping, subqueries, and conditional aggregation.
* Examples of `CASE`, `GROUP BY`, and date filtering for period analyses (e.g., year-specific onboarding).
* Simple, relational table designs (customers, policies, claims, agents, branches, accounts, transactions) to keep the focus on SQL reasoning.
* Queries written to be portable across PostgreSQL and MySQL with minor syntax adjustments where needed.

## Dataset

The repository includes two small relational schemas. Each is intentionally compact to emphasize query logic over data volume.

### Insurance Dataset

* **customers** — Customer profile (full_name, email, city, signup_date).
* **policies** — Policy metadata (policy_id, policy_type, premium_amount, customer_id, agent_id).
* **claims** — Claims tied to policies (claim_id, policy_id, status, claim_date).
* **agents** — Agent roster (agent_id, full_name).

### Banking Dataset

* **branches** — Branch info (branch_id, name).
* **accounts** — Accounts linked to branches (account_id, branch_id, status).
* **transactions** — Ledger of activity (transaction_id, account_id, txn_type, amount, txn_date).
* **customers** — Customer profile (full_name, email, signup_date) for onboarding analysis.

## How to Use

1. **Clone** this repository.
2. **Load schema and sample data** into your SQL environment (PostgreSQL or MySQL).
3. **Run the domain-specific queries** in the `insurance/` and `banking/` folders that correspond to the business questions.
4. **Adapt to your SQL engine** as needed.
5. **Extend** the queries by adding filters (e.g., current year, month-to-date), ranking (e.g., top branches/agents), or subqueries (e.g., compare against global averages) to deepen analysis.

## Insights You Can Find

* **Insurance analytics:**

  * Rapid customer outreach by city (e.g., Toronto), enabling targeted claims follow-ups.
  * Revenue mix by **policy_type**, helping finance evaluate product performance and shifts over time.
  * **Agent performance** via end-to-end join paths (agent → policy → claim) with conditional approval metrics.

* **Banking analytics:**

  * **New customer onboarding** by year to inform growth and marketing activities.
  * Cash flow distribution by **txn_type** to spotlight drivers of balance movements and fees.
  * **Branch-level KPIs** that combine operational (active accounts) and financial (deposit totals) signals.

These exercises build practical proficiency for interviews and day-to-day analytics—especially in creating stakeholder-ready summaries from normalized datasets.

## Tools & Technologies

* SQL (PostgreSQL / MySQL compatible)
* DBeaver, pgAdmin, or SSMS for query execution
* Git & GitHub for version control and portfolio building
