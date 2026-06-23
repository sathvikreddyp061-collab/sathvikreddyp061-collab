<!-- ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░  HERO  ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ -->
<div align="center">

<img width="100%" src="./assets/header.svg" alt="Sathvik Reddy Puli — Senior Data Engineer" />

<br/>

<img src="./assets/typing.svg" alt="Streaming · Lakehouses · AI in production" />

<br/><br/>

<a href="https://portfolio-fawn-beta-zjvbplk2vx.vercel.app"><img src="https://img.shields.io/badge/Live_Portfolio-0B0F1A?style=for-the-badge&logo=vercel&logoColor=22D3EE&labelColor=0B0F1A" alt="Portfolio" /></a>
<a href="https://www.linkedin.com/in/sathvik-0d138/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
<a href="mailto:sathvikreddyp061@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
<img src="https://img.shields.io/badge/Frisco,_TX-6D28D9?style=for-the-badge&logo=googlemaps&logoColor=white" alt="Location" />

</div>

<!-- ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░  INTRO  ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ -->
<br/>

> 👋 I'm **Sathvik** — a senior data engineer with five years building real-time pipelines and lakehouses on AWS for financial services and healthcare. I care about one thing above all: shrinking the latency between an **event** happening and the **decision** it should trigger.

<div align="center">
  <img width="78%" src="./assets/skills.svg" alt="Tech stack icons" />
</div>

<!-- ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░  ARCHITECTURE  ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ -->
## 🗺️ How I think about data systems

```mermaid
flowchart LR
    subgraph SRC["🟢 Sources"]
        PG[(Postgres)]
        EDI[EDI 837 / Synthea]
        CARD[Card-auth events]
    end
    subgraph SPINE["🔵 Event Spine"]
        DBZ[Debezium CDC]
        K{{Apache Kafka}}
    end
    subgraph COMPUTE["🟣 Compute"]
        SS[Spark Structured Streaming]
        ICE[(Apache Iceberg Lakehouse)]
        DBT[dbt transforms]
    end
    subgraph SERVE["🟡 Serve / Decide"]
        RDS[(Redis features)]
        ML[XGBoost · ONNX]
        API[FastAPI scoring]
        BI[Analytics marts]
    end

    PG --> DBZ --> K
    EDI --> K
    CARD --> K
    K --> SS --> ICE --> DBT
    SS --> RDS --> ML --> API
    DBT --> BI

    classDef src fill:#0B0F1A,stroke:#22F0FF,color:#fff
    classDef spine fill:#0B0F1A,stroke:#22D3EE,color:#fff
    classDef comp fill:#0B0F1A,stroke:#6D28D9,color:#fff
    classDef serve fill:#0B0F1A,stroke:#F0ABFC,color:#fff
    class PG,EDI,CARD src
    class DBZ,K spine
    class SS,ICE,DBT comp
    class RDS,ML,API,BI serve
```

<!-- ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░  PROJECTS  ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ -->
## 🚀 Featured Projects

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

- ⚡ **[fraud-streaming](https://github.com/sathvikreddyp061-collab/fraud-streaming)** — sub-250ms card-auth fraud scoring on a 5K eps stream. `Kafka → Spark → Redis → XGBoost (ONNX) → Iceberg + FastAPI`
- 🔄 **[retail-cdc](https://github.com/sathvikreddyp061-collab/retail-cdc)** — exactly-once CDC via outbox + content-hash. `Postgres → Debezium → Kafka → Spark/Iceberg → dbt → reverse-ETL`
- 🏥 **[claims-lakehouse](https://github.com/sathvikreddyp061-collab/claims-lakehouse)** — HIPAA-flavored claims lakehouse. `Synthea + EDI 837 → Kafka → PySpark Iceberg → dbt → Great Expectations → Airflow`
- 🎨 **[portfolio](https://github.com/sathvikreddyp061-collab/portfolio)** — cinematic 3D site. `Next.js · React Three Fiber · GLSL shaders · Framer Motion` · **[Live ↗](https://portfolio-fawn-beta-zjvbplk2vx.vercel.app)**

<!-- ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░  STACK  ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ -->
## 🧰 Tech I work with

<div align="center">

| Layer | Tools |
|:--|:--|
| **Languages** | ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white) ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white) |
| **Streaming** | ![Kafka](https://img.shields.io/badge/Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white) ![Debezium](https://img.shields.io/badge/Debezium-FF4632?style=flat-square&logo=redhat&logoColor=white) ![Spark](https://img.shields.io/badge/Spark_Streaming-E25A1C?style=flat-square&logo=apachespark&logoColor=white) |
| **Lakehouse** | ![Iceberg](https://img.shields.io/badge/Iceberg-2496ED?style=flat-square&logo=apache&logoColor=white) ![Delta](https://img.shields.io/badge/Delta_Lake-00ADD4?style=flat-square&logo=databricks&logoColor=white) ![dbt](https://img.shields.io/badge/dbt-FF694B?style=flat-square&logo=dbt&logoColor=white) ![DuckDB](https://img.shields.io/badge/DuckDB-FFF000?style=flat-square&logo=duckdb&logoColor=black) |
| **Warehouse** | ![Snowflake](https://img.shields.io/badge/Snowflake-29B5E8?style=flat-square&logo=snowflake&logoColor=white) ![Redshift](https://img.shields.io/badge/Redshift-8C4FFF?style=flat-square&logo=amazonredshift&logoColor=white) |
| **Orchestration** | ![Airflow](https://img.shields.io/badge/Airflow-017CEE?style=flat-square&logo=apacheairflow&logoColor=white) ![Step Functions](https://img.shields.io/badge/Step_Functions-FF4F8B?style=flat-square&logo=awslambda&logoColor=white) |
| **AI / ML** | ![Bedrock](https://img.shields.io/badge/Bedrock-232F3E?style=flat-square&logo=amazonwebservices&logoColor=FF9900) ![SageMaker](https://img.shields.io/badge/SageMaker-232F3E?style=flat-square&logo=amazonwebservices&logoColor=FF9900) ![XGBoost](https://img.shields.io/badge/XGBoost-189FDD?style=flat-square&logo=python&logoColor=white) ![ONNX](https://img.shields.io/badge/ONNX-005CED?style=flat-square&logo=onnx&logoColor=white) |
| **Infra** | ![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=FF9900) ![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=flat-square&logo=terraform&logoColor=white) ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white) ![GitHub Actions](https://img.shields.io/badge/Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white) ![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white) |

</div>

<!-- ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░  STATS  ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ -->
## 📊 GitHub Activity

<div align="center">

<img height="170" src="./assets/stats.svg" alt="GitHub stats" />
&nbsp;
<img height="170" src="./assets/top-langs.svg" alt="Top languages" />

<br/><br/>

<img width="92%" src="https://raw.githubusercontent.com/sathvikreddyp061-collab/sathvikreddyp061-collab/output/github-contribution-grid-snake-dark.svg" alt="Contribution snake" />

<br/>

<img width="92%" src="./assets/activity.svg" alt="Contribution activity graph" />

</div>

<!-- ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░  FOOTER  ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ -->
## 💬 Let's talk

<div align="center">

Open to senior data engineering roles — remote · hybrid · on-site. Want a walkthrough of any pipeline? Reach out.

<a href="https://www.linkedin.com/in/sathvik-0d138/"><img src="https://img.shields.io/badge/Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
<a href="mailto:sathvikreddyp061@gmail.com"><img src="https://img.shields.io/badge/Say_Hello-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>

<img width="100%" src="./assets/footer.svg" alt="" />

</div>

<!-- profile readme -->
