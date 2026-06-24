<!-- ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░  HERO  ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ -->
<div align="center">

<img width="100%" src="./assets/header.svg" alt="Sathvik Reddy Puli — Senior Data Engineer" />

<br/>

<img src="./assets/typing.svg" alt="Streaming · Lakehouses · AI in production" />

<br/><br/>

<a href="https://portfolio-fawn-beta-zjvbplk2vx.vercel.app"><img src="https://img.shields.io/badge/Live_Portfolio-0B0F1A?style=for-the-badge&logo=vercel&logoColor=22D3EE&labelColor=0B0F1A" alt="Portfolio" /></a>
<a href="https://www.linkedin.com/in/sathvik-0d138/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
<a href="mailto:sathvikreddyp061@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>

</div>

<!-- ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░  INTRO  ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ -->
<br/>

> 👋 I'm **Sathvik** — a senior data engineer with five years building real-time pipelines and lakehouses on AWS for financial services and healthcare. I care about one thing above all: shrinking the latency between an **event** happening and the **decision** it should trigger. Every project below is **open-source and reproducible from a single `make` command.**

<!-- ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░  LIVE PIPELINE  ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ -->
## 🛰️ The system I build, end to end

<div align="center">

<img width="100%" src="./assets/pipeline.svg" alt="Animated event-to-decision data pipeline" />

<sub>**ingest → event spine → compute → lakehouse → serve** — watch the data flow through it.</sub>

</div>

<!-- ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░  3D STACK  ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ -->
## 🧊 My stack, in three dimensions

<div align="center">

<img width="100%" src="./assets/tech-iso.svg" alt="Isometric 3D tech stack" />

</div>

<!-- ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░  PROJECTS  ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ -->
## 🚀 Featured Projects — deep dive

<div align="center">
<table>
<tr>
<td width="50%" align="center">
<a href="https://github.com/sathvikreddyp061-collab/fraud-streaming"><img width="100%" src="./assets/pin-fraud-streaming.svg" alt="fraud-streaming" /></a>
</td>
<td width="50%" align="center">
<a href="https://github.com/sathvikreddyp061-collab/retail-cdc"><img width="100%" src="./assets/pin-retail-cdc.svg" alt="retail-cdc" /></a>
</td>
</tr>
<tr>
<td width="50%" align="center">
<a href="https://github.com/sathvikreddyp061-collab/claims-lakehouse"><img width="100%" src="./assets/pin-claims-lakehouse.svg" alt="claims-lakehouse" /></a>
</td>
<td width="50%" align="center">
<a href="https://github.com/sathvikreddyp061-collab/portfolio"><img width="100%" src="./assets/pin-portfolio.svg" alt="portfolio" /></a>
</td>
</tr>
</table>
</div>

### ⚡ [fraud-streaming](https://github.com/sathvikreddyp061-collab/fraud-streaming) &nbsp;·&nbsp; sub-second risk on a 5K event/sec spine

> Re-platformed a batch-heavy risk surface into an event-native lakehouse. Card-auth events hit Kafka under strict Avro contracts; PySpark Structured Streaming joins each against a Redis feature store and scores with XGBoost→ONNX — **P99 inference under 1 ms**, well inside the 250 ms decisioning budget.

<p align="center">
<img src="https://img.shields.io/badge/5K-events%2Fsec_sustained-22F0FF?style=for-the-badge&labelColor=0B0F1A" />
<img src="https://img.shields.io/badge/%3C1ms-P99_inference-22F0FF?style=for-the-badge&labelColor=0B0F1A" />
<img src="https://img.shields.io/badge/0.892-model_AUC-22F0FF?style=for-the-badge&labelColor=0B0F1A" />
<img src="https://img.shields.io/badge/73%25-recall@review-22F0FF?style=for-the-badge&labelColor=0B0F1A" />
</p>

`Kafka (Redpanda) + Avro → PySpark Structured Streaming ⇄ Redis features → XGBoost/ONNX → Iceberg silver · alerts topic · FastAPI`

### 🔄 [retail-cdc](https://github.com/sathvikreddyp061-collab/retail-cdc) &nbsp;·&nbsp; exactly-once change data capture

> Postgres logical decoding → Debezium → Kafka → Spark/Iceberg → dbt → a custom reverse-ETL worker. The **outbox pattern + content-hash idempotency** proves producer-side exactly-once: 76,533 webhook POSTs on first run, **zero on rerun**.

<p align="center">
<img src="https://img.shields.io/badge/1.1M-CDC_events-FF3CAC?style=for-the-badge&labelColor=0B0F1A" />
<img src="https://img.shields.io/badge/76,533-exactly--once_POSTs-FF3CAC?style=for-the-badge&labelColor=0B0F1A" />
<img src="https://img.shields.io/badge/45%2F45-dbt_tests-FF3CAC?style=for-the-badge&labelColor=0B0F1A" />
<img src="https://img.shields.io/badge/%3C5min-on_a_laptop-FF3CAC?style=for-the-badge&labelColor=0B0F1A" />
</p>

`PostgreSQL 16 → Debezium 2.6 → Kafka → PySpark → Iceberg → dbt-DuckDB → content-hash reverse-ETL → mock Segment`

### 🏥 [claims-lakehouse](https://github.com/sathvikreddyp061-collab/claims-lakehouse) &nbsp;·&nbsp; HIPAA-flavored claims lakehouse

> Synthetic patients (Synthea) and a hand-written **X12 EDI 837 writer + parser** flow through Kafka into Iceberg, transform via dbt-DuckDB, pass Great Expectations gates, get SHA-256 PII masking, and land as a Member-360 mart — all orchestrated by Airflow.

<p align="center">
<img src="https://img.shields.io/badge/55K-claims_0_dropped-7C5CFF?style=for-the-badge&labelColor=0B0F1A" />
<img src="https://img.shields.io/badge/26%2F26-dbt_tests-7C5CFF?style=for-the-badge&labelColor=0B0F1A" />
<img src="https://img.shields.io/badge/8%2F8-GE_expectations-7C5CFF?style=for-the-badge&labelColor=0B0F1A" />
<img src="https://img.shields.io/badge/%3C3min-end--to--end-7C5CFF?style=for-the-badge&labelColor=0B0F1A" />
</p>

`Synthea + EDI 837 → Kafka → PySpark Iceberg → dbt-DuckDB → Great Expectations → hipaa_mask → Member 360 → Airflow`

### 🎨 [portfolio](https://github.com/sathvikreddyp061-collab/portfolio) &nbsp;·&nbsp; the cinematic front door

> A 3D, WebGL personal site that makes the work above tangible. `Next.js App Router · React Three Fiber · custom GLSL particle shaders · Framer Motion · Lenis` — **[live ↗](https://portfolio-fawn-beta-zjvbplk2vx.vercel.app)**

<!-- ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░  STATS  ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ -->
## 📊 GitHub Activity

<div align="center">

<img height="170" src="./assets/stats.svg" alt="GitHub stats" />
&nbsp;
<img height="170" src="./assets/top-langs.svg" alt="Top languages" />

<br/><br/>

<img width="92%" src="./assets/activity.svg" alt="Contribution activity graph" />

</div>

<!-- ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░  FOOTER  ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ -->
## 💬 Let's talk

<div align="center">

Want a walkthrough of any pipeline? Reach out.

<a href="https://www.linkedin.com/in/sathvik-0d138/"><img src="https://img.shields.io/badge/Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
<a href="mailto:sathvikreddyp061@gmail.com"><img src="https://img.shields.io/badge/Say_Hello-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>

<img width="100%" src="./assets/footer.svg" alt="" />

</div>
