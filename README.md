# Skeptical Moment Calculator (SMC)

A free, offline, logic‑based tool for individuals with schizophrenia who experience auditory hallucinations. It helps answer one critical question during moments of doubt:

> *"Is this voice real, or is it generated inside my head?"*

---

## Features

- ✅ **Zero dependencies** – pure HTML + CSS + JavaScript
- ✅ **Fully offline** – no internet required after download
- ✅ **Privacy‑first** – nothing is stored or transmitted
- ✅ **Instant response** – < 0.01 seconds per check
- ✅ **Free and open‑source** – no commercial intent
- ✅ **Extensible** – new fallacy patterns can be added easily

---

## How It Works

### 1. Classic Fallacy Interceptor
Detects common delusional reasoning patterns (e.g., the "Ako chain") and outputs a mathematical falsification report covering:
- **Fallacy of composition** (individual property ≠ group property)
- **Event substitution** (state vs. speech act – missing causal link)
- **Synchronised attack impossibility** (multi‑agent coordination probability ≈ 0)

### 2. Generic Reality‑Check Questions
If no classic pattern is matched, the system asks three simple yes/no questions:

| # | Question |
| :--- | :--- |
| 1 | Is the voice heard through **air‑vibration (ears)** or does it arise directly inside your head? |
| 2 | If someone else were beside you, **could they hear** it? |
| 3 | Does the content match **what you physically see right now**? |

Based on the answers, SMC calculates a **reality probability**:
- 0% → Logically certain hallucination – safe to ignore
- 33% → Suggest audio recording for verification
- 66% → Suggest checking with people nearby
- 100% → Trust your physical environment

### 3. Mandatory Physical Grounding
Every session ends with a tactile grounding task to shift attention away from auditory/language centres and break the cognitive loop.

---

## Requesting a Trial

The tool is currently in **v0.1** (core logic validated with simulated cases).  

**If you are a patient or a clinician and would like to try it**, you may request the single HTML file by opening an issue or contacting us via the method provided in this repository. The file will be sent **free of charge**, with no strings attached.

We do **not** actively promote or push this tool to anyone – we respect patient autonomy and clinical boundaries.

Feedback from real‑world use is welcome and will be used to refine future versions (v0.2 and beyond).

---

## Medical Disclaimer

> **This tool is a cognitive‑aid prototype, not a medical device.** It does **not** replace medication, psychotherapy, or professional diagnosis. Always consult with your attending physician before using any self‑management tool. The SMC is intended for **daily grounding practice** during stable periods only.

---

## Roadmap

| Version | Planned Improvements |
| :--- | :--- |
| v0.1 (current) | Core logic, Ako chain interceptor, 3‑question fallback, grounding action |
| v0.2 | Negation detection, "Quick Mode" for repeated use, multiple random grounding actions, anonymous usage count (no content stored) |
| v0.3 | Custom fallacy pattern editor (for clinicians to add patient‑specific delusions) |

---

## About the Project

The Skeptical Moment Calculator was built in ~4 hours as a **personal engineering exercise** – a response to the realisation that complex AI models (vector databases, sensor fusion) are often too slow, heavy, and privacy‑invasive for real‑world mental health support.

The design philosophy is simple:

> *When you're unsure, you don't need a black‑box AI. You need a transparent, deterministic, and verifiable process that you can trust.*

---

## License

MIT – free for personal and non‑commercial use.

---

**Last Updated**: 2026‑06‑27  
**Version**: v0.1 – ready for trial upon request