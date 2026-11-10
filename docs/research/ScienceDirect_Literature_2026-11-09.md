# ScienceDirect literature pack: Viz.ai venture

Found 2026-11-09. Every paper below is published by Elsevier, so it is on ScienceDirect. Search filter: 2024-2026.
Each DOI was checked in Crossref, and each summary comes from the published abstract (PubMed or OpenAlex).

**Before you cite a paper:**
1. Open it on ScienceDirect through the JCE library.
2. Check the numbers against the full text; these summaries come from abstracts only.
3. Use "Export citation to text" for the reference list.

**AI use:** these papers were found with Claude (Anthropic) using the Crossref, PubMed and OpenAlex databases. Add this to Appendix C (syllabus, appendix C).

Rubric sections (מחוון) referenced below: 2.1 problem and its size, 2.2 technology, 2.7 IP and barriers, 3.2 market, 3.3 competitors, 4.2 financial assumptions.

---

## A. Problem and AI in stroke (rubric 2.1, 2.2)

### A1. Royan et al. 2026, *The Lancet Neurology* (research article) **(headline paper for the problem slide)**
- **Study:** 22,410 patients transferred between hospitals for thrombectomy (US GWTG-Stroke registry, 2019-2023).
- **Finding:** median door-in-door-out (DIDO) time was **121 min**. Compared with ≤90 min, a DIDO time over 270 min gave **65% lower odds of receiving thrombectomy** (aOR 0.35) and worse disability at discharge (aOR 1.70).
- **Authors' conclusion:** system-level strategies to cut DIDO time are essential.
- **Why we use it:** minutes lost in transfer coordination cost patients function. This is the pain our escalation engine targets.
- **Correction to our earlier notes:** these are "lower *odds*", not "65% lower chance". The "only 26% within 90 min" figure does not appear in the abstract, so check the full text before using it.
- **Related:** a comment on this study, Chan et al., "Reducing door-in-door-out time to improve stroke outcome," *Lancet Neurol.* 2026, doi:10.1016/S1474-4422(25)00495-8.

### A2. Zebrowitz et al. 2024, *Intelligence-Based Medicine* (systematic review + meta-analysis, open access)
- **Study:** 38 studies (2019-2023) comparing AI-assisted with non-AI LVO detection.
- **Finding:** AI was associated with shorter triage time (OR 0.39), door-to-intervention-notification time (OR 0.30) and door-to-puncture time (OR 0.50), all significant. CT-to-puncture and door-to-CTA times were **not** significant.
- **Why we use it:** an independent review, not Viz.ai-specific, showing that the gain sits in *notification*: the communication step.

### A3. Kunst et al. 2024, *Journal of the American College of Radiology* (research article)
- **Study:** real-world test of two FDA-cleared LVO triage-and-notification algorithms at two stroke centers (704 and 642 cases).
- **Finding:** the manufacturers reported sensitivity of 97% and 87.8%. In real use, sensitivity for the main vessels (ICA/M1) was 85.3% and 90.7%, and dropped to about 60% when all proximal vessels were included. Some scans produced no AI result at all.
- **Authors' conclusion:** there are gaps in the *detection and communication* of treatable LVOs.
- **Why we use it:** an honest limitation slide. AI detection is not perfect, so the human loop after the alert matters.

### A4. Srinivasan et al. 2024, *Journal of Stroke and Cerebrovascular Diseases* (research article, free full text on PMC)
- **Study:** 29 spoke hospitals in a hub-and-spoke telestroke network (South Carolina, 2015-2022).
- **Finding:** hospitals with a stroke coordinator and/or certification had door-to-needle times of 57-61 min, against 81 min with neither. The effect was strongest in small and rural hospitals.
- **Why we use it:** coordination, not only technology, drives speed. Our product is a coordination layer, aimed at hospitals with few resources.

### A5. Sarhan et al. 2025: the Viz.ai meta-analysis (Doaa's summary 1)
- The full paper is in *Translational Stroke Research* (Springer, PMID 40335883). A version also appears in *Brain and Spine* (Elsevier) 2025, doi:10.1016/j.bas.2025.105536; that one is probably a conference abstract, so check it.
- **Confirmed from the abstract:** 12 studies, 15,595 patients. CT-to-EVT time SMD -0.71, door-to-groin SMD -0.50, DIDO time SMD -0.49, all p<0.001. No significant change in clinical outcomes.
- This confirms Doaa's summary. Her link should be https://pmc.ncbi.nlm.nih.gov/articles/PMC12596299/ (issue #5).

---

## B. Technological feasibility (rubric 2.2, 2.7)

