# Midterm 1: "No Alert Left Unanswered"
### The story version: script, slide plan and team briefing

**Length:** about 6.5 minutes at a calm pace (about 90 words a minute).
**The story:** Susan and Adam are **fictional**. The delays in their story are illustrative, based on the problems the research describes. Say so on screen (slide 1, small text) and in the intro. Inventing a patient and presenting her as real would be a problem in an academic presentation.

| # | Slide | Speaker | Time |
| --- | --- | --- | --- |
| 1 | Meet Susan | Hiba | 1:00 |
| 2 | Susan is not alone | Joelle | 0:50 |
| 3 | What the research says + our add-on | Doaa | 1:30 |
| 4 | How it works: Susan's case in our loop | Joelle | 1:00 |
| 5 | Feasible with proven technology | Joelle | 0:45 |
| 6 | What we replace + how we build it | Cleo | 1:00 |
| 7 | Back to Susan (closing) | Cleo | 0:30 |
| 8 | References + AI use | silent | 0:05 |

---

## Slide 2: "Meet the Team" (Joelle, about 25 seconds)
**On screen:** four cards (J, H, D, C) with each person's name, role and one line.

**Joelle:**
> Hi, we're the team behind *No Alert Left Unanswered*. I'm Joelle, the team leader; I lead the product and designed the escalation algorithm. Hiba makes sure that everything we propose can really be built. Doaa finds and checks the science behind every claim we make. And Cleo plans how we'll build, staff and launch the product. Now let us tell you about Susan.

*(The roles are a proposal. Change them on the slide if the team splits the work differently.)*

---

## PART 1: Hiba and Joelle

### Slide 1: "Meet Susan" (Hiba)
**On screen:** a clock showing **9:20**, a phone with an unopened notification: *"STROKE ALERT: suspected large vessel occlusion"*. Below it, a timeline that fills in as Hiba speaks: 8:40 → 9:05 → 9:20 → 10:10. Small text: *"Susan and Adam are fictional. Their story is based on delays described in the research."*

**Hiba:**
> Meet Susan. She's 61, and every Tuesday she makes breakfast for her granddaughter. This Tuesday, at 8:40, the spoon falls out of her hand. Half of her face won't move, and she can't find her words.
>
> By 9:05 she's in the emergency room of her small local hospital. Adam, the nurse on shift, gets her straight to the CT scanner. At 9:20 the AI software spots it: a large blood clot in her brain. An alert goes out to the stroke specialist at the big hospital, forty minutes away.
>
> And then… nothing. The specialist is in the middle of another procedure. Her phone is in a locker.
>
> Adam keeps checking the screen. At 9:45 he starts calling: the switchboard, another number, voicemail. At 10:10 he finally reaches the backup doctor.
>
> Nobody did anything wrong. But Susan waited **fifty minutes for someone to answer.**

### Slide 2: "Susan is not alone" (Joelle)
**On screen:** one huge number, then two stat cards.
- **50 minutes ≈ 95 million brain cells** *(an estimated 1.9 million per minute [1])*
- **121 min**: median wait at the first hospital before transfer (22,410 patients) [2]
- **65% lower odds** of thrombectomy when the wait is over 4.5 hours [2]

**Joelle:**
> Fifty minutes. It's estimated that an untreated stroke destroys about 1.9 million brain cells every minute. For Susan, that is about ninety-five million brain cells, lost while waiting for an answer.
>
> Susan is fictional, but her wait is not unusual. A 2026 study in *The Lancet Neurology* followed more than 22,000 stroke patients who had to be transferred for treatment. The median time they spent at the first hospital was 121 minutes, about two hours. When that wait went over four and a half hours, their odds of getting the clot removed were 65% lower, and they left hospital more disabled.
>
> AI already finds the stroke fast. The minutes are lost in what happens **after** the alert. That's why our solution is a must-have, not a nice-to-have.

---

## PART 2: Doaa

### Slide 3: "The time is won in communication" (Doaa)
**On screen:** left, three short research findings with numbered circles; right, four icon cards (bell, chart, network, calculator).

