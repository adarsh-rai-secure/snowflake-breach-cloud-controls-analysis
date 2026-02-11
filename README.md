# When Shared Responsibility Breaks: UNC5537 Snowflake Attack Analysis

## Project Summary

Analyzing the 2024 UNC5537 campaign targeting Snowflake customer accounts, reconstructing the credential-abuse attack chain, and evaluating how optional MFA enforcement, excessive role privileges, and weak egress monitoring enabled large-scale data exfiltration. This research maps observed control failures to formal security models (Bell–LaPadula and Clark–Wilson) and proposes a modified shared-responsibility framework for high-value SaaS data platforms.

The analysis demonstrates that the breach did not exploit a platform vulnerability, but rather systemic weaknesses in identity assurance and shared-responsibility execution. Over 100+ tenants were impacted, with estimated aggregate response costs exceeding $25M across affected organizations. Mandatory MFA, conditional access, scoped RBAC, and rate-limited exports would have nullified or materially constrained the attack vector. :contentReference[oaicite:0]{index=0}

## Scope of Analysis

- Reconstructing the four-stage UNC5537 attack chain (credential harvesting, validation, session abuse, and exfiltration)
- Evaluating failed safeguards across IAM, RBAC, anomaly detection, and egress controls
- Quantifying economic impact through counterfactual cost analysis
- Applying Bell–LaPadula (confidentiality) and Clark–Wilson (integrity) models to modern SaaS environments
- Proposing a Modified SaaS Shared Responsibility Framework aligned with “shared-fate” security principles

## Core Insight

Credential-based compromise remains the dominant SaaS breach vector. When MFA is optional, roles are over-permissive, and export telemetry lacks enforcement, valid credentials bypass perimeter defenses entirely. The incident illustrates that in multi-tenant SaaS platforms, provider defaults directly shape customer exposure. Effective cloud security cannot rely on documentation alone; it must be enforced through baseline identity controls and verifiable policy mechanisms.

## Repository Contents

- Full research paper (technical analysis and control mapping)
- Formal model diagrams and control failure matrices
- Comparative SaaS incident analysis
- Proposed shared-responsibility redesign framework
