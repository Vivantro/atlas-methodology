<div align="center">

<img src="./assets/cover-vivantro.png" alt="Vivantro — Innovation & Technologie" width="100%" />

# ATLAS

### A methodology for AI-augmented legacy modernization.

*Cellule legacy dediee — methodologie vivante et auto-apprenante, outillee par skills reutilisables.*

[![POC](https://img.shields.io/badge/POC-8%20completed-29B6E8?style=flat-square&labelColor=1C2847)](#proof-points)
[![Lines migrated](https://img.shields.io/badge/Source%20lines-~27%2C500-29B6E8?style=flat-square&labelColor=1C2847)](#proof-points)
[![Patterns covered](https://img.shields.io/badge/Patterns-48%20covered-29B6E8?style=flat-square&labelColor=1C2847)](#proof-points)
[![Live demos](https://img.shields.io/badge/Live%20demos-7-29B6E8?style=flat-square&labelColor=1C2847)](#live-demos)
[![Vivantro](https://img.shields.io/badge/by-Vivantro%20%C2%B7%20Access%20International-1C2847?style=flat-square)](https://github.com/Vivantro)

</div>

---

## What ATLAS is

ATLAS is the methodology our cellule legacy uses to modernize **COBOL**, **Delphi** and **BizTalk** systems toward modern stacks (TypeScript, .NET, Java, Python — on-prem or cloud), **augmented by AI** at every step.

It is **not** a tool you download and run. It is a **way of working** — 10 steps, 10 principles, a catalogue of pitfalls, and a fidelity audit baked into the delivery — that we apply across engagements.

This repository is the **public face** of ATLAS: what it does, what it has proven, and what we are willing to share. The full runbook stays with the team.

---

## The problem we address

> Two thirds of legacy modernization projects miss their deadline, exceed budget, or end up with a partial migration nobody wants to touch.

The reasons are well documented: missing knowledge of the source system, over-confident "lift and shift" tooling, no quantified fidelity check, no plan for the long tail of edge cases.

ATLAS takes those failure modes one by one and answers them with a sequenced, audited workflow.

---

## Methodology at a glance

ATLAS is **10 steps** organized in three phases. Each step has a clear deliverable, a risk it watches, and a verification gate before moving on.

### Phase 1 — Understand

| Step | What it produces |
|---|---|
| **E1** Inventory | Full source inventory: programs, copybooks, JCL, complexity classification |
| **E2** Discovery | Per-program deep analysis: business intent, integrations, data touchpoints |
| **E2b** Functional spec | Validated specification — readable by a non-technical stakeholder |
| **E2e** Existing-state capture | Screenshots, reports, transactions of reference, datasets — the *gold standard* of "what works today" |

### Phase 2 — Transform

| Step | What it produces |
|---|---|
| **E3** Scope & dependency map | Migration order, kill zones, infrastructure code excluded from rewrite |
| **E4** Target architecture | Stack mapping, target schema, ETL plan |
| **E5** Migration | Pattern-by-pattern translation, business logic preserved bit for bit |
| **E6** Fidelity audit | Source vs target, every discrepancy classified CRITICAL / ADAPTATION / COSMETIC |

### Phase 3 — Run

| Step | What it produces |
|---|---|
| **E7** Containerize & deploy | Container, CI, k8s manifests, healthcheck, smoke tests, browser-level validation |
| **Run & Evolve** | Production support, evolution backlog, knowledge handover playbook |

---

## Principles

Ten principles guide every engagement. They exist because each of them has a scar behind it.

1. **Capture the existing state before you migrate** — without a gold reference, you can't prove fidelity
2. **Migrate by functional block, not by file** — files are an artifact, business flows are the unit of value
3. **30% of legacy code is infrastructure** — don't translate it, replace it
4. **Code = 60% of the work, deploy + test = 40%** — budget accordingly
5. **Browser-level validation is mandatory before delivery** — API tests are not enough
6. **Every discordance is documented, classified, decided** — silence is the enemy
7. **Adaptations are deliberate, not accidental** — a platform improvement is OK, an unintentional drift is not
8. **One reference architecture per stack** — variance is the cost driver
9. **Capture knowledge in writing** — methodology compounds, undocumented learnings evaporate
10. **Enrich the methodology with external benchmarks** — at least once per quarter, test on a system we did not build

---

## Proof points

ATLAS has been validated on **8 public POCs** (~27,500 lines of COBOL, Delphi and BizTalk source) and **2 production-grade benchmarks** (anonymized, ~25,500 additional lines).

### POCs by stack

| # | Source | Domain | Source lines | Target | Ratio |
|---|---|---|---:|---|---:|
| 1 | COBOL (CLI) | Reporting | 209 | Python / Java | — |
| 3 | COBOL + CICS + VSAM | Credit card management | 7,650 | TypeScript (Cloudflare) | 7.4:1 |
| 4 | COBOL + CICS + DB2 | Core banking | 7,900 | TypeScript (Cloudflare) | 7.2:1 |
| 5 | COBOL + CICS + DB2 | Insurance policy | 3,211 | TypeScript (Cloudflare) | 3.8:1 |
| 6 | COBOL + IMS + VSAM ESDS/RRDS + JCL SORT | Auth & user mgmt | 1,624 | TypeScript (Cloudflare) | — |
| 7 | Delphi 5+ + Volga Tables | Invoicing (desktop) | 1,333 | TypeScript (Cloudflare) | — |
| 8 | COBOL | Sovereign tax calc | 5,225 | TypeScript (Cloudflare) | 6.2:1 |
| 9 | BizTalk + XSD + maps | Insurance integration | ~400 | TypeScript + Logic Apps Standard | 1.3:1 |

### Coverage

- **48 patterns** documented and migrated end-to-end (39 COBOL · 9 BizTalk)
- **44 discordances** identified across audits, **5 with business impact** (all resolved or accepted with client)
- **0 CRITICAL discordance** unresolved at delivery

### Production-grade validation

ATLAS was applied to **2 production benchmarks** of ~25,500 additional lines (anonymized for confidentiality). It held without methodology change at **x67 the volume** of the smallest POC. Three new pitfall candidates were added to the catalogue from these runs.

---

## Live demos

Every POC ships as a working application. You can interact with the migrated systems directly:

| POC | Live URL | Original source | Original license |
|---|---|---|---|
| Credit card management (CardDemo) | https://carddemo.vivantro.org | [aws-samples/aws-mainframe-modernization-carddemo](https://github.com/aws-samples/aws-mainframe-modernization-carddemo) | Apache 2.0 |
| Credit card extended (CardDemo Ext) | https://carddemo-ext.vivantro.org | same as CardDemo | Apache 2.0 |
| Core banking (CBSA) | https://cbsa.vivantro.org | [cicsdev/cics-banking-sample-application-cbsa](https://github.com/cicsdev/cics-banking-sample-application-cbsa) | EPL 2.0 |
| Insurance (GenApp) | https://genapp.vivantro.org | [cicsdev/cics-genapp](https://github.com/cicsdev/cics-genapp) | EPL 2.0 |
| Sovereign tax (DGFiP) | https://dgfip.vivantro.org | [gitlab.adullact.net/dgfip/taxe_fonciere](https://gitlab.adullact.net/dgfip/taxe_fonciere) | CeCILL v2.1 |
| Invoicing (Raptor — Delphi) | https://raptor.vivantro.org | [quartexNOR/RaptorInvoice](https://github.com/quartexNOR/RaptorInvoice) by Jon Lennart Aasenden | Apache 2.0 |
| Insurance integration (BizTalk) | https://biztalk.vivantro.org | [Azure/aimbiztalk](https://github.com/Azure/aimbiztalk) (Microsoft) | MIT |

### Migration sources we publish

For the three copyleft licenses (EPL 2.0, CeCILL v2.1) we publish the source of the migration alongside the live demo, in compliance with the original licenses' redistribution requirements:

- [Vivantro/poc-cbsa](https://github.com/Vivantro/poc-cbsa) — TypeScript port of CBSA (EPL 2.0)
- [Vivantro/poc-genapp](https://github.com/Vivantro/poc-genapp) — TypeScript port of GenApp (EPL 2.0)
- [Vivantro/poc-dgfip](https://github.com/Vivantro/poc-dgfip) — TypeScript port of DGFiP Taxe Fonciere (CeCILL v2.1)

For the four permissive licenses (Apache 2.0, MIT), the migrated code is not republished here — but each live demo carries a footer with the original source URL, the license, and our attribution. The original projects retain their copyright; our migration is documented work, not a fork.

---

## What's open · what's not

To keep both client trust and the methodology's commercial value, we publish in **three tiers**:

| Tier | What is here | What is **not** here |
|---|---|---|
| **Vitrine** (this repo) | Methodology overview, principles, proof points, live demos | The detailed runbook |
| **Teasers** (companion repos) | One discovery skill in *lite* form, generic pattern examples, public discordance catalogue | The full toolkit, the production patterns, the migrated code |
| **Reserved** | — | The 10 production skills, the 56 internal learnings, the 19 pitfalls, the migrated codebases, client-specific adaptations |

If you want to evaluate ATLAS for a real engagement, the right path is a **conversation**, not a download.

---

## Get in touch

| Region | Email | Site |
|---|---|---|
| 🇫🇷 France | [contact form](https://vivantro.org/#contact) | [vivantro.com](https://vivantro.com) |
| 🇹🇳 Tunisia | [contact form](https://vivantro.org/#contact) | [access-international.dev](https://access-international.dev) |

---

<div align="center">

<sub>© Vivantro · Access International — All rights reserved. Read freely; for commercial use, contact us.</sub>

</div>