**Doaa:**
> So what does the research say? Viz.ai is the company that built the AI in Susan's story. A meta-analysis of 12 studies and more than 15,000 patients found that Viz.ai shortens the time from the CT scan to treatment. But it found no significant change in patients' outcomes yet [3].
>
> Another study found that the AI cut the time from the scan to notifying the team from 26 minutes to 7 [4]. And a study of 29 hospitals found that hospitals with a stroke coordinator, someone whose job is to keep things moving, treat patients faster: about 60 minutes from arrival to treatment, against 81 without one [5].
>
> Together, these studies tell us one thing: the AI detection works, and the time is won in **communication**. What's missing is a guarantee that every alert gets an answer.
>
> That's our idea: an add-on that works **with** Viz.ai. It has four parts. An **escalation engine**, so an unanswered alert moves to the next doctor. A **dashboard** that shows hospitals where minutes are lost. A **digital twin**, a computer simulation of the hospital, to test changes before making them. And an **ROI calculator** that turns minutes saved into money.

---

## PART 3: Joelle

### Slide 4: "How it works: Susan's case in our loop" (Joelle)
**On screen:** the flowchart (CT scan → Viz.ai flags stroke → alert + timer → answered? → yes: log times / no: escalate to next doctor → back to timer). Susan's times appear beside the boxes: 9:20 alert, 9:25 no answer, 9:25 backup doctor alerted, 9:30 accepted. The four technologies sit along the bottom.

**Joelle:**
> Let's run Susan's morning through our system. At 9:20 Viz.ai flags the stroke, and our system alerts the on-call specialist and starts a timer. The hospital decides how long; say five minutes.
>
> At 9:25 there's still no answer, so the system doesn't wait for Adam to notice. It automatically alerts the next doctor on the on-call list, and the timer starts again. At 9:30 the backup doctor accepts. Every step is time-stamped, and that data feeds the dashboard and the simulation.
>
> To build it we use four technologies. A **mobile app with push notifications**, to reach the doctor's phone in seconds. **HL7 FHIR**, the international standard that hospital systems use to share data, so we can connect to the hospital. **Python**, to build the simulation. And a **secure cloud server** that stores every timestamp and controls who can see the data.

### Slide 5: "Feasible: built from proven technology" (Joelle)
**On screen:** left, "Already proven" with the big number **39 → 23 min** [6]; right, "Risks we manage" with four short items. Bottom: **Feasibility: high.**

**Joelle:**
> Can this actually be built? We believe yes, because every piece already exists. A 2024 study built exactly this kind of simulation, in Python, for a real stroke center. By testing changes in the simulation first, it cut the time from arrival to treatment from 39 minutes to 23 [6].
>
> There are risks we take seriously. Alert fatigue: if staff get too many alerts, they start ignoring them [7], so our escalation must be targeted. Connecting to each hospital's systems. Medical-device regulation. And an existing patent on alert escalation that we need to check.
>
> Our conclusion: technological feasibility is high. The innovation is in the combination, not in a scientific breakthrough.

---

## PART 4: Cleo

### Slide 6: "What we replace, and how we build it" (Cleo)
**On screen:** top, before → after. "Adam on the phone" (phone icon) → "automatic backup alert" (lightning icon). Bottom, three stage cards: 1 Prototype, 2 Dashboard + simulation, 3 Pilot in one hospital. Small team line.

**Cleo:**
> Every innovation replaces something. Economists call it creative destruction. What we replace is Adam on the phone: the manual step of noticing that nobody answered and hunting for the backup doctor. With our add-on, the hospital sets a time limit, and when it runs out the backup doctor is alerted automatically.
>
> We'll build it in three stages. First, an alert prototype tested on fictional cases; the milestone is that an unanswered alert reaches the backup doctor. Second, the dashboard and the simulation; the milestone is showing where patients wait and comparing two alert rules. Third, a pilot in one hospital, where staff test the system and tell us what to fix.
>
> In the first year that takes two developers, with part-time clinical and regulatory advisors. In the second year we add a developer and a person for hospital partnerships.

