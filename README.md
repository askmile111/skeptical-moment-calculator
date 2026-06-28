# Skeptical Moment Calculator

A free, offline, logic-based tool for individuals recovering from schizophrenia who still experience residual auditory hallucinations. It helps answer one question during moments of doubt:

> *"Is this voice real, or is it a hallucination?"*

**Who this is for:** People who have been stabilized on medication, have insight into their condition, and need a quick logic checkpoint to break the rumination cycle. Not for acute crisis.

---

## Features

- ✅ **Zero dependencies** – pure HTML + CSS + JavaScript
- ✅ **Fully offline** – no internet required after download
- ✅ **Privacy-first** – nothing is stored or transmitted
- ✅ **Instant response** – < 0.01 seconds per check
- ✅ **Free and open-source** – no commercial intent
- ✅ **Extensible** – new fallacy patterns can be added easily

---

## How It Works

The tool analyzes the text you paste in — no questions, no interactions, no judgments. It checks for two types of logical flaws:

### 1. False Cause-Effect Chains
Detects when a voice claims that one thing causes another, but no physical causal link exists. For example:

- "He glanced at me → therefore he knows my secrets" (appearance cannot reveal thoughts)
- "The TV is talking about me" (public broadcast cannot target an individual)
- "One person said something → therefore everyone is against me" (individual ≠ group)

### 2. Sourceless Accusations
Detects when a voice makes a claim about someone harming or watching you, but you never describe how you learned this information. If there's no sensory source (heard, saw, someone told), the information likely originated internally.

### 3. Physical Grounding Prompt
After the logic check, the tool suggests a simple grounding action: press your hand against a solid surface and feel its hardness. This shifts attention away from auditory processing and helps break the cognitive loop.

---

## Requesting a Trial

The tool is currently in **v0.1** (core logic validated with limited test cases).

**If you are a stabilized patient or a clinician and would like to try it**, the HTML file is available in this repository. Simply download `index.html` and open it in any browser. No installation. No internet. No strings attached.

We do **not** actively recruit users or push this tool on anyone. It sits here. If someone finds it useful, they're welcome to use it.

Feedback is welcome via GitHub Issues, but there is no response timeline. This is a public-good project, not a startup.

---

## Medical Disclaimer

> **This tool is a cognitive aid, not a medical device.** It does **not** replace medication, psychotherapy, or professional diagnosis. Always consult with your attending physician. It is intended for daily grounding practice during stable periods only. If you are in crisis, contact your doctor or emergency services immediately.

---

## Roadmap

| Version | Planned Improvements |
| :--- | :--- |
| v0.1 (current) | False cause-effect detection, sourceless accusation detection, grounding prompt |
| v0.2 | More fallacy patterns from user-submitted examples, improved negation handling, multiple random grounding actions |
| v0.3 | Custom fallacy pattern editor (for clinicians to add patient-specific patterns) |

*No timeline. Updates happen when they happen.*

---

## About the Project

Built in a few hours as a personal engineering exercise. The design philosophy:

> *When you're unsure whether a voice is real, you don't need a black-box AI. You need a transparent, deterministic process you can trust — and that runs entirely on your own device.*

---

## License

MIT

---

**Last Updated**: 2026-06-28
**Version**: v0.1