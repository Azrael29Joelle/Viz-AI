# Business model and ROI calculator (#13, rubric 3.7 + input to 4.1-4.6)

**Spreadsheet:** [`ROI_calculator.xlsx`](ROI_calculator.xlsx). Change only the blue cells on a yellow background in the *Inputs* sheet; everything else is a formula and updates by itself.

---

## 1. Business model (3.7)

| Question | Our answer |
| --- | --- |
| **Who pays?** | The hospital (stroke centre or its management), not the patient. In Israel: the hospital or the health-system group it belongs to |
| **Who uses it?** | On-call stroke doctors and nurses (the app), stroke-unit and hospital managers (the dashboard, the simulation, the ROI report) |
| **What do they buy?** | A yearly **software subscription (SaaS)** per hospital, plus a **one-time setup fee** for integration with hospital systems (FHIR where supported) and staff training |
| **Draft price** | **€40,000 per hospital per year** + **€15,000 setup**. These are our assumptions: we test them in the market survey (#14) and against competitors (#12) |
| **Why would they pay?** | The ROI calculator shows each hospital the value of the minutes it saves, using its own numbers |
| **Channel** | Direct sales to stroke centres, then the hospitals connected to them (hub and spoke). Later: a partnership with Viz.ai, since we add to its alerts |
| **Later revenue** | Simulation studies sold as consulting ("test your pathway before you change it"); more urgent pathways (e.g. pulmonary embolism) on the same escalation engine |

**Why a subscription:** hospitals already buy clinical software this way, and Viz.ai sells mainly through software subscriptions (search summary only, **not verified**, see the research file section 3). A subscription also pays for what we keep running: the cloud alert service, its uptime (KPI 99.9%) and support.

## 2. The ROI logic (one hospital, one year)

```
treated patients x share of alerts left unanswered  = patients affected
minutes lost per unanswered alert x share we recover = minutes saved per patient
patients affected x minutes saved per patient       = minutes saved per year
minutes saved per year x €309                       = health value of the minutes   [van Voorst 2021]
extra thrombectomies x £2,297                       = cash saving for the health system [Balami 2026]
(value - subscription) / subscription               = ROI
```

### Base case (the numbers in the spreadsheet today)

| Step | Value |
| --- | --- |
| Patients treated with thrombectomy per year | 120 *(assumption)* |
| Share of alerts not answered within 10 min | 20% *(assumption)* |
| Minutes lost per unanswered alert / share we recover | 30 min / 70% *(assumptions)* |
| **Minutes saved per year** | **504** |
| Health value (504 × €309) | **€155,736** |
| Patients' disability-free life gained (504 × 1.3 days) | **655 days** |
| Cash saving from 2 extra thrombectomies | €5,283 |
| **Total value per year** | **€161,019** |
| Cost: year 1 / from year 2 | €55,000 / €40,000 |
| **ROI year 1 / from year 2** | **193% / 303%** (about **€4 of value per €1**) |
| Payback in year 1 | about 4 months |
| **Break-even** | **130 minutes saved per year** (€40,000 ÷ €309), i.e. about 1 minute per treated patient |

### Scenarios (sheet *Scenarios*)

| | Cautious | Base | Optimistic |
| --- | --- | --- | --- |
| Alerts not answered in 10 min | 10% | 20% | 30% |
| Minutes lost per unanswered alert | 15 | 30 | 50 (the Susan story) |
| Share recovered | 50% | 70% | 85% |
| Extra thrombectomies per year | 0 | 2 | 5 |
| Minutes saved per year | 90 | 504 | 1,530 |
| Total value per year | €27,810 | €161,019 | €485,978 |
| ROI from year 2 | **−30%** | **+303%** | **+1,115%** |

The cautious case **loses money**. That is useful on the slide: it shows we did not only pick good numbers, and it gives the honest message, "we break even if we save about **130 minutes a year**, about one minute per treated patient." The pilot measures which case is true.

### What to say about the value (important)
- The **€309 per minute** is a *net monetary benefit*: health gained (QALYs) valued at €80,000 per QALY, over 5 years, in the Netherlands. It is **value of care for patients and the health system, not cash in the hospital's account**. Say "value of care", not "profit".
- Faster treatment does **not** raise costs: in van Voorst 2021 the 5-year costs barely changed (median −€15), and in Kunz 2020 lifetime costs were similar.
- The **cash** argument is the extra patients who reach thrombectomy in time: thrombectomy saves about **£2,297 per patient over 5 years** compared with standard care (NHS England) [Balami 2026].
- Figures come from different countries and thresholds. **Israeli cost data is still missing** (claim 10 in the research file).

## 3. Revenue for the financial plan (sheet *Revenue*, feeds #22)

| | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 |
| --- | --- | --- | --- | --- | --- |
| Paying hospitals (end of year) | 0 | 1 | 3 | 6 | 10 |
| Subscriptions | – | €40,000 | €120,000 | €240,000 | €400,000 |
| Setup fees | – | €15,000 | €30,000 | €45,000 | €60,000 |
| **Total revenue** | **–** | **€55,000** | **€150,000** | **€285,000** | **€460,000** |

Year 1 is build and test; year 2 is the pilot (2.4/2.5); 3 paying hospitals by the end of year 3 is objective 3b in the goals page. Costs (salaries from Cleo's staffing table in 2.5, cloud, regulatory advice) go into the cash-flow and P&L in #22.

## 4. Source check (done 2026-11-19 in PubMed / Crossref)

| Number | Status | Source |
| --- | --- | --- |
| €309 NMB and 1.3 disability-free days per minute faster; costs about unchanged (−€15) | **Confirmed in the abstract** | H. van Voorst *et al.*, "Quantified health and cost effects of faster endovascular treatment for large vessel ischemic stroke patients in the Netherlands," *J. NeuroInterv. Surg.*, vol. 13, no. 12, pp. 1099–1105, 2021, doi: 10.1136/neurintsurg-2020-017017 |
| Every 10 min earlier: 39 disability-free days, NMB +$10,593 (US, $100,000/QALY); similar lifetime costs | **Confirmed in the abstract** | W. G. Kunz *et al.*, "Public health and cost consequences of time delays to thrombectomy for acute ischemic stroke," *Neurology*, vol. 95, no. 18, pp. e2465–e2475, 2020, doi: 10.1212/WNL.0000000000010867 |
| Thrombectomy £6,135 per procedure; saves £2,297 per patient over 5 years | **Confirmed in the abstract** | J. S. Balami *et al.*, "Cost-effectiveness of mechanical thrombectomy for acute ischemic stroke: generalizability across implementation settings," *J. Stroke Cerebrovasc. Dis.*, vol. 35, no. 10, Art. no. 108730, 2026, doi: 10.1016/j.jstrokecerebrovasdis.2026.108730 |
| Median 102 min (pager) vs 169 min (EHR) to acknowledge urgent alerts | **Confirmed**, but small (48 alerts, 1 centre, stopped early, p = 0.15) | M. A. Dziadzko *et al.*, "Testing modes of computerized sepsis alert notification delivery systems," *BMC Med. Inform. Decis. Mak.*, vol. 16, Art. no. 156, 2016, doi: 10.1186/s12911-016-0396-y |
| Target: Stroke: door-to-needle **77 → 67 min (median)**; mortality 9.93% → 8.25% | **Corrected.** The research file said "74 → 59 (mean)"; the abstract gives medians 77 → 67 | G. C. Fonarow *et al.*, *JAMA*, vol. 311, no. 16, pp. 1632–1640, 2014, doi: 10.1001/jama.2014.3203 |
| Brainomix 360: £49 saved and 0.021 QALY per patient | **Not checked**: no abstract in PubMed or Crossref. Open it via JCE | Naylor *et al.*, *NeuroImage: Stroke*, vol. 1–2, Art. no. 100008, 2026, doi: 10.1016/j.ynist.2026.100008 |
| Price of competing stroke software per hospital | **Not found.** Ask in interviews (#14) and look for NHS/NICE documents | – |
| Number of thrombectomies per year in Israel | **Not found yet** | – |

## To do before the slide
- [ ] Replace the yellow assumptions with real numbers (hospital volumes, the survey answer on price)
- [ ] Find Israeli cost and volume data (Ministry of Health, Gertner Institute, Israeli stroke registry)
- [ ] One slide: business model on the left; ROI base case + break-even on the right; footnote "value of care, not hospital profit"
- [ ] Hand the *Revenue* sheet to whoever builds #22
