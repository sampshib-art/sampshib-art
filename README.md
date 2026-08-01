<img
  src="https://capsule-render.vercel.app/api?type=waving&color=0:1a1a2e,100:16213e&height=180&section=header&text=Sampanna%20Shibabhakti&fontSize=42&fontColor=ffffff&desc=3D%20Web%20%7C%20Systems%20%7C%20Full-Stack&descSize=16&descAlignY=62"
  width="100%"
  alt="Sampanna Shibabhakti"
/>

<p align="center">
  <img
    src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=20&pause=1000&color=7C3AED&center=true&vCenter=true&width=560&lines=3D+Web+Designer+%26+Developer;Systems+%26+Backend+Engineering;Kathmandu%2C+Nepal"
    alt="3D Web Designer and Developer, Systems and Backend Engineering"
  />
</p>

<!-- TODO: Insert GIF of WebGLBackground.tsx here (Width: 100%) -->

---

## 👋 About

I build interactive 3D interfaces for the browser, and I'm just as interested in what runs underneath them.

- **3D web** — Three.js and React Three Fiber. Scroll-bound camera paths, procedural geometry, counter-rotating mesh systems.
- **Systems and backend** — replication and consensus, stream processing, authorisation, provisioning, compliance tooling. Mostly Python, mostly built from scratch to understand how the real thing works.
- **How I work** — I pick a system I don't understand, rebuild a working version of it, and let the tests tell me where I was wrong. Several of the design notes in these repos are things I got wrong first.
- Based in Kathmandu, Nepal. Open to hackathons and 3D web work.

---

## 🧰 Toolkit

<p align="center">
  <img src="https://skillicons.dev/icons?i=threejs,webgl,react,nextjs,ts,tailwind&theme=dark" alt="3D and frontend stack" />
</p>
<p align="center">
  <img src="https://skillicons.dev/icons?i=python,fastapi,nodejs,sqlite,git,linux&theme=dark" alt="Backend and tooling stack" />
</p>

---

## 🌐 Live

| Site | What it is |
| :--- | :--- |
| **[pranishstore1.netlify.app](https://pranishstore1.netlify.app/)** | Custom e-commerce storefront for a Kathmandu electronics retailer. Next.js App Router, category and sub-category routing, product detail pages, scroll-driven motion. Built from scratch, no template. |
| **[sampuu.netlify.app](https://sampuu.netlify.app/)** | Front-end study rebuilding the interaction model of `unseen.co` — WebGL canvas, drag-to-explore scene, audio toggle. Recreation for study; original design and theme code belong to unseen.co. |

---

## 🔩 Forge

Nine standalone builds. The six with a test count are pure-stdlib Python with no runtime dependencies — clone and run.

| Repo | What it does | Verified |
| :--- | :--- | :--- |
| **[Forge-StreamEngine](https://github.com/sampshib-art/Forge-StreamEngine)** | Event-time stream analytics. Tumbling and sliding windows, VWAP, rolling sigma anomaly detection. | 45 tests |
| **[Forge-ZeroTrust](https://github.com/sampshib-art/Forge-ZeroTrust)** | Zero-trust gateway. HMAC capability tokens with replay protection, deny-by-default policy engine. | 27 tests |
| **[Forge-Governance](https://github.com/sampshib-art/Forge-Governance)** | Config compliance auditing. Severity-weighted controls, remediation output, CI exit codes. | 26 tests |
| **[Forge-Replica](https://github.com/sampshib-art/Forge-Replica)** | Leader/follower replication. Quorum commit, log-shipping catch-up, split-brain-safe failover. | 25 tests |
| **[Forge-Provision](https://github.com/sampshib-art/Forge-Provision)** | Declarative provisioning. Plan/apply/converge, content-hashed drift detection, dependency ordering. | 25 tests |
| **[Forge-Microfront](https://github.com/sampshib-art/Forge-Microfront)** | Micro-frontend composition. Per-fragment timeout budgets, graceful fallbacks, TTL caching. | 19 tests |
| **[Forge-AgritechNode](https://github.com/sampshib-art/Forge-AgritechNode)** | IoT telemetry node. FastAPI over Server-Sent Events, RP2040 MicroPython firmware, mock-hardware fallback. | SSE stream verified |
| **[Forge-Fulfillment](https://github.com/sampshib-art/Forge-Fulfillment)** | Order fulfillment core. HMAC-verified ingress, bounded async queue, atomic SQLite stock and audit writes. | End-to-end verified |
| **[Forge-Sentinel](https://github.com/sampshib-art/Forge-Sentinel)** | Host threat-intel daemon. Socket scanning, failed-auth windowing, local LLM triage with offline fallback. | Detection path verified |

A few things these turned up that are worth more than the code:

- Sliding windows need an explicitly documented boundary. `(t-span, t]` versus `[t-span, t]` is a real behavioural difference, and a test should pin it in both directions.
- An unset compliance control is not a passing control. Scoring a missing field as compliant manufactures false assurance, so `Forge-Governance` reports it as a third state and excludes it from the denominator.
- Text-mode file writes translate `\n` to `\r\n` on Windows, so content-hash drift detection never converges. Found by running the demo, not by the tests.

---

## 📊 Stats

<p align="center">
  <img
    height="200em"
    src="https://github-profile-summary-cards.vercel.app/api/cards/stats?username=sampshib-art&theme=radical"
    alt="GitHub stats"
  />
  <img
    height="200em"
    src="https://github-profile-summary-cards.vercel.app/api/cards/repos-per-language?username=sampshib-art&theme=radical"
    alt="Most used languages"
  />
</p>

---

## 🤝 Connect

<p align="center">
  <a href="https://www.linkedin.com/in/sampanna-s-8057343b9/" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
  </a>
  <a href="mailto:sampshib@gmail.com">
    <img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" />
  </a>
  <a href="https://sampuu.netlify.app/" target="_blank">
    <img src="https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=vercel&logoColor=white" alt="Portfolio" />
  </a>
</p>
