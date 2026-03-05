---
title: "AgentEval Evidence Lab: Reproducible Evidence Packaging for Repository-Level LLM Agent Evaluation"
tags:
  - LLM agents
  - software engineering
  - reproducibility
  - benchmarking
  - evaluation tooling
authors:
  - name: Satya Narayana Panda
    affiliation: "1"
    corresponding: true
    email: spand14@unh.newhaven.edu
  - name: Bhumika Shah
    affiliation: "2"
affiliations:
  - index: 1
    name: Business Statistics, University of New Haven, West Haven, USA
  - index: 2
    name: Information Technology, University of the Cumberlands, Williamsburg, Kentucky, USA
date: 5 March 2026
bibliography: paper.bib
---

# Summary

AgentEval Evidence Lab is an open-source reproducibility package for evaluating repository-level LLM agent behavior in software engineering tasks. The repository provides a compact, auditable workflow that transforms run-level evaluation records into publication-ready tables and machine-readable evidence artifacts. It is designed for researchers who need transparent, repeatable analysis of task outcomes, quality metrics, latency, and safety signals without rebuilding an evaluation stack from scratch.

The software centers on a practical evidence workflow: curated run inputs in CSV form, a notebook-driven transformation pipeline, and deterministic output artifacts used directly in manuscripts and downstream analysis. The current version includes pilot benchmark outputs and templates that can be extended to larger studies.

# Statement of need

Evaluation of LLM coding systems frequently emphasizes synthetic or short-horizon benchmarks, while real repository workflows introduce complexity through iterative tool use, context management, and failure modes tied to safety and execution constraints. Teams attempting to reproduce such evaluations often face fragmented outputs, weak provenance, and manual table construction steps that are difficult to audit.

AgentEval Evidence Lab addresses this gap by packaging an end-to-end evidence layer around repository-level agent experiments. Instead of prescribing one model or one orchestration framework, it standardizes how run-level outcomes are represented and converted into analysis-ready artifacts. This makes it easier to compare backends under fixed policies, rerun hypothesis checks, and regenerate manuscript tables with traceable inputs.

The target audience includes researchers evaluating coding agents in realistic software tasks, practitioners maintaining benchmark suites for internal model comparisons, and teams preparing reproducibility artifacts for peer review or preprint release.

# State of the field

Function-level and benchmark-centric evaluations remain important for model progress, but they do not fully capture repository-grounded engineering performance [@chen2021evaluating; @jimenez2024swebench]. SQL-focused realism studies also show that benchmark success may overestimate practical task success in production-like settings [@yu2018spider; @li2024bird; @lei2024spider2].

Existing ecosystems provide experiment logging and notebook analysis, yet many workflows still require substantial custom glue to produce review-ready evidence with clear provenance. AgentEval Evidence Lab contributes at this interface: it narrows the distance between raw runs and publishable, inspectable evidence. Rather than replacing benchmark design or model orchestration frameworks, it complements them with a lightweight, open, and reproducible artifact pipeline.

# Software design

The repository is intentionally minimal and organized into three stable surfaces: structured inputs and templates in `tables/`, an executable notebook pipeline in `notebooks/`, and immutable outputs in `artifacts/`.

This design prioritizes low-friction reuse and explicit data flow. Notebook execution is the primary interface to lower onboarding cost for mixed research teams while preserving deterministic output files for archival and review. The trade-off is that notebook-based pipelines can become opaque if unconstrained; this is mitigated by keeping inputs and outputs in stable directories and by committing generated artifacts.

# Research impact statement

AgentEval Evidence Lab has immediate value as a reproducibility companion to repository-level LLM agent evaluation studies. It has been used to generate evidence assets accompanying the associated manuscript and enables external users to inspect, rerun, and adapt the analysis workflow.

Its near-term research impact comes from three concrete benefits: comparability through a consistent run-level schema, auditability through committed JSON and tabular artifacts, and reusability through templates for scaling beyond pilot experiments.

# AI usage disclosure

Generative AI tools were used in limited ways to assist drafting and editing of software documentation and manuscript-related text. Human authors made the core research decisions, software design decisions, and all evaluative judgments. All AI-assisted outputs were reviewed and edited by the authors before release.

# Acknowledgements

We thank mentors, teachers, and collaborators who supported this work, and our families for sustained encouragement throughout this project.

# References
