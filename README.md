I'm Bharath Mandha, a machine learning engineer at Goldman Sachs. I build retrieval and agent systems over financial documents. Before that I built readmission risk models at Cigna and demand forecasts at Best Buy.

The first two repos below are problems from my jobs, rebuilt on public data so every number can be checked: code, evaluation, committed results, and CI that reruns them.

- **[finance-rag-eval](https://github.com/bharathkumardev1/finance-rag-eval)**: retrieval over SEC filings, scored page by page on FinanceBench. Reading the company and period out of the question and sending statement questions to statement pages takes held-out Hit@10 from 0.14 to 0.75. A MiniLM hybrid looked better on the dev split and tied BM25 on test at 9x the latency, so BM25 ships. The service does about 170 requests a second per core.
- **[readmission-capacity](https://github.com/bharathkumardev1/readmission-capacity)**: which discharged patients to call when the care team can call 10% of them. On 101,766 public encounters split by patient, a LightGBM list reaches 24.9% of 30-day readmissions against 20.5% for the usual prior-visits rule, and the README shows who it misses.
- **[Agentic-Research-Assistant](https://github.com/bharathkumardev1/Agentic-Research-Assistant)**: cited answers over a set of papers from a retrieve, summarize and evaluate loop in LangGraph, with a hard cap on model calls. Tested end to end offline; answer quality isn't measured yet, and the README says how I'd measure it.

Both evaluations have demos that run in the browser at [bharathkumardev1.github.io](https://bharathkumardev1.github.io), next to my resume.