### B1. Koca et al. 2024, *Journal of the Neurological Sciences* (research article, open access) **(the digital twin is proven feasible)**
- **Study:** a discrete-event simulation of the full acute stroke process at a comprehensive stroke center, **written in Python**, built from a time-and-motion study. It simulated 500 patients 30 times and tested 9 process changes.
- **Finding:** combining all changes cut door-to-CT time from 14.2 to 10.1 min, door-to-needle time from 39.4 to 23.0 min, and door-to-groin time from 67.9 to 38.5 min (all p<0.001).
- **Why we use it:** this is exactly component 3 of our product, already shown to work. It also supports choosing Python for the simulation (rubric 2.2.2 asks us to justify the programming tools from the literature).

### B2. Hashemi et al. 2024, *International Journal of Medical Informatics* (systematic review, open access)
- **Study:** 50 studies on how clinical alerts and reminders are designed, using the MINDSPACE behavioural framework.
- **Finding:** alerts designed with behavioural effects (defaults, salience, messenger, norms) influenced clinical decisions **73% of the time**.
- **Why we use it:** design rules for escalation messages. Who sends it, how salient it is, and what the default action is all matter.

### B3. Sarma et al. 2026, *JACEP Open* (research article, open access)
- **Study:** an emergency department that moved from one-way paging to two-way secure chat.
- **Finding:** messages per resident per shift went from a median of 42 pages to 107 chat messages, consolidated into 28 threads.
- **Why we use it:** a risk slide point. Better channels can *raise* message volume, which feeds alert fatigue. Our escalation must be targeted, not just "more messages".

### B4. Wang et al. 2026, *Intensive and Critical Care Nursing* (systematic review + meta-analysis)
- **Study:** 16 studies, 4,084 ICU nurses.
- **Finding:** alarm fatigue is widespread. It was highest in junior nurses, on rotating night shifts, and **without alarm-management training** (pooled score 31.5 vs 25.9 overall).
- **Why we use it:** evidence that alert fatigue is real. Training and smart routing reduce it.

### B5. Chen et al. 2024, *Computer Methods and Programs in Biomedicine* (research article)
- **Study:** a machine-learning clinical decision support system (MedGuard) designed to cut irrelevant alerts and so reduce alert fatigue.
- **Why we use it:** shows machine learning can filter alerts. This is a possible future feature, smart escalation that learns who answers.
- **Read the full abstract before using any numbers.**

### B6. Menon et al. 2025, *Intelligent Hospital* (review, open access)
- **Study:** a review of digital twins in medicine, including optimization of healthcare systems.
- **Barriers:** data privacy, incompatible systems, cyber threats and regulation.
- **Why we use it:** belongs in the risks and barriers part of the feasibility slide.

### B7. Mezrich 2026, *Clinical Imaging* (commentary)
- "Closing the loop": radiologists should be cautious using electronic-record messaging for critical results.
- **Why we use it:** supports the need for *acknowledged* (closed-loop) alerts. This is a commentary, not a study, so cite it as an opinion.

---

## C. Business and ROI (rubric 3.2, 3.3, 4.2)

### C1. Naylor et al. 2026, *NeuroImage: Stroke* (research article, open access) **(main source for the ROI model)**
- **Study:** cost-effectiveness of **Brainomix 360 Stroke**, a Viz.ai **competitor**, across NHS England. The model covered 81,565 patients and was based on 5 years of real-world data from 26 hospitals.
- **Finding:** thrombolysis rose 8% and thrombectomy rose 44%. The software was dominant (cheaper *and* better): about £4M saved and over 1,700 extra QALYs, with a net monetary benefit over £38M. That is **£49 saved and 0.021 QALY gained per patient**.
- **Why we use it:**
  - (1) A template for our ROI calculator (decision tree + Markov model).
  - (2) A competitor slide fact: Brainomix has published cost-effectiveness evidence.
  - (3) Evidence that hospitals and payers can justify paying for stroke-AI software.

### C2. Balami et al. 2026, *Journal of Stroke and Cerebrovascular Diseases* (research article, open access)
- **Study:** cost-effectiveness of thrombectomy in real-world pathways (5 English centers, 5-year horizon).
- **Finding:** the procedure costs about **£6,135**. Thrombectomy saves about **£2,297 per patient** over 5 years against standard care.
- **Why we use it:** every patient our faster coordination gets to thrombectomy saves money. This is a direct input to the ROI model (rubric 4.2 assumptions).

### C3. Chodankar et al. 2025, *Journal of the Neurological Sciences*
- **Study:** cost of stroke treatment by demographic and clinical factors at a tertiary hospital (India).
- **Why we use it:** a cost-driver reference for the ROI model. **No abstract was available, so open the paper first.** We still need Israeli cost data.

---

## D. Corrections to our existing notes
| Note | Correction |
| --- | --- |
| Doaa summary 1 link | The paper is Sarhan et al., Transl Stroke Res 2025 (PMC12596299), not PubMed 34417344 |
| "Above 4.5 h, the chance of thrombectomy fell 65%" | Change to "65% lower *odds*" (Royan 2026, aOR 0.35). Median DIDO time is 121 min |
| "Only 26% within 90 min" | Not in the Royan abstract; check the full text or drop it |
| Koca PhD thesis 2024 | The same work is now a peer-reviewed paper (B1). Cite the paper instead |

