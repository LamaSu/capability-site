# capability-site

Marketing / onboarding product page for **PCC — the capability network** (capability.network).

Bright, editorial, de-scarified front door to an agent-native, two-sided capability marketplace.
The opposite of a terminal: type is the art, the CLI is the basement.

## Design

Composed from the **Controlled Chaos** design system (`~/.claude/skills/controlledchaos`) —
Monument + Swiss voices, motion choreography, and the three axioms (hierarchy / tension / time),
with a custom **`pcc` mood**:

| Token | Value | Role |
|-------|-------|------|
| `--bg` | `#FAFAF7` | warm paper-white base |
| `--fg` | `#0A0A0A` | ink |
| `--accent` | `#1B2BFF` | electric blue — primary, "Do things" |
| `--discord` | `#FF4D1C` | signal-orange — the one that doesn't belong, "Offer things" |

Hero direction: **Bold Statement (editorial)** — huge Space Grotesk headline, asymmetric Swiss grid,
animated capability-mesh, two color-blocked doors.

## Structure

- `index.html` — self-contained v1 (zero build, opens anywhere, instantly screenshot-able)

## Run / preview

```bash
# any static server
python -m http.server 4321
# then open http://localhost:4321
```

## Data spine (TODO before launch)

The page is a **demand sensor**. The `PCC.capture()` shim in `index.html` currently logs to console.
Drop your **PostHog** project key into the marked snippet to go live, and wire anonymous intent
capture from a real input — every intent typed (signed-up or not) is demand signal into PCC's
demand-intelligence layer.

Own the pixel + PostHog yourself; do not rent the content/hosting layer.

## Roadmap

1. **v1 (this):** self-contained editorial hero + live-demo + two-door onboarding + verified band.
2. **v2:** port to **Astro** (islands for the mesh + a real interactive intent bar), MDX content collections, deploy to Cloudflare Pages / Vercel.
3. **v3:** wire the real capability catalog + agent-connect + the "describe → agent scaffolds the kernel" operator flow.
