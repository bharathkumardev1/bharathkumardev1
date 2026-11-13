I'm Bharath Mandha, an AI engineer in Dallas. I build retrieval and agent systems over financial documents at Goldman Sachs. Before that I built readmission risk models at Cigna Healthcare and retail demand forecasts at Deloitte.

Every repo below runs on public data, commits its code, evaluation and results, and reports each headline number against a baseline.

**[wiki-retrieval](https://github.com/bharathkumardev1/wiki-retrieval)**: search over the 2.68M-passage BEIR Natural Questions corpus with a LoRA-tuned MiniLM, an INT8 ONNX reranker and a cite-or-refuse agent.
nDCG@10 0.402 on the full corpus, against 0.290 for BM25 and +0.014 over the untuned encoder (paired p 0.0001). [Demo video](https://www.youtube.com/watch?v=5vtW4iaUe3A)

**[tlc-demand](https://github.com/bharathkumardev1/tlc-demand)**: a LightGBM Poisson forecast of 15-minute NYC taxi pickups, served through ONNX behind a Spring Boot gateway with a circuit breaker.
WAPE 0.2415 against 0.3104 for the best simple baseline; it loses in the two quietest zone quartiles. [Demo video](https://youtu.be/Hd28gbz9jy0)

**[finance-rag-eval](https://github.com/bharathkumardev1/finance-rag-eval)**: page-level retrieval over SEC filings on FinanceBench.
A company and period filter plus statement routing take held-out Hit@10 from 0.14 to 0.71. An embedding hybrid tied BM25 at about five times the latency, so BM25 ships. [Try it in the browser](https://bharathkumardev1.github.io/projects/finance-rag-eval/)

**[readmission-capacity](https://github.com/bharathkumardev1/readmission-capacity)**: which discharged patients a care team should call when it can call one in ten.
A LightGBM call list holds 25.0% of 30-day readmissions, against 20.6% for calling whoever had the most prior stays. [Try it in the browser](https://bharathkumardev1.github.io/projects/readmission-capacity/)

**[Agentic-Research-Assistant](https://github.com/bharathkumardev1/Agentic-Research-Assistant)**: a LangGraph loop that reviews its own cited answers about research papers, measured against a single pass on QASPER.
The loop loses to a wider single pass (58.7% against 68.0% judged correct), so the extra model calls aren't worth it. CI replays every recorded model call without an API key.

Case studies and my résumé are at [bharathkumardev1.github.io](https://bharathkumardev1.github.io).
