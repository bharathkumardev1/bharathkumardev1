I'm Bharath Mandha, an AI/ML engineer in Dallas. At Goldman Sachs I build retrieval and agent systems over financial documents; before that I built readmission risk models at Cigna and demand forecasts at Best Buy.

The first two repos below are problems from my jobs, rebuilt on public data so every number can be checked: code, evaluation, committed results, and CI that reruns them.

- [finance-rag-eval](https://github.com/bharathkumardev1/finance-rag-eval): retrieval over SEC filings, scored page by page on FinanceBench. Reading the company and period from the question and sending statement questions to statement pages takes held-out Hit@10 from 0.14 to 0.75. A MiniLM hybrid led on the dev split and tied BM25 on test at about five times the latency, so the service runs BM25: 126 queries a second per core at 12 ms p95.
- [readmission-capacity](https://github.com/bharathkumardev1/readmission-capacity): which discharged patients a care team should call when it can call one in ten. On 101,766 public encounters split by patient, a LightGBM call list holds 25.0% of 30-day readmissions against 20.5% for calling whoever had the most prior inpatient stays, with reason codes on every call and the patients it misses spelled out.
- [Agentic-Research-Assistant](https://github.com/bharathkumardev1/Agentic-Research-Assistant): answers about research papers with cited passages, from a LangGraph loop where a second model call reviews each answer and asks for another search when it falls short. Its evaluation against a single pass on QASPER records every model reply, so CI can rerun it without an API key.

The first two have demos that run in the browser at [bharathkumardev1.github.io](https://bharathkumardev1.github.io), next to my résumé.
