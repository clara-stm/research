# CLARA Research

Public English research-dissemination area for the CLARA project.

## Project

CLARA - an acronym for **CyberSecurity Learning And Response Agent** - develops an AI-assisted cybersecurity architecture for detection, analysis, explanation, learning, and response support. The public materials expressly published in this repository are disseminated as open-source public research artifacts under the Apache License 2.0, unless a file states otherwise. This public license does not include non-public CLARA materials or proprietary copyrighted works owned by AI STM LEARNING S.R.L. that are not expressly included here.

The public materials in this repository summarize technical and research progress without publishing operational secrets, private datasets, internal evidence, credentials, proprietary implementation artifacts, or confidential implementation details.

CLARA is positioned as a modular, auditable system built around a specialized language-model core, specialized cybersecurity agents, controlled tool use, traceable execution, and research assets for reproducible evaluation.

## Project Evolution Notice

Materialele publicate reflectă starea proiectului CLARA și a procesului de cercetare-dezvoltare-inovare la momentul publicării rapoartelor sau al disponibilizării informațiilor online. Pe parcursul evoluției proiectului pot surveni modificări substanțiale, inclusiv schimbări arhitecturale, ajustări ale componentelor tehnice, ale priorităților de integrare sau ale modului de livrare, în funcție de rezultatele cercetării, validării, feedbackului operațional și în special datorită obiectivului de a obține o aliniere produs-piață cât mai solidă.

## Financing And Project References

| Field | Value |
| --- | --- |
| Program | Program Creștere Inteligentă, Digitalizare și Instrumente Financiare |
| Priority | P1. Supporting and promoting an attractive and competitive RDI ecosystem in Romania |
| Specific objective | RSO1.1. Developing and enhancing research and innovation capacities and adopting advanced technologies |
| Action | Action 1.1. Support for the private sector and collaboration between public-system actors and the business environment in RDI |
| Call | `PCIDIF/155/PCIDIF_P1/OP1/RSO1.1/PCIDIF_A1` |
| Project title | CLARA (CyberSecurity Learning And Response Agent) - Innovative Cybersecurity Solution |
| SMIS code | `334596` |
| Financing contract | `390016/28.08.2025` |
| Implementation period | `29.08.2025 - 28.08.2027` |
| Beneficiary | AI STM LEARNING S.R.L. |
| Implementation region | South-East Region, Romania |

## Objective

The objective of CLARA is to research, design, and validate an AI-assisted cybersecurity system that can support human operators in understanding security events, correlating evidence, recommending response actions, and learning from controlled feedback while preserving auditability, privacy, and security-by-design constraints.

## Main Research Directions

- **LLM and SLM use in cybersecurity:** natural-language interpretation, incident triage, explanation, summarization, and report generation.
- **Multi-agent cybersecurity orchestration:** a CLARA Core coordinating specialized agents for audit, network monitoring, browser-risk analysis, and future defensive workflows.
- **Controlled tool use:** allowlisted tools, parameter validation, sandboxing, traceability, and mitigation of tool-injection risks.
- **Knowledge grounding:** structured cybersecurity knowledge, MITRE ATT&CK-style mapping, STIX-like representations, RAG/GraphRAG, and evidence-linked explanations.
- **Privacy-preserving and edge-aware learning:** local execution, minimization of sensitive data flows, LoRA-style adaptation, federated-learning concepts, and privacy-preserving evaluation.
- **Synthetic cybersecurity data:** large-scale synthetic logs, network events, threat-intelligence-like records, and attack episodes for repeatable testing without real operational data.
- **Reproducible evaluation:** evaluation harnesses, evaluation records, model/version traceability, prompt/tool-call records, and comparable technical reports.
- **Distributed and auditable execution:** research alignment with edge orchestration, immutable audit, and controlled adversarial validation.

## Main Project Components

| Component | Role |
| --- | --- |
| CLARA Core | Interprets user intent, plans work, routes tasks, aggregates agent outputs, and produces explanatory responses. |
| Specialized agents | Execute focused cybersecurity tasks such as audit, network analysis, browser risk checks, triage, or reporting. |
| Tool Registry | Controls which tools may be called, under which parameters, with logging and policy enforcement. |
| Internal messaging | Standardizes requests, responses, events, severity, evidence, correlation IDs, and error reporting. |
| Audit and trace layer | Records routing decisions, tool calls, agent results, and final responses for explainability and debugging. |
| Knowledge layer | Grounds answers in cybersecurity taxonomies, threat knowledge, and project-approved references. |
| Synthetic data package | Provides repeatable cybersecurity scenarios for testing, validation, and model evaluation. |
| Evaluation harness | Supports reproducible measurement of model, agent, and workflow behavior over time. |
| Adaptive education layer | Planned learning and guidance layer for operators and users. |
| Management infrastructure | Covers configuration, monitoring, access control, and operational governance. |

## Architecture Documents

The architecture directory has its own index for GitHub browsing:
[architecture/README.md](architecture/README.md).

| Topic | Document |
| --- | --- |
| Main AI roles | [architecture/AI_ROLES.md](architecture/AI_ROLES.md) |
| Execution and integration | [architecture/EXECUTION_AND_INTEGRATION.md](architecture/EXECUTION_AND_INTEGRATION.md) |

## Reports

The reports directory has its own current index:
[reports/README.md](reports/README.md).

| English | Romanian |
| --- | --- |
| [reports/REPORT_01.md](reports/REPORT_01.md) | [../ro/rapoarte/RAPORT_01.md](../ro/rapoarte/RAPORT_01.md) |
| [reports/REPORT_02.md](reports/REPORT_02.md) | [../ro/rapoarte/RAPORT_02.md](../ro/rapoarte/RAPORT_02.md) |

## Copyright And License

Copyright (c) 2026 AI STM LEARNING S.R.L. and contributors.

Unless stated otherwise, only the files and materials expressly published in this repository are made available under the Apache License 2.0. This repository contains public summaries and dissemination materials.

The Apache License 2.0 does not grant rights to non-public CLARA materials or to proprietary copyrighted works, software, datasets, models, prompts, infrastructure descriptions, trademarks, trade secrets, know-how, personal data, credentials, third-party content, or other intellectual property owned by AI STM LEARNING S.R.L. that are not expressly included here.

## Public Disclosure Notice

The reports in this repository are public research summaries derived from project technical reports. They intentionally omit sensitive operational details, exact internal storage locations, credentials, private datasets, raw evidence, personal data, and non-public implementation artifacts.
