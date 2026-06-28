# The Hardest Part of Building a Mental Health Tool: Knowing Who NOT to Build For

_2026-06-28_

## The insight that changed everything

I spent the past day scraping Reddit for voice-hearing experiences to improve my calculator's fallacy pattern library. I got exactly what I asked for — and it scared me.

The voices I extracted are terrifying. Celebrities stalking. Chips implanted by doctors. Voices screaming that the patient killed someone. Demands to hurt themselves. Threats against their family.

These are real people. Their suffering is genuine. And they are absolutely, categorically the WRONG users for my tool.

## Who this tool is actually for

A patient in the grip of severe psychosis — the kind who hears voices commanding them to hurt themselves, who believes the doctor implanted a chip in their brain — will not use a logic calculator. They will either:

- Ignore it entirely
- Incorporate it into their delusion ("this tool was sent to monitor me")

My tool is not for them. They need medication, hospitalization, and professional psychiatric care. Nothing I build in a single HTML file can help someone in that state — and pretending otherwise would be dangerous.

The person I'm building for is different:

- They've been stabilized on medication
- They have insight into their condition (they know they sometimes hallucinate)
- They still have residual doubts — "was that real or a hallucination?"
- They need a quick, private, logic-based checkpoint to break the rumination cycle

This person exists. There are far more of them than the acute cases. And they are almost invisible in the data — because they don't post on crisis forums. They're quietly struggling, trying to get back to normal life, and every time a voice says something plausible, they lose a few hours to anxiety before they can dismiss it.

## The problem I now face

I went looking for training data to improve my calculator. What I found instead was a hard truth: **the most accessible data comes from the patients I shouldn't build for.**

The stabilized, self-aware patients — my actual users — rarely post their experiences publicly. Their voices aren't dramatic enough to become Reddit threads. They're mundane, insidious, and precisely because they sound plausible, they cause the most damage.

Example of what an acute patient hears: "You killed someone. The police are coming."

Example of what my target user hears: "Your coworker thinks you're incompetent. You saw the way she looked at you."

The first is obviously false to anyone with a grip on reality. The second? It could be true. And that ambiguity is exactly why a logic check is needed.

## What I'm doing about it

**1. Acknowledging the data gap.** I can't train my calculator on crisis posts. Those voices follow different patterns (grandiose, overtly violent, obviously impossible). My target user's voices are subtle, social, and sound plausible.

**2. Changing my search strategy.** Instead of r/schizophrenia and crisis forums, I'm now looking at:
- r/HearingVoices (a support network focused on living with voices, not crisis)
- Recovery-focused communities where people discuss managing residual symptoms
- First-person essays by people with schizophrenia who describe their daily management strategies

**3. Building a manual "calibration set."** I won't find a clean dataset. Instead, I'll work with a handful of people who match my user profile — stabilized, self-aware, willing to share examples of the mundane but distressing voices they still hear. Five people giving me ten examples each is worth more than 500 crisis posts I scraped from Reddit.

## The bigger lesson

I set out to build a logic checker. I'm learning that the hardest logic problem isn't in the code — it's in knowing who the tool is for, and having the discipline to NOT build for everyone else.

The same rule I apply to my demand intelligence pipeline applies here: **build for a specific person with a specific problem at a specific moment.** For the demand pipeline, that person is an indie hacker wondering if their idea is worth building. For this calculator, it's a stabilized patient who just heard something plausible and needs a 60-second logic check to break the anxiety spiral.

## Where I'm stuck

- Finding my real users is harder than I expected. They don't post on Reddit about their residual symptoms.
- The fallacy patterns I need to detect are more subtle than "the TV is talking to me." They're social, relational, and ambiguous.
- I might need to work directly with a mental health professional to understand what "plausible but false" voices sound like — and how to distinguish them from genuinely concerning social feedback.

## Next

- Leave the calculator publicly accessible. If stabilized patients or therapists find it useful and want to share feedback, they can open an issue on GitHub or email me. I'll read and incorporate suggestions when time allows.
- Continue refining the three-gate logic model, but accept that the rules will evolve slowly through real user feedback, not a one-time scrape of crisis posts.