### Slide 7: "Back to Susan" (Cleo)
**On screen:** the same timeline as slide 1, side by side. *Today: answered 10:10.* *With us: answered 9:30.* Under it, large: **40 minutes sooner ≈ 76 million brain cells.** Tagline: **No alert left unanswered.**

**Cleo:**
> Let's go back to Susan. With our system, her alert is answered at 9:30 instead of 10:10. Adam doesn't make a single phone call. That's forty minutes sooner: an estimated seventy-six million brain cells.
>
> Our vision is simple: help hospitals make sure that **no stroke alert is left unanswered**. Thank you.

---

## Slide 8: References (IEEE), silent
1. J. L. Saver, "Time is brain—quantified," *Stroke*, vol. 37, no. 1, pp. 263–266, 2006, doi: 10.1161/01.STR.0000196957.55928.ab.
2. R. Royan *et al.*, "Door-in-door-out times and outcomes in patients with acute ischaemic stroke transferred for endovascular therapy in the USA," *Lancet Neurol.*, vol. 25, no. 2, pp. 160–169, 2026, doi: 10.1016/S1474-4422(25)00478-8.
3. K. Sarhan *et al.*, "Automated emergent large vessel occlusion detection using Viz.ai software and its impact on stroke workflow metrics and patient outcomes in stroke centers: A systematic review and meta-analysis," *Transl. Stroke Res.*, vol. 16, no. 6, pp. 2258–2271, 2025, doi: 10.1007/s12975-025-01354-0.
4. L. Elijovich *et al.*, "Automated emergent large vessel occlusion detection by artificial intelligence improves stroke workflow in a hub and spoke stroke system of care," *J. NeuroInterv. Surg.*, vol. 14, no. 7, pp. 704–708, 2022, doi: 10.1136/neurintsurg-2021-017714.
5. M. Srinivasan *et al.*, "The role of stroke care infrastructure on the effectiveness of a hub-and-spoke telestroke model in South Carolina," *J. Stroke Cerebrovasc. Dis.*, vol. 33, no. 6, Art. no. 107702, 2024, doi: 10.1016/j.jstrokecerebrovasdis.2024.107702.
6. G. Koca, J. T. Blake, G. J. Gubitz, and N. R. Kamal, "Discrete event simulation model of an acute stroke treatment process at a comprehensive stroke center," *J. Neurol. Sci.*, vol. 468, Art. no. 123369, 2024, doi: 10.1016/j.jns.2024.123369.
7. K. Wang *et al.*, "Alarm fatigue levels and associated factors among intensive care unit nurses: A systematic review and meta-analysis," *Intensive Crit. Care Nurs.*, vol. 99, Art. no. 104608, 2026, doi: 10.1016/j.iccn.2026.104608.

*AI use: Claude (Anthropic) helped find the literature and draft this script and these slides. The tools and prompts are listed in the AI appendix.*

---
---

# Team briefing: the full context

Read this before recording, so that everyone understands the whole presentation, not just their own part.

## The project in 30 seconds
- **Course:** Management of Technological Ventures (Dr. Elvira Bar). We build a full business plan for a tech venture and present it in English; everyone speaks.
- **Inspiration:** **Viz.ai**, a company whose AI reads stroke CT scans, flags a blocked brain artery, and sends an alert to the stroke team's phones.
- **Our idea:** an add-on that works **with** Viz.ai and focuses on what happens **after** the alert:
  1. **Escalation engine:** if the doctor doesn't confirm within X minutes, the alert goes to the next doctor.
  2. **Delay dashboard:** shows where minutes are lost (arrival → scan → decision → treatment).
  3. **Digital twin:** a computer simulation of the hospital, to test changes before making them.
  4. **ROI calculator:** turns minutes saved into money (shorter hospital stays, less long-term disability). It later becomes our financial plan.
- **What we do NOT claim:** that Viz.ai has no escalation feature. We haven't verified that. Always say "complements Viz.ai" or "works with Viz.ai".
- **This video is Midterm 1:** the theory part (the problem, the research, the solution, the algorithm and the feasibility). It gets feedback, not a grade. The final presentation must fix whatever the teacher comments on.

