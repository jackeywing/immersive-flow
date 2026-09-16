# “They Understood You” · 15-Second Interactive Ad
### Roundtable script (3 hosts) · Duolingo membership trial
**Scenario: English native speaker learning French** — UI copy in English, learning content in French.

---

## 1. Concept

**Format**: a three-character roundtable (the NotebookLM Audio Overview feel). The learner is not the
audience — they're the **fourth participant**. They speak; the characters answer.

**Core mechanic**: the product's "peak moment" is moved *into the ad*.
> Before being asked to pay, the learner experiences saying something real — and being understood.

**The emotional pivot (the one design decision that matters)**:
the praise comes from the character **least likely to give it**.
Lily saying "I understood you" beats any character saying "amazing."
**Approval from someone hard to impress is the strongest social proof there is.**

---

## 2. Casting & personality calibration

| Character | Personality | Function in the ad | Voice treatment |
|---|---|---|---|
| **Duo** | Official mascot. Relentless cheerleader, slightly over the top. | Opens, closes, delivers the CTA (brand voice) | Bright, fast, **+20%** rate |
| **Lily** | Purple-haired deadpan teen. Flat affect, rarely praises, secretly cares. | **Emotional pivot** — her approval is the highest compliment | Slow **−8%**, pitch **−4Hz**, leading pause |
| **Zari** | Outgoing, effusive, high-energy social butterfly. | Pushes the emotion up | **+26%**, pitch **+4Hz** |
| (Learner) | The user | Interaction beat: says the line from their current unit | French native voice (demo) |

**Why these three**: three energy registers — **eager (Duo) × flat (Lily) × explosive (Zari)**.
The bigger the contrast, the more weight Lily's line carries.

---

## 3. Shot-by-shot script

| Time | Speaker | Line | Delivery / visual |
|---|---|---|---|
| 0.00–2.9 | **Duo** | "Hey! Say something from the unit you're learning." | Eager, fast. Three avatars light up in turn; mic icon pulses |
| 2.9–4.9 | **Learner** | *(open mic)* Demo: **« Bonjour, je voudrais réserver une chambre. »** | **Interaction beat.** Screen shows a line from their current unit |
| 4.9–5.4 | **Duo** | "Whoa!" | Short, surprised |
| 5.4–8.0 | **Lily** | "...Mm. I understood you." | Half-beat pause, flat, slow. **The heaviest line in the ad.** Caption: *"The highest praise Lily gives."* |
| 8.0–8.9 | **Zari** | "That was real French!" | Burst of energy; screen brightens |
| 8.9–10.7 | **Lily** | "Your accent... it's okay." | Still flat — but she has never complimented anyone before |
| 10.7–14.9 | **Duo** | "Again? Super — free for seven days." | Warm close; CTA button appears in sync |

**Total runtime: 14.92s** ✅

---

## 4. Interaction beat (at 2.9s)

| Step | Design |
|---|---|
| What the user does | Speaks the prompted line into the mic — a sentence from their current unit |
| What the system does | Short-utterance ASR → match against "current unit phrase bank" → trigger the matching character reaction |
| Why that line | It must come from a unit the learner **has actually studied** — the credibility of "being understood" depends on it being something they learned |
| Feedback timing | Reaction fires immediately on recognition (target <600ms). Latency kills the feeling of being understood |

---

## 5. Edge cases

| Case | Handling | Rationale |
|---|---|---|
| Silent >2s | Duo drops to a prompt: "No rush — try this one:" → learner repeats | No dead air. An ad must never embarrass the viewer |
| Wrong language / wrong words | Zari catches it warmly: "English counts as speaking up! Now try it in French." | Never correct, never judge — only encourage |
| Mic permission denied | Fallback to a "tap to hear it" version; characters react to a preset line | A denied permission must not become a dead end |
| Noisy room / low confidence | **Default to positive feedback** | In an ad, a false positive costs far less than killing the mood |
| User says a full sentence | Escalated reaction: "Wait — you said a whole sentence?" | Delight for high-engagement users |
| Cost / compliance | Short-utterance ASR, no audio retained, no voiceprint; frequency-capped | Avoids PII and runaway inference cost |

---

## 6. KPI mapping

This 15-second ad **is the first screen of the trial**.

| Metric | Note |
|---|---|
| Completion rate | 15s is a hard constraint; Lily's deadpan is the retention hook |
| **Speak-up rate** | The key intermediate metric — did the user actually talk to the ad? |
| 7-day trial activation | Primary metric (conversion) |
| vs. silent control | The decisive experiment: interactive vs. watch-only, to quantify the lift from interaction |

**How it moves the KPI**: it pulls "being understood" forward from a post-purchase experience to a
pre-purchase one. Users get to feel the state they'll be asked to pay to repeat — before the pitch.

---

## 7. Audio file

`ad_15s_roundtable_en.mp3` — 14.92s, 7 lines, 4 distinct voices (3 characters + French learner line).

> Note: demo voices are synthesized with edge-tts and are **not official Duolingo voice actors**.
> They exist to convey pacing, delivery and character contrast; a production version would use the
> official cast. (The earlier Chinese/Spanish cut remains as `ad_15s_roundtable.mp3`.)
