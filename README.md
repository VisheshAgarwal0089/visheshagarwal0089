# Vishesh Agarwal

**Software engineering student · builder · exploring what sits below the abstraction layer**

I build practical systems, then trace them downward: product logic → runtime behavior → backend control → data consistency → protocols → infrastructure.

<p align="center">
  <img src="./assets/depth-map.svg" alt="Vishesh Agarwal computing depth map" width="100%" />
</p>

---

## /currently

```text
studying      operating systems · computer networks · backend internals
building      browser tooling · reconciliation systems · automation
practising    Java DSA · SQL · system-oriented debugging
exploring     distributed systems · database internals · protocols
```

The distinction matters: the projects below are verified builds; the deeper systems topics are the direction I am actively moving into.

---

## /systems

### [SettleWise AI](https://github.com/VisheshAgarwal0089/settlewise_ai)

Verification-first settlement reconciliation system for synthetic Razorpay-format data.

```text
React/Vite client
      ↓
Express API
      ↓
candidate scoring + hard safety gates
      ↓
SQLite-backed reconciliation state
      ↓
human review + audit hash chain
```

What is technically interesting:

- deterministic 150-order evaluation batch
- exact-ID / receipt / amount-date candidate matching
- hard gates for amount, date, ambiguity, and prior links
- integer-paise financial calculations
- transactional approve / reject / manual-link review actions
- append-only SHA-256 audit chain
- Razorpay adapter with atomic CSV fallback
- optional AI explanations kept outside the authoritative matching path
- React 19 + Express 5 + SQLite, deployed through Vercel and Railway

Verified canonical evaluation:

| signal | result |
|---|---:|
| automatic matches | 123 / 146 pairable |
| known-pair recall | 84.25% |
| precision | 100% |
| false positives | 0 |
| exception recall | 90% |
| non-automatic records surfaced | 27 / 27 |
| matching duration | 140 ms |

The lower recall is deliberate: safety gates reject unsafe automatic links rather than optimizing for a prettier metric.

---

### [LeetGitSync](https://github.com/VisheshAgarwal0089/leetgitsync)

A browser extension that captures accepted LeetCode submissions and writes them directly into GitHub without a separate backend.

```text
LeetCode page
    ↓
MAIN-world capture
    ↓
isolated content script
    ↓
MV3 background worker
    ↓
persistent retry queue
    ↓
GitHub REST API
    ↓
solution file + managed README index
```

Implementation characteristics:

- JavaScript + React + WXT
- Manifest V3
- browser extension storage for configuration and queue state
- GitHub Device Flow
- deterministic solution paths
- SHA-aware GitHub file updates
- duplicate protection and retry handling
- managed README generation
- Brave / Chrome / Edge / Firefox builds
- automated checks for manifests, runtime assumptions, release state, and sensitive data
- test coverage split across capture, queue, GitHub writer, README generation, and foundation behavior

The generated [leetcode_problems](https://github.com/VisheshAgarwal0089/leetcode_problems) repository is the output surface: Java and SQL solutions are indexed automatically by topic.

---

### [CertiSync / CredVault blueprint](https://github.com/VisheshAgarwal0089/CredVault-AI-Powered-Certificate-Deduplicator-Repo-Streamliner)

An architecture/design blueprint for a local credential archiver and deduplication tool.

Current repository state: **design documentation, not a completed implementation**.

The proposed pipeline combines:

```text
filesystem watcher
      ↓
PDF parser / OCR
      ↓
perceptual hashing + normalized text
      ↓
SQLite ledger
      ↓
categorization
      ↓
GitHub sync
```

The interesting part is the duplicate-detection boundary: filenames are treated as weak evidence, while visual fingerprints and normalized document content become stronger signals.

---

## /below_the_abstraction

I do not treat this as a list of mastered subjects.

| layer | using now | actively deepening |
|---|---|---|
| Application | React, Vite, Node.js, Express | system boundaries, failure modes |
| Browser runtime | MV3, content scripts, workers, local storage | browser internals, event lifecycles |
| Data | SQLite, SQL, MongoDB | transactions, indexes, consistency |
| Network | HTTP APIs, CORS, auth flows | DNS, TLS, sockets, proxies |
| OS / environment | Linux, processes, ports, deployment | memory, filesystems, scheduling |
| Infrastructure | Vercel, Railway, AWS/GCP labs | distributed systems, queues, observability |

The goal is to keep moving downward until abstractions stop feeling magical.

---

## /engineering_notes

Topics already visible in the repositories or current study path:

- reconciliation scoring, ambiguity and false-negative diagnostics
- auditability and tamper-evident state
- browser-extension architecture
- MAIN-world vs isolated-world communication
- background workers and persistent retries
- atomic-ish GitHub content updates using blob SHAs
- local-first / browser-only processing boundaries
- HTTP, DNS, reverse proxies, ports, Linux and deployment flows
- SQL, indexing, transactions and database fundamentals
- dynamic programming, graphs, trees, segment trees, sliding window and backtracking

The [Interview_DS_Algo](https://github.com/VisheshAgarwal0089/Interview_DS_Algo) and [leetcode_problems](https://github.com/VisheshAgarwal0089/leetcode_problems) repositories are the algorithm/practice side of that work.

---

## /stack

```text
languages       Java · JavaScript · Python · SQL
frontend        React · Vite · HTML/CSS
backend         Node.js · Express
data            SQLite · MongoDB · Pandas · NumPy
ml              scikit-learn · TensorFlow · PyTorch
browser/tooling WXT · Manifest V3 · GitHub REST API
infra           Linux · Git · Vercel · Railway · AWS · GCP
analytics       Power BI · Excel
```

Technologies are listed by where they are actually used, not as a logo wall.

---

## /other_signal

- [Labs-Solutions](https://github.com/VisheshAgarwal0089/Labs-Solutions) — large Google Cloud / Linux / security / networking lab archive
- [Excel_project](https://github.com/VisheshAgarwal0089/Excel_project) — Excel dashboard and data-cleaning work
- [Certifications](https://github.com/VisheshAgarwal0089/Certifications) — certification archive
- [frontpage](https://github.com/VisheshAgarwal0089/frontpage) — older Django-based project
- [Web-Calculator](https://github.com/VisheshAgarwal0089/Web-Calculator) — early frontend build

Older and empty repositories are intentionally not treated as flagship work.

---

## /links

[LinkedIn](https://www.linkedin.com/in/visheshagarwal0089/) ·
[LeetCode](https://leetcode.com/u/visheshaga0089/) ·
[Codolio](https://codolio.com/profile/vishesh0089)

```text
build()
trace()
break_assumptions()
understand()
repeat()
```
