# Vision, mission, values, goals and KPIs (rubric 2.3)

Course assignment: lecture 5, "חזון, משימה, ערכים, יעדים ומטרות". Issues #28 (vision), #29 (mission), #30 (values), #31 (goals, objectives, KPIs). The slide goes into #16.

The lecture's structure, which this page follows:

| Part | Question it answers | Lecture definition |
| --- | --- | --- |
| **Vision** | What do we want to be? | An ambitious, clear picture of the future. The "what" and the compass |
| **Mission** | How will we get there? | The means to reach the vision. The "how" |
| **Values** | How do we behave on the way? | Guiding beliefs about how things should be done |
| **Goal (יעד)** | Which big results do we aim for? | A broad, important result |
| **Objective (מטרה)** | How do we know we got there? | Measurable, concrete, with a deadline (SMART) |
| **KPI** | What do we track every week or month? | Indicators of performance against the objectives |

All of it builds on the development plan in 2.4 and 2.5 (Cleo): **year 1** build and test the prototype, dashboard and simulation on fictional cases; **year 2** pilot at one hospital.

---

## 1. Vision (#28)

> **No stroke patient should lose brain to an unanswered alert.**

Why this line:
- It is short, like the Disney and IKEA examples, and matches our deck title, *No Alert Left Unanswered*.
- It names the benefit to the patient (lecture: "expresses a consumer benefit").
- It is realistic: we do not promise to cure stroke, only to close the gap after the alert.
- It can be measured: the share of alerts that get an answer in time (see the KPIs).

Check against the lecture's 6 components:

| Component | Yes because |
| --- | --- |
| Future direction | Describes the world we want, not today's product |
| Customer benefit | Patients keep brain tissue; doctors and nurses stop chasing phones |
| Realistic | Escalation is proven technology (see the feasibility slide) |
| Motivating | One clear enemy: the unanswered alert |
| Communicated | One sentence, the same as the deck title |
| Followed and measured | KPI "alerts acknowledged in time" |

Avoided (lecture "common mistakes"): a vague vision such as "be the best stroke software in the world".

## 2. Mission (#29)

**Slide version:**
> **Escalate every alert, measure every minute, test before you change, prove the value.**

**Full version (for the talk and the executive summary):**
> We help hospitals respond faster to stroke alerts and see where patients lose time on the way to treatment. Our add-on to Viz.ai moves an unanswered alert to the next doctor in line, shows each step from arrival to treatment on one dashboard, lets managers test a change in a simulation before they make it, and turns the minutes saved into money.

The four verbs are our four components: escalation engine, door-to-treatment dashboard, hospital digital twin, ROI calculator. The mission is the "how"; the vision is the "what".

