# Viz.ai Venture: Research File (for Perplexity fact-checking)

Course: Management of Technological Ventures (100997101/2/3), Dr. Elvira Bar.
File written 2026-10-25. Team: 4 students (updated 2026-11-14).

---

## 1. How to use this file with Perplexity

1. Paste or upload this file into Perplexity.
2. Run the prompts in section 9, one at a time. Ask for sources with links every time.
3. Open each source yourself. Perplexity can also be wrong.
4. Update the "Status" column in section 6 and the bibliography in section 10.
5. **Course rule:** if you use AI for the work, say so on the slides and attach an appendix with the tool names and the exact prompts (screenshots are enough). Save every prompt, including these.

---

## 2. The venture

**Company that inspired it:** Viz.ai (https://www.viz.ai), an AI care-coordination company.

**Problem (1-2 sentences):** In a stroke every minute counts: an estimated 1.9 million brain cells die per minute without treatment. An alert to the on-call doctor does not always get a response in time, and hospitals struggle to see where the minutes are lost between a patient's arrival and treatment.

**Solution (1-3 sentences):** A web dashboard and mobile app for medical teams and hospital managers. An escalation engine moves an unanswered alert to the next doctor in line. A dashboard shows where time is lost along the care pathway. A server-side simulation (a hospital "digital twin") tests pathway changes before they are made, and an ROI calculator turns minutes saved into money.

**What we are NOT claiming:** that Viz.ai lacks automatic escalation. We have not verified this. The text says "complements Viz.ai".

### Core components
1. **Escalation engine:** if the on-call specialist does not acknowledge within a set time, the alert goes to the next person.
2. **Door-to-treatment dashboard:** shows where minutes are lost from arrival to scan, decision and treatment.
3. **Hospital digital twin:** a discrete-event simulation of the stroke pathway for what-if tests (staffing, layout, on-call order).
4. **ROI calculator:** converts minutes saved into money (shorter stays, less long-term disability care). Doubles as the financial plan.
5. **Optional trust layer:** fairness audit checking alerts and treatment times across groups (age, sex, language, distance from the city).

---

## 3. What we know about Viz.ai

| Fact | Status |
| --- | --- |
| AI analyzes medical images and other clinical data, flags suspected disease, alerts care teams | Read on https://www.viz.ai (company claim) |
| Products: Viz.ai One (enterprise care-coordination platform), Viz Assist (workflow assistant), suites for neuro, vascular, cardio, pulmonary, radiology, trauma, oncology; Viz Life Sciences for pharma/device partners | Read on homepage |
| "More than 50 FDA-cleared AI algorithms" (CT, EKG, echo) | Read on homepage (company claim) |
| Neuro pathways include large vessel occlusion, CT perfusion, hemorrhage, aneurysm, post-acute stroke; vascular includes aortic disease and pulmonary embolism; cardio includes hypertrophic cardiomyopathy, acute coronary syndrome, cardiac amyloidosis | Read on homepage |
| Homepage gives no hospital count and no outcome figures | Read on homepage |
| Founded in Tel Aviv; sells mainly to hospitals via software subscriptions | Search summary only. UNVERIFIED |
| Funding: a $71M Series C reported by MobiHealthNews; a startup-tracker profile lists about $289.5M total and a Series D in July 2025 | Search summary only; article returned an access error; sources conflict. UNVERIFIED |
| Company-reported study: 2,544 patients, 139 hospitals, 96% sensitivity and 94% specificity for large vessel occlusion | Search summary only, company claim. UNVERIFIED |
| Untreated large-vessel stroke destroys an estimated 1.9 million neurons per minute | Saver 2006, Stroke, https://pubmed.ncbi.nlm.nih.gov/16339467/ . A modeled estimate, not a measurement |

---

## 4. Current problems (from general knowledge, NOT yet sourced)

These are the problem claims behind the idea. Each needs a source before it goes on a slide.

- Transfers between hospitals are slow and often run on phone calls.
- Smaller or peripheral hospitals often lack a specialist on site.
- An alert may reach someone who does not respond, and nothing escalates.
- Coordination is split across pagers, calls and messaging apps.
- Hospitals struggle to measure where time is lost (often done by hand).
- Alert fatigue reduces trust in clinical AI alerts.

---

## 5. All 11 ideas considered

| # | Idea | What it does | Problem | Why Viz.ai would want it |
| --- | --- | --- | --- | --- |
| 1 | Escalation engine | Moves an unanswered alert to the next on-call person | Unanswered alerts waste minutes | More trusted alerts |
| 2 | Door-to-treatment dashboard | Shows where minutes are lost | Hospitals measure delays by hand | Proof of value for renewals |
| 3 | Ambulance destination advisor | Recommends nearest hospital that can treat now | Paramedics decide with little live information | Extends coordination before arrival |
| 4 | Peripheral-hospital transfer app | One place to request, track, confirm a transfer | Slow, phone-based transfers | Reaches smaller hospitals |
| 5 | Hospital digital twin | Simulation to test staffing and layout changes | Managers guess | Selling tool |
| 6 | ROI calculator | Turns minutes saved into money | Managers cannot justify cost | Shorter sales cycles |
| 7 | Fairness audit dashboard | Checks alerts and times across groups | Bias in medical AI is hard to see | Trust, regulatory scrutiny |
| 8 | Family update app | Live plain-language status for relatives, several languages | Families wait with no information | Patient experience |
| 9 | Low-cost integration layer | Standards-based connector to image and record systems | Custom integrations are slow and costly | Faster rollout |
| 10 | Post-discharge follow-up | App tracks medication, rehab, warning signs | Care stops at the hospital door | Extends post-acute stroke pathway |
| 11 | New pathway, such as sepsis | Detect, alert, coordinate for another urgent condition | Slow recognition on wards | New market, if not already covered |

### Combinations
- **A (chosen): 1 + 2 + 5 + 6.** Escalate, measure, prove, sell. The dashboard produces data for the twin and the ROI calculator.
- **B:** A plus 7 (fairness slide).
- C: 3 + 4 (routing story; needs live capacity data). D: 8 + 10 (easy survey, weak paying-customer story). E: 9 + 11 (growth story, unconfirmed coverage).

### Ranking (my judgment, not a measured score)
1 Escalation engine; 2 Digital twin; 3 ROI calculator; 4 Dashboard; 5 Fairness audit; 6 Family app; 7 Transfer app; 8 Ambulance advisor; 9 Integration layer; 10 Post-discharge; 11 New pathway.

---

## 6. Claims to verify with Perplexity

| # | Claim | Where it matters | Status |
| --- | --- | --- | --- |
| 1 | Viz.ai does or does not already auto-escalate unanswered alerts | Core novelty | TO CHECK |
| 2 | Viz.ai founding details, hospital count, funding total | Company slide | TO CHECK |
| 3 | 96% sensitivity / 94% specificity study (2,544 patients, 139 hospitals) | Credibility slide | TO CHECK |
| 4 | 1.9 million neurons per minute (Saver 2006) | Problem slide | Confirmed paper exists; modeled estimate |
| 5 | Transfers between hospitals are slow; typical door-to-needle / door-in-door-out times | Problem slide | TO CHECK |
| 6 | Alert fatigue evidence in clinical AI | Problem slide | TO CHECK |
| 7 | Competitors in stroke care coordination (names, products) | Marketing 3.3 | TO CHECK |
| 8 | Market size for stroke care coordination software | Marketing 3.2 | TO CHECK |
| 9 | Evidence that discrete-event simulation is used to improve stroke pathways | Technical 2.2 | TO CHECK |
| 10 | Cost data for stroke (hospital stay, disability care) in Israel or elsewhere | Finance 4.2, ROI model | TO CHECK |
| 11 | Regulation: is an escalation/dashboard layer a regulated medical device? | Risk / IP 2.7 | TO CHECK |
| 12 | Evidence for bias or disparities in stroke treatment times | Fairness slide | TO CHECK |

---

## 7. Mapping to the course rubric

| Rubric item | What we have / need |
| --- | --- |
| 2.1 Problem and size | Saver 2006 figure; need delay and cost statistics |
| 2.2.2 Block algorithm | Escalation logic (timer, acknowledge, next on-call); simulation flow |
| 2.2.3 Creative destruction | Replaces phone trees, pagers, manual spreadsheets |
| 2.7 IP and barriers | TO DO: patentability, data advantage, hospital integrations |
| 3.1 Market survey | TO DO: interview 2-3 nurses, paramedics or hospital relatives |
| 3.3 Competitors | TO DO: see claim 7 |
| 3.7 and 4 Business model and finance | Likely hospital software subscription; ROI model feeds the financial plan; need Excel |
| 5 Bibliography | Fill section 10 |
| Appendix C | Keep AI prompt log |

Presentation limits: English slides, every member speaks, max 15 minutes (13-14 content slides) plus 3-5 minutes Q&A. Executive summary (half a page) submitted separately.

---

## 8. Risks and rules

- Use synthetic or public data in any prototype; real patient data is regulated. Say so on the slides.
- Do not present medical claims as fact without a citation. Say "an estimated" for the Saver figure.
- Another team may pick Viz.ai too. Post early in the forum and keep the idea clearly different.
- Ruled out: patient-facing "AI explains your results" ideas (classmates already posted K Health, Healthy.io, TytoCare ideas), and hardware, quantum and defense companies.

---

## 9. Perplexity prompts (copy one at a time)

Start every prompt with: "Answer with sources and links. Say clearly when you cannot find a source. Do not guess."

1. "Does Viz.ai offer automatic escalation of unanswered stroke alerts to the next on-call clinician? Check Viz.ai's product pages, FDA listings and independent reviews. Quote the source for each claim."
2. "Summarize Viz.ai: founding year, founders, headquarters, number of hospitals, total funding and latest round. List every source and flag any conflicts between sources."
3. "Find the peer-reviewed study behind Viz.ai's large vessel occlusion detection (about 2,544 patients, 139 hospitals, 96% sensitivity, 94% specificity). Give the journal, year and authors, and say whether the company or independent researchers ran it."
4. "Find peer-reviewed evidence on delays in inter-hospital transfer of stroke patients (door-in-door-out time) and how much time AI alerting tools save. Give numbers and citations."
5. "Find evidence on alert fatigue and unacknowledged alerts in clinical AI and clinical decision-support systems, with statistics and citations."
6. "List competitors of Viz.ai in stroke care coordination and AI triage (for example RapidAI, Brainomix, Methinks, and others). For each: product, regulatory status, and pricing model if public."
7. "Estimate the market size and growth of stroke care coordination or clinical communication software, with sources for each figure."
8. "Find peer-reviewed studies that used discrete-event simulation to model and improve stroke care pathways or emergency department flow."
9. "Find cost data for stroke in Israel (or OECD countries): average hospital stay cost, rehabilitation cost and long-term disability cost per patient, with sources."
10. "Would software that only routes alerts and analyzes workflow time (without analyzing images) be regulated as a medical device in the US (FDA) and the EU (MDR)? Cite the regulatory guidance."
11. "Find studies on disparities in stroke treatment times by sex, age, ethnicity, language or distance from a stroke center."
12. "Review this venture idea critically (paste section 2). List the 5 strongest objections a hospital manager or an investor would raise, with evidence for each."

---

## 10. Sources so far

| Source | Used for | Status |
| --- | --- | --- |
| https://www.viz.ai | Products, pathways, 50+ FDA-cleared algorithms | Opened |
| https://pubmed.ncbi.nlm.nih.gov/16339467/ (Saver JL, "Time is brain: quantified", Stroke 2006;37(1):263-6) | 1.9 million neurons per minute | Paper confirmed via search; abstract page |
| https://www.mobihealthnews.com/news/vizai-raised-71-million-expand-beyond-stroke-care-coordination | Funding and expansion | Not opened (access error) |
| https://startupim.com/company/viz | Funding and headcount lead | Not opened |
| https://nocamels.com/?p=98421 | Israeli tech news item | Not opened |

Add each new source here with the date you opened it.

---

## 11. Draft texts already prepared

**Google Form, field 1 (inspiration):** Viz.ai (https://www.viz.ai) - the company builds AI that spots medical emergencies such as stroke and alerts the care team. Our idea is a complementary add-on that, as far as we checked, it does not offer. (Remove "as far as we checked" and the claim unless you verified it.)

**Field 2 (problem):** In a stroke every minute counts (an estimated 1.9 million brain cells die per minute without treatment), but an alert to the on-call doctor does not always get a response in time, and hospitals struggle to see where the minutes are lost between a patient's arrival and treatment.

**Field 3 (solution):** A web dashboard and mobile app for medical teams and hospital managers: an escalation engine that automatically moves an unanswered alert to the next doctor in line, and a dashboard that shows where time is lost along the care pathway. A server-side simulation model also tests pathway changes before they are made and calculates the time and money saved.

(Contact details are left out of this file on purpose, so you don't paste them into Perplexity.)

---

## 12. Technological feasibility assignment: research found (2026-11-01)

Assignment (lecture PDF "בדיקת היתכנות טכנולוגית"): (a) ask an AI (Perplexity, GPT) to judge the idea **only on technological feasibility, using only academic sources**; (b) check it yourself in the literature: ScienceDirect through the JCE library (ezproxy.jce.ac.il), filter to Review / Research articles from 2024-2026, and export each citation with "Export citation to text".

Found through web search on 2026-11-01. Figures come from abstracts or summaries unless marked otherwise. **Open each paper yourself before you cite it.**

**Fix in the Google Doc:** Doaa's summary 1 (the meta-analysis) links to the wrong PubMed page (34417344, which is the hub-and-spoke paper from summary 2). The correct link is https://pmc.ncbi.nlm.nih.gov/articles/PMC12596299/ .

### A. The base works: AI alerts speed up stroke workflow (Doaa's 2 papers plus related work)
| Source | Key finding | Supports |
| --- | --- | --- |
| Systematic review and meta-analysis of Viz.ai, *Translational Stroke Research* 2025, DOI 10.1007/s12975-025-01354-0, https://pmc.ncbi.nlm.nih.gov/articles/PMC12596299/ | 12 studies, 15,595 patients. Shorter CT-to-thrombectomy (SMD -0.71) and door-to-groin (SMD -0.50), p<0.001. **No significant change in clinical outcomes.** The authors say the gains come partly from communication and system changes, not only from the detection algorithm | Problem and feasibility: the communication layer matters. That opens room for our escalation component |
| Hub-and-spoke Viz.ai study, PubMed 34417344 | 680 cases. CTA-to-notification time fell from 26 to 7 minutes. Door-to-puncture for transferred patients fell from 185 to 141 minutes | Fast alerts are technically proven |

### B. Escalation engine (component 1)
| Source | Key finding | Supports |
| --- | --- | --- |
| Randomized test of sepsis alert delivery methods (ICU), https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5148853/ | Median time to acknowledge an urgent alert: 102 minutes by pager vs 169 minutes in the EHR. The smartphone arm failed because of technical delivery errors | **Strong evidence for the problem:** alerts sit unanswered for a long time, and the delivery channel changes the response time |
| Automated alerts for critical pathology results, *Applied Clinical Informatics* 2018, https://www.thieme-connect.com/products/ejournals/pdf/10.1055/s-0038-1654700.pdf | Faster documented acknowledgment. Compliance with the institution's policy did not improve | Automation helps, but a closed loop is needed |
| Patent US 8,775,196, "System and method for notification and escalation of medical data" | Describes an escalation timer of about 2 minutes that the hospital can configure | **Feasibility:** the technology exists. **IP risk:** check freedom to operate (rubric 2.7) |
| Poly et al., *JMIR Med Inform* 2020, systematic review of alert fatigue, https://medinform.jmir.org/2020/7/e15653/PDF | Average override rates from 46.2% to 96.2% | Alert fatigue is real; escalation has to be smart, not just another alert |
| Ray et al. 2026, review of systematic reviews on alert fatigue (MetroHealth PDF) | Alert fatigue lacks a clear definition. Recommends measuring a sustained drop in the response rate against a baseline | A KPI we can show on our dashboard |

### C. Smartphone communication apps (the technical basis of the app)
| Source | Key finding |
| --- | --- |
| Join app, Japan, *Journal of Neuroendovascular Therapy* 2020, https://www.jstage.jst.go.jp/article/jnet/14/9/14_oa.2020-0030/_article/-char/en | Shorter door-to-puncture time. Information was shared before the patient arrived in 42% of cases |
| Join app vs control group, *Neurological Sciences* 2021, https://link.springer.com/article/10.1007/s10072-021-05132-2 | Image-to-needle, door-to-needle and door-to-recanalization times all significantly shorter |
| Note | The evidence is mostly small single-center studies; we found no large RCT. Also: Join, Pulsara and Vocera are **competitors** (rubric 3.3) |

### D. Door-to-treatment dashboard (component 2)
| Source | Key finding |
| --- | --- |
| Fonarow et al., *JAMA* 2014;311(16):1632-1640 (Target: Stroke) | 71,169 patients at 1,030 hospitals. Measurement plus a quality program cut mean door-to-needle time from 74 to 59 minutes, and in-hospital mortality fell from 9.9% to 8.3%. (Critics note that other changes happened over the same period) |
| Large DIDO study (AHA GWTG-Stroke registry, Lancet Neurology 2026; seen only in news summaries, **check the original**) | Only 26% of transfers met the 90-minute target. Above 4.5 hours, the chance of thrombectomy fell by 65% |
| European Stroke Journal 2023;8(3):667-674 | Median DIDO 66 minutes. **The largest contributor: the time from CTA to calling the ambulance**, a communication delay our system targets |
| Israeli study, *Frontiers in Neurology* 2023, https://www.frontiersin.org/journals/neurology/articles/10.3389/fneur.2023.1303061 | Door-to-puncture: 190 minutes for direct admission vs 293 minutes for transferred patients. Local Israeli data for the problem slide |

### E. Hospital digital twin (component 3)
| Source | Key finding |
| --- | --- |
| Bulmer et al., *Frontiers in Neurology* 2021, DOI 10.3389/fneur.2021.746404, https://pmc.ncbi.nlm.nih.gov/articles/PMC8586711/ | A discrete-event simulation (ARENA) of the thrombolysis process at urban and rural hospitals. Combining all scenarios cut median door-to-needle time by 26.7%. The best change differed between sites. **Direct evidence that our component is feasible** |
| Koca, PhD thesis, Dalhousie 2024 | Time-and-motion study plus DES. Median door-to-needle time fell from 39.4 to 23.0 minutes in the simulation. Also covers thrombectomy |
| Olawade et al. 2025, review of digital twins in emergency care, *Int J Med Inform* (S1386505625004460) | Uses: resource allocation, workflow optimization, ED capacity management |
| Zheng et al. 2025, *Reliability Engineering & System Safety* v.261 | **Barriers:** data integration and long, complex deployment. Belongs in the risks section |

### F. ROI calculator (component 4)
| Source | Key finding |
| --- | --- |
| HERMES-based Markov model, *Neurology* 2020 ("Public health and cost consequences of time delays to thrombectomy") | Every 10 minutes earlier gives about 39 more days of disability-free life and about $10,593 net monetary benefit (US, $100K/QALY) |
| Netherlands study, *J NeuroInterventional Surgery* 2021, https://jnis.bmj.com/content/early/2021/03/23/neurintsurg-2020-017017 | Each minute earlier is worth about €309 net monetary benefit and 1.3 days of disability-free life. Costs stay about the same over 5 years |
| Note | These figures come from different countries and thresholds and are not directly comparable. Israeli cost data is still missing (claim 10) |

### G. Regulation (feasibility and risks)
- FDA final guidance, Clinical Decision Support Software (Sep 28, 2022): software that analyzes **medical images** is a medical device (criterion 1). An escalation and dashboard layer that does not analyze images may count as non-device CDS or MDDS, **but this needs checking in the original guidance** (claim 11). This argues for building our product on top of Viz.ai's output rather than analyzing images ourselves.

### H. Interoperability
- HL7 FHIR: the Da Vinci Alerts/Notifications IG (v1.1.0, 2025) is a standard for clinical notifications. We found no peer-reviewed review of FHIR-based alerting; search PubMed/JAMIA. The integration barrier also appears in the digital twin reviews.

### Draft conclusion for the slide (technological feasibility)
Every component relies on existing, proven technology: push alerts and smartphone apps, discrete-event simulation of stroke pathways, and health-economic models of time to treatment. The novelty is in combining them, not in a technological breakthrough. Main technological risks: (1) integration with hospital systems (EHR, PACS, on-call rosters); (2) alert fatigue if escalation is not smart; (3) regulatory classification; (4) existing patents on alert escalation. **Feasibility: high**, unlike the ice idea in the lecture example.

### ScienceDirect keywords (for the manual search with the JCE login)
- `"stroke" AND "alert" AND "escalation"`
- `"alarm fatigue" OR "alert fatigue" AND "clinical decision support"`
- `"discrete event simulation" AND "stroke"`
- `"digital twin" AND "hospital" AND "emergency department"`
- `"door-to-needle" AND "quality improvement"`
- `"cost-effectiveness" AND "time to treatment" AND "thrombectomy"`
Filters: Review articles + Research articles, years 2024-2026.

### AI prompt for part (a) (save a screenshot for Appendix C)
"Below is a proposal. Examine it only on technological feasibility. Rely only on academic sources and cite them in full (authors, year, journal, DOI). Say explicitly when you cannot find a source. [paste section 2]"
