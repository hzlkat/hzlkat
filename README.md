## Hi there

I'm Katharina, an AI Engineer with a passion for building practical AI solutions and exploring new technologies.

### Projects

#### [Mobility-on-Demand Transport Prediction](https://github.com/hzlkat/Mobility-on-demand-transport-prediction)

End-to-end ML pipeline for forecasting demand for on-demand mobility services on Google Cloud.

- **Data preparation & cleaning:** handling missing values and outliers, feature engineering for temporal and spatial patterns
- **Data visualization:** exploratory analysis of demand over time and across regions
- **Model training & evaluation:** training and comparing temporal and spatiotemporal models (see table)
- **Explainability:** SHAP values to interpret model predictions and identify the key demand drivers

| Approach | Platform | Models |
|---|---|---|
| Temporal forecasting | GCP | Linear Regression, Random Forest, LSTM |
| Spatiotemporal forecasting | GCP (Vertex AI) | Linear Mixed Model, Mixed Effects Random Forest |

#### Contract Analysis

RAG application for analyzing contracts, built on the [NVIDIA RAG Blueprint](https://build.nvidia.com/nvidia/build-a-rag-pipeline).

- **Foundation:** NVIDIA's RAG Blueprint as the base pipeline for document ingestion, retrieval and answer generation, using NVIDIA NIM microservices, NeMo Retriever (embedding & reranking) and Milvus as the vector database
- **Hybrid search:** extended the semantic retrieval with keyword search, so exact terms such as contract numbers, party names or specific clauses are found reliably
- **Contract filtering:** narrowing the search to selected contracts, so answers are grounded only in the relevant documents

#### Hermes Agents: Account Manager Dashboard

Multi-agent dashboard that supports account managers in their daily work, powered by specialized Hermes agents running on an on-prem Linux server and NVIDIA DGX Spark.

- **Morning Briefing agent:** researches news on interests and key accounts and turns them into story cards and call-prep cards for the day's meetings
- **Podcast agent:** generates a 2–3 minute spoken call-prep briefing with text-to-speech for listening on the go
- **Contract Analyst agent:** reviews NDAs against a company checklist with a traffic-light rating (mutuality, exceptions, group privilege, liability caps) and produces revised drafts
- **Live agent activity:** streams intermediate steps and tool events to the dashboard via Server-Sent Events instead of a loading spinner
- **Cost & resource transparency:** tracks tokens per agent profile, disk footprint and host CPU/RAM, separating cloud inference from on-prem metrics
- **Engineering:** FastAPI backend, isolated agent profiles via `HERMES_HOME`, token cost control with turn limits and tool scoping, scripted deployment to DGX Spark

#### [Hermes Agents x Wiz Cloud Security](https://github.com/hzlkat/wiz-hermes-security)

Securing an AI agent framework (Hermes Agents) running on an on-premises Ubuntu host with Wiz.

- **Runtime protection:** deployed the eBPF-based Wiz Runtime Sensor for real-time process, network and file integrity monitoring of agent workloads
- **Vulnerability management:** used the Wiz Workload Scanner to generate SBOMs (OS packages, Python and Node.js dependencies) and map them against CVE databases
- **On-prem architecture:** modeled the subscription, resource and project hierarchy in Wiz, including RBAC scoping for teams
- **Onboarding insights:** documented the asynchronous Security Graph sync and how sensor-only hosts appear as native servers in Wiz

### Tech Stack

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?logo=linux&logoColor=black)
![Azure AI](https://img.shields.io/badge/Azure%20AI-0078D4?logo=microsoftazure&logoColor=white)
![Google Cloud](https://img.shields.io/badge/Google%20Cloud-4285F4?logo=googlecloud&logoColor=white)
![NVIDIA AI Enterprise](https://img.shields.io/badge/NVIDIA%20AI%20Enterprise-76B900?logo=nvidia&logoColor=white)

### Let's collaborate

I enjoy taking GenAI, AI agents and RAG applications from proof of concept to production, whether on-premises, hybrid or in the cloud. If you're working on enterprise AI deployments, I'd love to connect and exchange ideas.