> Keep the wording "add-on to Viz.ai" or "complements Viz.ai". We have **not** verified that Viz.ai lacks timed escalation (#11).

## 3. Values (#30)

| Value | What it means in practice |
| --- | --- |
| **Every minute counts** | We treat delay as harm. A feature that does not save time or show where it is lost does not go first |
| **Evidence before claims** | Every medical or business number on a slide has a source. When we have none, we say so |
| **Safety and privacy first** | The prototype uses fictional or public data only. Real patient data only under regulation and the hospital's approval |
| **Support clinicians, don't replace them** | The doctor decides. We make sure the right doctor hears in time, and we work with Viz.ai, not against it |
| **Fair care for every patient** | We check that response times are the same across age, sex, language and distance from the city |

Format follows the Data.AI example from the lecture: a short name and one line of behaviour.

## 4. Goals, SMART objectives and KPIs (#31)

Three goals only (the lecture warns against "overplanning"). Months count from the start of development. Every objective is checked against SMART below.

### Goal 1: Faster response to stroke alerts
*Relevant to the vision: an alert that gets answered is the vision itself.*

| Objective | S | M | A | R | T |
| --- | --- | --- | --- | --- | --- |
| **1a.** By **month 6**, the escalation prototype passes all test scenarios on fictional cases: every unacknowledged alert reaches the backup doctor when the timer runs out | One feature, one test set | % of test alerts escalated on time = 100% | Timers and push notifications are standard technology | It is our core component | Month 6 |
| **1b.** During the **year-2 pilot**, the median time from alert to a doctor's acknowledgment is **under 5 minutes**, and **98%** of alerts are acknowledged within **10 minutes** | One pilot hospital, stroke alerts only | Two numbers from the system log | A ~2 min escalation timer already exists in a patent (US 8,775,196); a 5 min median allows two escalation steps | Directly measures the vision | End of year 2 |

Baseline for 1b: in a small ICU trial of urgent sepsis alerts, the median time to acknowledge was **102 minutes by pager** and 169 in the EHR [Dziadzko et al. 2016, PMC5148853; 48 alerts, stopped early, so use it as an illustration, not a benchmark].

### Goal 2: Make delays visible, then cut them
*Relevant to the vision: you cannot fix minutes you cannot see.*

| Objective | S | M | A | R | T |
| --- | --- | --- | --- | --- | --- |
| **2a.** By **month 12**, the dashboard shows door-to-scan, scan-to-decision and decision-to-treatment times, and the simulation compares at least **two alert rules**, both on sample data | Named steps and a named comparison | Feature done / not done, checked in a demo | A stroke-pathway simulation has been built before [6] | Shows where Susan's minutes went | Month 12 |
| **2b.** During the pilot, the simulation reproduces the hospital's real median times **within 10%** | One hospital, median times | % difference | Bulmer 2021 and Koca 2024 built validated models | Makes the "test before you change" promise credible | Month 18 |
| **2c.** By the **end of the pilot**, median door-to-needle time at the pilot hospital is **10% lower** than its baseline | One metric, one site | Before vs after | A US national quality program (Target: Stroke) cut the median from 77 to 67 min, about 13% [Fonarow 2014] | Minutes saved = brain saved | End of year 2 |

### Goal 3: Prove the value to hospitals
*Relevant to the vision: hospitals adopt what they can justify, so more patients get the benefit.*

| Objective | S | M | A | R | T |
| --- | --- | --- | --- | --- | --- |
| **3a.** At the **end of the pilot**, the pilot hospital gets an ROI report built from its own measured minutes (ROI calculator, #13) | One report, one hospital | Delivered / not | The calculator already exists (`docs/business/`) | Turns minutes into a reason to buy | End of year 2 |
| **3b.** By the **end of year 3**, **3 hospitals** pay a subscription, including the pilot hospital | Paying hospitals | Count of signed contracts | 1 pilot + 2 referrals in one country | Each hospital means more patients covered | End of year 3 |

### KPIs (what we track every month)

Includes technical KPIs on purpose: the lecture lists "no technological KPIs (response time, uptime, usage)" as a common mistake.

| Type | KPI | Target | Feeds objective |
| --- | --- | --- | --- |
| Technical | Alert delivery time (server to phone) | under 5 seconds | 1b |
| Technical | Uptime of the alert service | 99.9% | 1b |
| Technical | Test coverage of the escalation logic | 90% of code paths | 1a |
| Clinical | Median time from alert to acknowledgment | under 5 min | 1b |
| Clinical | Share of alerts that needed escalation | falling month on month | 1b |
| Clinical | Median door-to-needle time | 10% below baseline | 2c |
| Alert fatigue | Response rate compared with the first month (no lasting drop) | stable or rising | 1b |
| Usage | Monthly active on-call doctors / doctors on the roster | over 80% | 1b |
| Business | Pilots converted to paid | 1 of 1 | 3b |
| Business | Hospital renewal after the first year | 90% | 3b |

For the slide, pick **5-7 KPIs** and keep at least 2 technical ones. Suggested: delivery time, uptime, alert-to-acknowledge, door-to-needle, pilot conversion.

### Short slide version (one slide)

| | |
| --- | --- |
| **Vision** | No stroke patient should lose brain to an unanswered alert |
| **Mission** | Escalate every alert, measure every minute, test before you change, prove the value |
| **Goal 1** | Faster response: median alert-to-acknowledge < 5 min in the pilot |
| **Goal 2** | Visible delays: door-to-needle −10% at the pilot hospital |
| **Goal 3** | Proven value: 3 paying hospitals by the end of year 3 |
| **KPIs** | Delivery < 5 s · uptime 99.9% · alert-to-acknowledge · door-to-needle · pilot-to-paid |

---

## Before this goes on a slide
- [ ] Team agrees on the vision line and the 5 values (or cuts to 4)
- [ ] Targets are **our proposals**, not facts: say "our target" on the slide
- [ ] Check the cited numbers in the original papers (see the source check in `docs/business/business-model-and-roi.md`)
- [ ] Match the timeline with Cleo's 2.4/2.5 slides (year 1 build, year 2 pilot)