## Words you need to know
| Term | Plain meaning |
| --- | --- |
| **Ischemic stroke** | A blood clot blocks an artery in the brain; brain tissue starts dying |
| **LVO (large vessel occlusion)** | The clot is in one of the big brain arteries. The most severe kind, and the kind Viz.ai detects |
| **CT / CTA** | Brain scan / scan of the blood vessels with contrast dye |
| **Thrombectomy (EVT)** | A procedure where a doctor threads a catheter to the brain and pulls the clot out. Only big "stroke centers" can do it |
| **Thrombolysis (tPA)** | A clot-dissolving drug given by IV |
| **Door-to-needle / door-to-groin** | Time from arrival at the hospital to the drug / to the start of thrombectomy |
| **DIDO (door-in-door-out)** | How long a patient stays at the first hospital before being transferred |
| **Hub-and-spoke** | Small local hospitals (spokes) send patients to one big stroke center (hub) |
| **Escalation** | Moving an unanswered alert up to the next person |
| **Alert fatigue** | Staff get so many alerts that they start ignoring them |
| **Digital twin / discrete-event simulation** | A computer model of the hospital's steps, used to test "what if" changes |
| **HL7 FHIR** | The international standard hospital computer systems use to exchange data |
| **ROI / QALY** | Return on investment / a "quality-adjusted life year", the unit health economists use to value health |

## The sources behind each claim
| Claim | Source | Note |
| --- | --- | --- |
| About 1.9 million brain cells lost per minute | Saver 2006 [1] | A modelled **estimate**; always say "an estimated" |
| Median wait before transfer 121 min; >4.5 h gives 65% lower odds of thrombectomy | Royan 2026, *Lancet Neurology* [2] | 22,410 US patients. It's "lower **odds**", not "lower chance" |
| Viz.ai shortens workflow times; no significant change in outcomes | Sarhan 2025 meta-analysis [3] | 12 studies, 15,595 patients |
| Scan-to-notification time 26 → 7 min | Elijovich 2022 [4] | 680 cases, hub-and-spoke system |
| Stroke coordinator: 57-61 vs 81 min | Srinivasan 2024 [5] | 29 spoke hospitals |
| Python simulation: 39 → 23 min door-to-needle | Koca 2024 [6] | Shows our digital twin is feasible |
| Alert fatigue is widespread | Wang 2026 [7] | Meta-analysis of 4,084 ICU nurses |
| Susan's 50 minutes; 40 minutes saved | **Fictional** | Illustration only. 50 × 1.9M ≈ 95M; 40 × 1.9M ≈ 76M |

**Before recording, each speaker should open their own sources** (JCE library → ScienceDirect) and check their numbers. The numbers above come from the papers' abstracts.

## Questions the teacher might ask, and how to answer
- **"Doesn't Viz.ai already do this?"** "Viz.ai sends the alert and has team communication. We haven't confirmed whether it automatically escalates an unanswered alert, so we designed our product as an add-on that works with it. Checking this is one of our next steps."
- **"Is Susan real?"** "No. She's a fictional patient, but her delays reflect what the research found, like the two-hour median wait in the *Lancet Neurology* study."
- **"Won't more alerts cause alert fatigue?"** "That's a real risk, and it's in our risk list. Our system doesn't send more alerts; it sends the same alert to one more person, only when nobody answered."
- **"Is it a medical device?"** "We don't analyze images, only route alerts and measure times, which may put us in a lighter regulatory category. We still need to check the FDA and EU guidance; it's in our risks."
- **"Why would a hospital pay?"** "Saving minutes means less disability and shorter hospital stays. Our ROI calculator will show this in money; that's our next part, the marketing and financial plan."

## Before you record: checklist
- [ ] Everyone has read the whole script, not only their part
- [ ] Each speaker has checked the numbers in their own sources
- [ ] The slides say Susan and Adam are fictional
- [ ] Save every AI prompt you used (screenshots) for the AI appendix; it's a course requirement
- [ ] Practice with a timer: about 6.5 min in total
- [ ] Don't read the slides; look at the camera
