# Skeptical Moment Calculator (SMC) – Engineering Build Log

**Project Type**: Pure front‑end offline tool (single HTML file)  
**Build Time**: ~4 hours  
**Current Status**: Core logic loop complete; awaiting real‑world validation

---

## 1. The Problem I Am Solving

Patients with schizophrenia often experience moments during stable phases when **a voice or thought arises, and they cannot tell whether it is actually spoken by someone else or generated internally.**

Traditional reassurance ("Don't be afraid, it's just a hallucination") lacks persuasive power. The patient needs **an operational, deterministic verification process** – as simple as using a calculator: input → compute → get a result.

**Atomic closed‑loop**: type the text → automatic logical judgement → falsification report → one physical grounding action → reset.

---

## 2. Key Design Branch Points

### Option A (abandoned): AI vector matching
- Use `sentence‑transformers` for semantic similarity
- Result: model loading takes 8 seconds, memory >1.2GB, patient's device cannot run it
- **Realisation**: pursuing "intelligence" sacrificed usability – wrong direction

### Option B (abandoned): real‑time audio + sensors
- Use microphone for ambient sound, accelerometer for activity detection
- Result: passive monitoring increases patient anxiety, hardware integration is extremely complex
- **Realisation**: the tool should comfort the patient, not monitor them

### Option C (finally adopted): pure rule‑based engine
- Input is text, output is a logical analysis
- Dependencies: **0** (pure HTML + CSS + JS)
- Response time: **< 0.01 s**
- Privacy: **fully offline**, nothing is uploaded
- **Conclusion**: when a tool is simple and transparent enough, patients are willing to trust it.

---

## 3. Core Structure of the Logic Engine

### Layer 1: Classic Fallacy Interceptor (hard‑coded)

The **Ako chain** – described by the patient themselves – is the first classic pattern stored:

> Ako graduated from School A → Ako is low‑quality → School A is low‑quality → Ako said bad things about School A → everyone at School A shouts at Ako in the dormitory

**Trigger conditions** (all four categories must be present simultaneously):
- Belonging: graduated / from / belongs to
- Negative attribute: low‑quality / sick / shameful
- Group: school / company / everyone
- Aggressive action: shout at / speak ill of / target

**Once triggered, output three mathematical falsifications**:
1. **Fallacy of composition**: individual quality ≠ group quality; no data exist for the other members.
2. **Event substitution**: a "state judgment" is replaced by a "speech act"; the physical event "opening the mouth to speak" is missing from the causal chain.
3. **Synchronised attack impossibility**: hundreds of people shouting at the same time and place → probability ≈ 0.

### Layer 2: Generic Fallback Logic (Three Reality Questions)

If the input does not match any classic pattern, the system automatically displays three **yes/no** buttons:

| # | Question | Reality Variable |
| :--- | :--- | :--- |
| 1 | Is this voice heard through **air‑vibration sensed by your ears**, or does it arise directly inside your head? | Physical sound source |
| 2 | If someone else were beside you, **could they hear** it? | External verifiability |
| 3 | Does the content match **what you physically see with your eyes right now**? (e.g., it says rain, but outside is sunny) | Multimodal consistency |

**Decision rules**:
- All three "No" → reality probability **0%** → output: "Logically certain to be a hallucination; can be safely ignored."
- Exactly 1 "Yes" → 33% → suggest audio recording for verification
- Exactly 2 "Yes" → 66% → suggest checking with people nearby
- 3 "Yes" → 100% → trust the physical environment

### Layer 3: Mandatory Physical Grounding (single action)

Regardless of which path is taken, the report ends with:

> **Place your palm flat on the desk or wall, press firmly for 5 seconds, feel the temperature and hardness, then click 'Done'.**

Rationale: tactile stimulation shifts attention away from auditory/language centres and breaks the cognitive loop.

---

## 4. Ako Chain Live Test

**Input**:
> "I am Ako, I graduated from School A and now study at School B. Yesterday I heard someone say I am low‑quality. This morning I heard everyone from School A shouting at me in the dormitory, because they mistook 'Ako is low‑quality' for 'Ako said bad things about School A'."

**System behavior**:
- Matched `FP_001_AKO`
- Response time: `< 0.01 s`
- Directly output the three‑step falsification report (skipped the three questions)
- Displayed the grounding task

**Conclusion**: ✅ Passed. The subtle substitution from "low‑quality" to "said bad things about School A" was precisely identified.

---

## 5. Current Limitations (v0.1 Known Issues)

| Issue | Impact | Planned Fix |
| :--- | :--- | :--- |
| Keyword‑AND matching may falsely trigger on negated sentences (e.g., "I am *not* low‑quality") | False positive | v0.2: add negation detection |
| Repeated use of the three‑question mode causes fatigue | Decreased user experience | v0.2: add "Quick Mode" to reuse last answers |
| Only one grounding action | Novelty decreases over time | v0.2: randomise among 3‑5 different actions |
| No usage statistics | Cannot assess effectiveness | v0.2: store only usage count (no content) |

---

## 6. Deliverables

- **Source code**: `skeptical-moment-calculator.html` (single file, ~140 lines, with comments)
- **User instructions**: oral explanation suffices (three steps: type → read report → press and confirm)
- **This log**: build record archive

---

## 7. Next Steps

1. **If a patient or their attending physician proactively requests a trial**, the HTML file may be provided free of charge, and feedback will be collected. (No active promotion to any individual or institution; the patient's autonomy and clinical boundaries are fully respected.)
2. After collecting sufficient feedback (estimated 3‑5 valid responses), adjust thresholds and keyword lists for v0.2.
3. Keep the tool open‑source / free; no commercialization efforts will be pursued.

---

**Log Archive Date**: 2026‑06‑27
**Document Status**: Draft finalized; ready for execution