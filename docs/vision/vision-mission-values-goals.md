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

## 1. Vision (#28, Cleo)

> **A hospital where every stroke alert is answered and every minute is accounted for.**

Proposed by Cleo in #28, for the team to agree on. Hebrew for the talk:
> החזון שלנו הוא בית חולים שבו כל התראה על שבץ מוחי מקבלת מענה, וכל דקה בתהליך הטיפול נמדדת.

Check against the lecture's 6 components (from #28):

| Component | Yes because |
| --- | --- |
| Future direction | Describes the hospital workflow we want to create |
| Customer benefit | Hospitals respond faster and see where delays happen |
| Realistic | Connects directly to our escalation engine and delay dashboard |
| Motivating | A shared purpose: reducing delays in stroke care |
| Communicated | On the slide and explained in the presentation |
| Followed and measured | Alert response times, % acknowledged within the time limit, time between care stages |

Avoided (lecture "common mistakes"): a vague vision such as "be the best stroke software in the world".
Alternative we considered: "No stroke patient should lose brain to an unanswered alert" (shorter, patient-centred).

## 2. Mission (#29, Hiba, agreed by the team)

**Slide version:**
> **Escalate every alert. Measure every minute. Test before you change. Prove the value.**

**Full version (slide / executive summary):**
> We give stroke teams and hospital managers one platform that makes sure every urgent stroke alert reaches a doctor who answers, shows where minutes are lost between arrival and treatment, and lets hospitals test changes in a digital twin before making them, proving the value in minutes and money saved. We build on top of Viz.ai's detection, not in place of it.

Hebrew version and the speaker line are in #29.

The four verbs are our four components: escalation engine, door-to-treatment dashboard, hospital digital twin, ROI calculator. The mission is the "how"; the vision is the "what".

> Keep the wording "add-on to Viz.ai" or "complements Viz.ai". We have **not** verified that Viz.ai lacks timed escalation (#11).

## 3. Values (#30, Doaa)

Doaa kept all five values and rewrote the descriptions (#30, 21 Nov 2026). The team can still review the wording before the final slide.

| Value | What it means in practice |
| --- | --- |
| **Every Minute Counts** | We focus on reducing delays so stroke patients can receive care as quickly as possible |
| **Evidence Before Claims** | We use reliable sources to support our medical and business claims, and are transparent when information is not available |
| **Patient Safety and Privacy First** | We use synthetic or public data for the prototype, and only use real patient data with the required approval and consent |
| **Support Clinicians, Don't Replace Them** | Our system helps urgent alerts reach the right doctor on time. It supports doctors and complements Viz.ai rather than replacing it |
| **Fair Care for Every Patient** | We aim to provide fair care by monitoring alert and treatment times across different ages, sexes, languages, and locations |

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
| **Vision** | A hospital where every stroke alert is answered and every minute is accounted for |
| **Mission** | Escalate every alert. Measure every minute. Test before you change. Prove the value. |
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
