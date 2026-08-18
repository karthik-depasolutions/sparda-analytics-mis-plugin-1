---
name: generic-analytics-analyst
description: Use this skill when analyzing Generic Analytics Pack data - revenue,
  volumes, trends, and pre-built KPIs (count_by_category, total_records). Guides querying
  via the bundled MCP tools instead of ad-hoc SQL.
metadata:
  pack_slug: generic-analytics
  pack_version: 1.0.0
---

# Generic Analytics Pack Analyst

Utilize the Generic Analytics Pack skill when analyzing tabular business data that does not clearly align with any specialized industry-specific analytics packages. This pack serves as a reliable, industry-agnostic fallback, providing a foundational analysis when no higher-confidence, specialized match is identified.

## Available KPIs

- `count_by_category` - **Count by Category**: Record count grouped by the primary categorical dimension. (unit: count)
- `total_records` - **Total Records**: Total number of rows in the primary table. (unit: count)

Not available for this data source (required data was missing): `average_measure`, `sum_measure`, `trend_by_month`

## How to use the MCP tools

1. Call `mcp__mis-mcp-runtime__describe_schema` or `mcp__mis-mcp-runtime__list_kpis` first if you're unsure what's available.
2. Prefer `mcp__mis-mcp-runtime__get_kpi` with one of the KPI ids above over writing SQL.
3. Use `mcp__mis-mcp-runtime__run_safe_query` only for questions no KPI answers, and always as a read-only SELECT with explicit columns.

## Guardrails

- No industry-specific vocabulary is assumed — treat all categorical values literally
- All data access must be read-only


## Context from the business owner

## What the business owner told us
- Q: What does it mean for your business that nearly all `agent_id` values are 'spardha-staging'?  A: this is campaign run for single session 
- Q: What does it mean for your business that 61% of `callback_date` entries are the string 'NULL' instead of actual missing values?  A: no one is opted for callback .
- Q: What does it mean for your business that 62.4% of `callback_time` entries are the string 'NULL'?  A: ignore
- Q: What does it mean for your business that almost all `campaign_id` values are 'bf7e5967-9de0-479e-8617-524daa2604cf'?  A: this is the id for campaign that has been done
- Q: What does it mean for your business that nearly all `dataset_id` values are 'stream-bf7e5967-9de0-479e-8617-524daa2604cf'?  A: the dataset where we picked the user phonenumbers to call
- Q: Anything else about this data an analyst should know?  A: this is data of ai_calling to get the leads .
## Known data-quality findings
- [medium] sparda_leads.agent_id: 94.9% of 5,530 non-null rows in "agent_id" are "spardha-staging".
- [medium] sparda_leads.callback_date: 61.0% of 223 non-null rows in "callback_date" are "NULL".
- [medium] sparda_leads.callback_time: 62.4% of 218 non-null rows in "callback_time" are "NULL".
- [medium] sparda_leads.campaign_id: 94.4% of 5,530 non-null rows in "campaign_id" are "bf7e5967-9de0-479e-8617-524daa2604cf".
- [medium] sparda_leads.dataset_id: 94.4% of 5,530 non-null rows in "dataset_id" are "stream-bf7e5967-9de0-479e-8617-524daa2604cf".
- [medium] sparda_leads.dataset_name: 94.4% of 5,530 non-null rows in "dataset_name" are "demo".
- [medium] sparda_leads.leads_score: 93.3% of 4,819 non-null rows in "leads_score" are "LOW".
- [medium] sparda_leads.outcome_of_the_call: 84.8% of 5,530 non-null rows in "outcome_of_the_call" are "unclear".
- [medium] sparda_leads.preferred_reschedule_time: 60.2% of 226 non-null rows in "preferred_reschedule_time" are "NULL".
- [medium] sparda_leads.user_sentiment: 65.5% of 2,091 non-
