# CLARA AI Roles Architecture

Public architecture note for a general audience.

## Public Status

This document explains the four main AI roles used in the CLARA architecture at a high level. It describes responsibilities and collaboration patterns, not confidential implementation details, internal prompts, private datasets, infrastructure identifiers, or operational procedures.

An AI role is not necessarily the same thing as one deployed model. A role describes a responsibility in the system. Depending on the implementation stage, one role may be supported by one model, several models, or a combination of model logic, tools, rules, and human review.

## Simple View

CLARA can be understood as a cybersecurity assistant team:

- **CLARA Core** acts as the coordinator.
- **Audit Agent** checks system and configuration posture.
- **Network Agent** looks at communication patterns and network evidence.
- **Browser / URL Risk Agent** reviews web-navigation and link-related risks.

The goal is not to replace cybersecurity specialists. The goal is to help them read evidence faster, ask better questions, compare signals, document reasoning, and keep a trace of how conclusions were reached.

## Role 1: CLARA Core

CLARA Core is the central coordination role. It receives the user's question or task, interprets the intent, decides what type of help is needed, and routes work to the appropriate specialized role.

For the general user, CLARA Core is the part of the system that makes the experience feel coherent. It translates a broad request such as "is this activity suspicious?" into smaller steps that can be checked by the relevant specialist roles.

Main responsibilities:

- understand the user's request in natural language;
- identify whether the task is about audit, network evidence, browser risk, or a combined situation;
- select the appropriate specialist role or roles;
- combine findings into a clear explanation;
- preserve traceability by recording what was asked, what was checked, and how the answer was produced;
- avoid unsupported conclusions when the evidence is incomplete.

CLARA Core is important because cybersecurity questions often combine several domains. A suspicious link may be connected to unusual network traffic. A weak configuration may make a phishing attempt more dangerous. The coordinator role keeps these signals connected.

## Role 2: Audit Agent

The Audit Agent focuses on security posture. It helps review whether systems, configurations, policies, or technical controls appear aligned with expected security practices.

For a general audience, this role is similar to an inspector. It does not simply say that something is "good" or "bad"; it explains what was checked, why it matters, and what should be improved.

Typical responsibilities:

- review configuration evidence and security-control descriptions;
- identify missing, weak, or inconsistent security settings;
- organize observations by severity and business impact;
- connect findings to known security principles and public frameworks where appropriate;
- suggest remediation steps in understandable language;
- produce audit-friendly explanations that can be reviewed by a human operator.

The Audit Agent supports accountability. A security recommendation should be explainable, repeatable, and linked to the evidence available at the time of analysis.

## Role 3: Network Agent

The Network Agent focuses on communication evidence: logs, events, flows, alerts, and other indicators that describe how systems communicate.

For a general audience, this role is similar to a traffic analyst. It looks for communication patterns that may be normal, unusual, or suspicious, then explains what makes them worth attention.

Typical responsibilities:

- read and summarize network-related evidence;
- detect unusual timing, volume, destination, protocol, or behavior patterns;
- correlate multiple events that may be weak individually but stronger together;
- distinguish clear evidence from hypotheses;
- help prioritize what a human analyst should inspect next;
- support incident triage with concise explanations.

The Network Agent is useful because many cybersecurity incidents leave traces in communication behavior before they are fully understood. Its job is to turn raw signals into a structured investigation path.

## Role 4: Browser / URL Risk Agent

The Browser / URL Risk Agent focuses on web and link-related risk. It helps evaluate whether a page, URL, download path, or browser interaction may be unsafe.

For a general audience, this role is similar to a cautious web-safety assistant. It looks at visible and technical clues before recommending whether something deserves trust, caution, or escalation.

Typical responsibilities:

- examine URL structure and domain-related clues;
- identify phishing-like patterns and misleading presentation;
- consider download, redirection, and page-behavior risks;
- explain user-facing warning signs in plain language;
- support safe browsing and investigation workflows;
- avoid treating a single weak signal as conclusive proof.

This role is important because many attacks begin with a link, a page, a file, or a browser action. The system therefore treats web-navigation risk as a distinct area of analysis.

## How The Roles Work Together

A typical CLARA workflow can be summarized as:

1. A user asks a question or submits evidence.
2. CLARA Core interprets the request and decides which specialist role is relevant.
3. The selected role reviews the appropriate type of evidence.
4. If the case spans multiple domains, CLARA Core coordinates more than one role.
5. The results are combined into a response that separates facts, interpretation, uncertainty, and recommended next steps.
6. The interaction is recorded for auditability and later evaluation.

This role-based architecture keeps the system modular. Each role can improve independently while still contributing to one coherent cybersecurity assistant.

## Safety And Governance Principles

The public CLARA architecture emphasizes controlled, auditable AI use:

- **Controlled tools:** specialist roles should use only approved tools and allowed parameters.
- **Traceability:** important decisions, tool calls, and generated findings should be recorded.
- **Human oversight:** CLARA supports human operators; it does not remove responsibility from them.
- **Data minimization:** sensitive information should be used only when needed and should not be exposed in public outputs.
- **Clear uncertainty:** the system should say when evidence is incomplete or when a conclusion is only a hypothesis.
- **Public/private boundary:** public documentation explains concepts and research progress, not confidential operational details.

## Why Four Roles

The four-role design reflects a practical cybersecurity split:

- one coordinator is needed to understand the user's request and orchestrate work;
- audit analysis needs structured control and compliance reasoning;
- network analysis needs event correlation and anomaly interpretation;
- browser and URL risk needs web-specific safety reasoning.

Together, these roles cover the main research directions of the first CLARA architecture without forcing every task through one general-purpose component.

## Evolution

As CLARA develops, the roles may be refined, split, merged, or supported by different model and tool combinations. The public role names describe the responsibilities that should remain understandable to users, evaluators, and project stakeholders even as the technical implementation evolves.

