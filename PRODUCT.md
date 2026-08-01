# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

Primary: **hackathon selection judges**, scanning many candidate profiles under time pressure — on the order of a minute per candidate, many tabs open — and making a single binary decision: advance or pass.

Secondary (unconfirmed priority): recruiters and prospective freelance clients reaching the same page through a different route. Design decisions resolve in favour of the judge when the two conflict.

## Product Purpose

The GitHub profile README at `sampshib-art/sampshib-art` is the landing surface for Sampanna Shibabhakti's engineering work. Success is narrow and measurable: a judge who lands on it reaches "this person can build" before they leave. It is not a documentation page, a CV, or a portfolio site — it is the thing that buys those a second look.

## Positioning

The differentiator is **verifiable work, not claims**. Nine standalone repositories, six of them pure-stdlib Python that a judge can clone and run with no install step, carrying 167 tests that actually pass. Most profiles at this level assert competence; this one can be checked in under a minute. That is the position a neighbouring profile cannot truthfully copy without doing the same work.

## Operating Context

- Read inside GitHub's own README renderer, not a browser page the author controls.
- **GitHub sanitises all styling.** `style`, `class`, and `<style>` are stripped. No CSS, no shadows, no transforms, no rounded corners, no custom fonts. Layout is achievable only through HTML tables, alignment attributes, images, and Markdown.
- All images pass through GitHub's camo proxy, which re-encodes SVGs and frequently drops in-SVG SMIL/CSS animation.
- Read on desktop and mobile; GitHub's mobile renderer collapses multi-column tables into stacked cells.
- Third-party badge and widget APIs are a live failure surface. Verified this session: `profile-counter.glitch.me` returns 410 Gone (permanent), `github-readme-stats.vercel.app` returns 503 for every username including its own author.

## Capabilities and Constraints

- Repository contains exactly two files: `README.md` and `demo.gif`. No build step, no components, no tokens.
- `demo.gif` is a 3.10 MB screen recording of the Pranish Store storefront, converted from an H.264 MP4 to GIF89a at 640×378, 10fps, 64-colour palette. It shows a Next.js storefront, **not** 3D or WebGL work.
- No recording of the React Three Fiber scene exists yet. The scene itself is real and lives in `Project-1-week-` (now archived on GitHub).
- Self-hosted assets: the hero GIF only. Every other image is a third-party dependency that can fail independently.
- Author identity for commits: Sampanna Shibabhakti <sampshib@gmail.com>.

## Brand Commitments

- Name: Sampanna Shibabhakti. GitHub handle: `sampshib-art`.
- The nine standalone builds are branded with a `Forge-` prefix. `Forge` is a naming convention for personal builds — **not** a company, organisation, team, or product suite, and must never be presented as one.
- Voice: concise, pragmatic, technical. Explicitly banned: "delve", "symphony", "cutting-edge", "testament to", and comparable filler. Bullet-dense over prose-dense.

## Evidence on Hand

Real and verified:

- Nine public repositories under `sampshib-art`, all pushed and live.
- **167 passing tests**, verified by running `pytest`: StreamEngine 45, ZeroTrust 27, Governance 26, Replica 25, Provision 25, Microfront 19.
- Three further builds verified by execution rather than test suite: AgritechNode (SSE stream), Fulfillment (end-to-end order → stock decrement → audit row), Sentinel (detection path with LLM-offline fallback).
- `pranishstore1.netlify.app` — live custom Next.js storefront built for a Kathmandu electronics retailer. Bundle inspection confirms **no Three.js or WebGL**; it is a 2D storefront with `requestAnimationFrame` motion.
- `sampuu.netlify.app` — live, contains genuine Three.js/WebGL, **but serves unseen.co's compiled WordPress theme**. Verified: 19 of 19 sampled 300-character slices of unseen.co's `theme.js` appear verbatim. Must always be described as a study or recreation, never as original design work.
- Original React Three Fiber code in `Project-1-week-/src/components/WebGLBackground.tsx` — scroll-bound camera path, counter-rotating mesh layers, eight orbiting low-poly nodes. This is the author's genuine 3D work.
- Location: Kathmandu, Nepal.

Absences future work must not paper over: no stars, no forks, no external contributors, no employment history, no testimonials, no client roster beyond the one storefront, no published metrics. The GitHub account is weeks old and its aggregate statistics are correspondingly low.

## Product Principles

1. **Checkable beats impressive.** Every claim on the surface should be verifiable by a judge in under a minute. Prefer a number that survives clicking through to an adjective that does not.
2. **Never inflate.** No invented titles, roles, founder or club affiliations, testimonials, or metrics. An accurate modest claim outperforms an inflated one that a judge can disprove from view-source.
3. **The proof is the product.** The nine repositories and their test counts are the strongest asset. Surface strategy is judged by whether that evidence reaches the visitor, not by whether the page looks tidy.
4. **Assume hostile infrastructure.** Any third-party image API may be down or permanently retired. Prefer self-hosted or verified-live assets; never ship a URL that has not returned 200.
5. **Match the claim to the artifact.** Stated identity must match what the page can actually show. Claiming 3D while displaying a 2D storefront is a defect, not a stretch.

## Accessibility & Inclusion

No product-specific standard established. Baseline obligation: every image carries meaningful `alt` text, since the surface is image-dense and GitHub offers no other fallback.