---

## E. IEEE reference list (verify page and article numbers on ScienceDirect)

[1] R. Royan *et al.*, "Door-in-door-out times and outcomes in patients with acute ischaemic stroke transferred for endovascular therapy in the USA: a retrospective cohort study," *Lancet Neurol.*, vol. 25, no. 2, pp. 160–169, 2026, doi: 10.1016/S1474-4422(25)00478-8.

[2] E. Zebrowitz *et al.*, "The impact of artificial intelligence on large vessel occlusion stroke detection and management: A systematic review meta-analysis," *Intell.-Based Med.*, vol. 10, Art. no. 100161, 2024, doi: 10.1016/j.ibmed.2024.100161.

[3] M. Kunst *et al.*, "Real-world performance of large vessel occlusion artificial intelligence–based computer-aided triage and notification algorithms—What the stroke team needs to know," *J. Am. Coll. Radiol.*, vol. 21, no. 2, pp. 329–340, 2024, doi: 10.1016/j.jacr.2023.04.003.

[4] M. Srinivasan *et al.*, "The role of stroke care infrastructure on the effectiveness of a hub-and-spoke telestroke model in South Carolina," *J. Stroke Cerebrovasc. Dis.*, vol. 33, no. 6, Art. no. 107702, 2024, doi: 10.1016/j.jstrokecerebrovasdis.2024.107702.

[5] K. Sarhan *et al.*, "Automated emergent large vessel occlusion detection using Viz.ai software and its impact on stroke workflow metrics and patient outcomes in stroke centers: A systematic review and meta-analysis," *Transl. Stroke Res.*, vol. 16, no. 6, pp. 2258–2271, 2025, doi: 10.1007/s12975-025-01354-0.

[6] G. Koca, J. T. Blake, G. J. Gubitz, and N. R. Kamal, "Discrete event simulation model of an acute stroke treatment process at a comprehensive stroke center: Determining the ideal improvement strategies for reducing treatment times," *J. Neurol. Sci.*, vol. 468, Art. no. 123369, 2024, doi: 10.1016/j.jns.2024.123369.

[7] S. Hashemi, L. Bai, S. Gao, F. Burstein, and K. Renzenbrink, "Sharpening clinical decision support alert and reminder designs with MINDSPACE: A systematic review," *Int. J. Med. Inform.*, vol. 181, Art. no. 105276, 2024, doi: 10.1016/j.ijmedinf.2023.105276.

[8] D. Sarma, E. L. Leventhal, D. T. W. Chiu, B. A. Stenson, and L. A. Nathanson, "Changes in communication after transition from paging to collaborative text messaging," *JACEP Open*, vol. 7, no. 5, Art. no. 100482, 2026, doi: 10.1016/j.acepjo.2026.100482.

[9] K. Wang *et al.*, "Alarm fatigue levels and associated factors among intensive care unit nurses: A systematic review and meta-analysis," *Intensive Crit. Care Nurs.*, vol. 99, Art. no. 104608, 2026, doi: 10.1016/j.iccn.2026.104608.

[10] C.-Y. Chen *et al.*, "Ability of machine-learning based clinical decision support system to reduce alert fatigue, wrong-drug errors, and alert users about look alike, sound alike medication," *Comput. Methods Programs Biomed.*, vol. 243, Art. no. 107869, 2024, doi: 10.1016/j.cmpb.2023.107869.

[11] G. Menon *et al.*, "Digital twin technologies in medicine: The innovations, barriers, and future directions," *Intell. Hosp.*, vol. 2, no. 1, Art. no. 100043, 2025, doi: 10.1016/j.inhs.2025.100043.

[12] J. L. Mezrich, "Closing the loop – Radiologists should be cautious using EMR messaging for clinically significant communications," *Clin. Imaging*, vol. 134, Art. no. 110807, 2026, doi: 10.1016/j.clinimag.2026.110807.

[13] N. R. Naylor *et al.*, "The cost-effectiveness of an artificial intelligence software for stroke imaging and treatment decisions in English hospitals," *NeuroImage: Stroke*, vols. 1–2, Art. no. 100008, 2026, doi: 10.1016/j.ynist.2026.100008.

[14] J. S. Balami *et al.*, "Cost–effectiveness of mechanical thrombectomy for acute ischemic stroke: generalizability across implementation settings," *J. Stroke Cerebrovasc. Dis.*, vol. 35, no. 10, Art. no. 108730, 2026, doi: 10.1016/j.jstrokecerebrovasdis.2026.108730.

[15] S. Chodankar *et al.*, "Economic burden of stroke: Evaluating the impact of demographic and clinical factors on the cost of stroke treatment at tertiary care university hospital," *J. Neurol. Sci.*, vol. 480, Art. no. 125572, 2025, doi: 10.1016/j.jns.2025.125572.
