---
description: 'Generic Analytics Pack Report: run every available KPI and summarize
  the results.'
allowed-tools: mcp__mis-mcp-runtime__describe_schema, mcp__mis-mcp-runtime__get_data_profile,
  mcp__mis-mcp-runtime__list_kpis, mcp__mis-mcp-runtime__get_kpi, mcp__mis-mcp-runtime__run_safe_query,
  mcp__mis-mcp-runtime__search_records, mcp__mis-mcp-runtime__render_chart
---

Run the report command to generate the Generic Analytics Pack Report from your Generic Analytics Pack business data.

1. Call get_kpi("count_by_category") - Count by Category.
2. Call get_kpi("total_records") - Total Records.
3. Summarize the results in plain business language, calling out anything unusual.


Context from the business owner:
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
