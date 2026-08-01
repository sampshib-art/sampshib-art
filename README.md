<!-- ==================================================================== -->
<!--                                                                      -->
<!--   DROP 3D PORTFOLIO GIF URL HERE                                     -->
<!--                                                                      -->
<!--   Paste the markdown link from the GitHub issue upload on the        -->
<!--   line directly below this block. It should look like:               -->
<!--   ![3d](https://github.com/user-attachments/assets/xxxxxxxx)         -->
<!--                                                                      -->
<!-- ==================================================================== -->

<!-- DROP 3D PORTFOLIO GIF URL HERE -->

# Sampanna Shibabhakti

**3D web designer and developer.** I build interactive 3D interfaces for the browser, and I'm just as interested in what runs underneath them.

`Kathmandu, Nepal` · `Three.js / React Three Fiber` · `Python systems work` · `open to hackathons`

<img src="https://img.shields.io/badge/-2ea44f?style=flat-square&label=tests%20passing&message=167&labelColor=14161a&color=2ea44f" alt="167 tests passing" />
<img src="https://img.shields.io/badge/stdlib%20only-6%20of%209%20repos-7C3AED?style=flat-square&labelColor=14161a" alt="6 of 9 repos are stdlib only" />
<img src="https://img.shields.io/github/last-commit/sampshib-art/Forge-StreamEngine?style=flat-square&labelColor=14161a&color=7C3AED&label=last%20push" alt="last push" />

---

## What I actually do

I pick a system I don't understand, rebuild a working version of it from scratch, and let the tests tell me where I was wrong.

That's the whole method. It's why the repos below have test counts instead of screenshots, and why each one ends with a short list of things that turned out to be harder than they looked.

- **3D web** — scroll-bound camera paths, procedural wireframe geometry, counter-rotating mesh systems, render budget treated as a design constraint.
- **Systems** — replication and quorum, event-time stream processing, authorisation, declarative provisioning, compliance tooling.
- **Full-stack** — Next.js and TypeScript on the front, Python and FastAPI behind it.

---

## Live

| | |
| :--- | :--- |
| **[pranishstore1.netlify.app](https://pranishstore1.netlify.app/)** | Custom e-commerce storefront for a Kathmandu electronics retailer. Next.js App Router, category and sub-category routing, product detail pages, scroll-driven motion. Built from scratch, no template. |
| **[sampuu.netlify.app](https://sampuu.netlify.app/)** | Front-end study rebuilding the interaction model of `unseen.co` — WebGL canvas, drag-to-explore scene, audio toggle. Recreation for study; original design and theme code belong to unseen.co. |

---

## Forge — nine standalone builds

Six are pure-stdlib Python with **no runtime dependencies**. Clone, run `python -m <package>`, run `pytest`. Nothing to install.

| Repo | What it does | Verified |
| :--- | :--- | :--- |
| **[Forge-StreamEngine](https://github.com/sampshib-art/Forge-StreamEngine)** | Event-time stream analytics — tumbling and sliding windows, VWAP, rolling sigma anomaly detection | `45 tests` |
| **[Forge-ZeroTrust](https://github.com/sampshib-art/Forge-ZeroTrust)** | Zero-trust gateway — HMAC capability tokens with replay protection, deny-by-default policy engine | `27 tests` |
| **[Forge-Governance](https://github.com/sampshib-art/Forge-Governance)** | Config compliance auditing — severity-weighted controls, remediation output, CI exit codes | `26 tests` |
| **[Forge-Replica](https://github.com/sampshib-art/Forge-Replica)** | Leader/follower replication — quorum commit, log-shipping catch-up, split-brain-safe failover | `25 tests` |
| **[Forge-Provision](https://github.com/sampshib-art/Forge-Provision)** | Declarative provisioning — plan/apply/converge, content-hashed drift detection, dependency ordering | `25 tests` |
| **[Forge-Microfront](https://github.com/sampshib-art/Forge-Microfront)** | Micro-frontend composition — per-fragment timeout budgets, graceful fallbacks, TTL caching | `19 tests` |
| **[Forge-AgritechNode](https://github.com/sampshib-art/Forge-AgritechNode)** | IoT telemetry node — FastAPI over Server-Sent Events, RP2040 firmware, mock-hardware fallback | `SSE stream verified` |
| **[Forge-Fulfillment](https://github.com/sampshib-art/Forge-Fulfillment)** | Order fulfillment core — HMAC-verified ingress, bounded async queue, atomic SQLite stock and audit writes | `end-to-end verified` |
| **[Forge-Sentinel](https://github.com/sampshib-art/Forge-Sentinel)** | Host threat-intel daemon — socket scanning, failed-auth windowing, local LLM triage with offline fallback | `detection path verified` |

---

## Three things these got wrong first

The bugs are the interesting part, so they're documented rather than quietly fixed.

**Half-open windows are a real decision, not a detail.**
A sliding window of span `S` ending at `t` covers `(t-S, t]`, not `[t-S, t]`. A tick exactly `S` old has aged out. My first test asserted the opposite; the implementation was right and the test was wrong. It's now pinned in both directions.

**An unset compliance control is not a passing control.**
A checker that reads a missing field as falsy and reports "compliant" is worse than no checker, because it manufactures false assurance. `Forge-Governance` reports a third state — `skip` — and excludes it from the compliance denominator, so an empty config scores 0%, not 100%.

**Text-mode writes break content-hash drift detection on Windows.**
`Path.write_text` translates `\n` to `\r\n`, so the bytes on disk stop matching the hashed content and every multi-line file reports as drifted forever. The unit tests missed it entirely — it only showed up when the demo printed `converged: False` after a successful apply.

---

## Stack

<img src="https://img.shields.io/badge/Three.js-14161a?style=flat-square&logo=three.js&logoColor=white" alt="Three.js" />
<img src="https://img.shields.io/badge/React_Three_Fiber-14161a?style=flat-square&logo=react&logoColor=61DAFB" alt="React Three Fiber" />
<img src="https://img.shields.io/badge/WebGL-14161a?style=flat-square&logo=webgl&logoColor=990000" alt="WebGL" />
<img src="https://img.shields.io/badge/TypeScript-14161a?style=flat-square&logo=typescript&logoColor=3178C6" alt="TypeScript" />
<img src="https://img.shields.io/badge/React-14161a?style=flat-square&logo=react&logoColor=61DAFB" alt="React" />
<img src="https://img.shields.io/badge/Next.js-14161a?style=flat-square&logo=nextdotjs&logoColor=white" alt="Next.js" />
<img src="https://img.shields.io/badge/Tailwind-14161a?style=flat-square&logo=tailwindcss&logoColor=38BDF8" alt="Tailwind CSS" />
<img src="https://img.shields.io/badge/Python-14161a?style=flat-square&logo=python&logoColor=FFD43B" alt="Python" />
<img src="https://img.shields.io/badge/FastAPI-14161a?style=flat-square&logo=fastapi&logoColor=009688" alt="FastAPI" />
<img src="https://img.shields.io/badge/SQLite-14161a?style=flat-square&logo=sqlite&logoColor=003B57" alt="SQLite" />
<img src="https://img.shields.io/badge/MicroPython-14161a?style=flat-square&logo=micropython&logoColor=white" alt="MicroPython" />
<img src="https://img.shields.io/badge/Linux-14161a?style=flat-square&logo=linux&logoColor=FCC624" alt="Linux" />

<!--
  STATS CARDS - currently disabled, ready to switch on.

  github-readme-stats.vercel.app is returning HTTP 503 for every username,
  verified against anuraghazra and torvalds as well as this account. It is
  an instance-wide outage, not a caching problem. Enabling these today
  renders two broken images.

  Check whether it is back:
    curl -sI "https://github-readme-stats.vercel.app/api?username=sampshib-art"

  Once that returns 200, delete the opening and closing comment markers
  around the two lines below and they go live exactly as written.

  ![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=sampshib-art&layout=compact&theme=dark&v=1)
  ![GitHub Stats](https://github-readme-stats.vercel.app/api?username=sampshib-art&show_icons=true&theme=dark&hide=stars,issues&v=1)
-->

---

## Contact

<a href="https://www.linkedin.com/in/sampanna-s-8057343b9/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
<a href="mailto:sampshib@gmail.com"><img src="https://img.shields.io/badge/Email-14161a?style=flat-square&logo=gmail&logoColor=EA4335" alt="Email" /></a>
<a href="https://sampuu.netlify.app/"><img src="https://img.shields.io/badge/Portfolio-14161a?style=flat-square&logo=vercel&logoColor=white" alt="Portfolio" /></a>
