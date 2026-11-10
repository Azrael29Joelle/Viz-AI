# Viz-AI: Technology Venture Project

Team project for the course **ניהול מיזמים טכנולוגיים** (Management of Technological Ventures, 100997101/2/3), Dr. Elvira Bar, JCE.
Over the semester we build a full **business plan** for a technology venture and present it **in English**. Every team member presents a part.

---

## The venture

**Inspiration:** [Viz.ai](https://www.viz.ai) is an AI care-coordination company. It detects suspected stroke (large vessel occlusion, LVO) on CT scans and alerts the stroke team.

**Problem:** in a stroke every minute counts. Without treatment, an estimated 1.9 million neurons die per minute [Saver 2006; a modelled estimate]. Patients transferred between hospitals wait a median of **121 min** before they even leave the first hospital, and longer waits mean worse outcomes [Royan et al., *Lancet Neurol.* 2026]. An alert to the on-call doctor does not always get an answer in time. Hospitals also struggle to see where the minutes are lost.

**Our solution:** a web dashboard and mobile app that **complements Viz.ai**:

| # | Component | What it does |
| --- | --- | --- |
| 1 | **Escalation engine** | If the on-call specialist does not acknowledge an alert within a set time, it moves to the next doctor in line |
| 2 | **Door-to-treatment dashboard** | Shows where minutes are lost between arrival, scan, decision and treatment |
| 3 | **Hospital digital twin** | A discrete-event simulation that tests changes to the care pathway (staffing, on-call order) before they are made |
| 4 | **ROI calculator** | Turns minutes saved into money. It doubles as the base of our financial plan |

> We do **not** claim that Viz.ai lacks escalation; that is not verified (see issue #11). The prototype uses synthetic or public data only.

---

## Team

| GitHub |
| --- |
| [@Azrael29Joelle](https://github.com/Azrael29Joelle) (team leader) |
| [@doaa-ab](https://github.com/doaa-ab) |
| [@HiBA-Kl](https://github.com/HiBA-Kl) |
| [@cleopatraka](https://github.com/cleopatraka) |

## How we work

- **Task board:** [Viz.ai Venture – Presentation](https://github.com/users/Azrael29Joelle/projects/3). Every task is an issue in **Todo**.
- **Tasks are not pre-assigned.** Pick an issue, assign yourself, and move it to *In Progress*, then *Done*. See issue #1.
- Try to pick tasks whose slides you will present. The syllabus says **everyone speaks**.
- Labels show the area: `area: deck & coordination`, `area: literature`, `area: tech feasibility`, `area: business`, `area: finance`, plus `sciencedirect`, `needs-verification` and `slide`.

## Milestones (from the syllabus)

| Milestone | What | Format |
| --- | --- | --- |
| **M1: Midterm 1** | Theory: the problem (backed by literature), the technological solution, a block algorithm (rubric 2.1-2.7) | 4-5 slides, 5-7 min, no reading from slides. Feedback only, no grade |
| **M2: Midterm 2** | Marketing plan (rubric 3.1-3.7) | 4-5 new slides, but present the whole deck so far: 10-12 min, everyone speaks |
| **M3: Final** | The full business plan | Max 15 min, 13-14 content slides + 3-5 min Q&A. Plus a half-page executive summary, Excel financial statements, IEEE bibliography and an AI prompt appendix |

Course dates: TBD (add them to the milestones).
The full course requirements are summarized in [`docs/course-requirements.md`](docs/course-requirements.md).

---

## Research & reports

| File | What it is |
| --- | --- |
| [`docs/research/VizAI_Project_Research.md`](docs/research/VizAI_Project_Research.md) | The main research file: the venture, the 11 ideas we considered, claims to verify, the technological feasibility findings, and search keywords |
| [`docs/research/ScienceDirect_Literature_2026-11-09.md`](docs/research/ScienceDirect_Literature_2026-11-09.md) | 15 ScienceDirect papers (2024-2026) with checked DOIs, summaries, why each matters, and an IEEE reference list |
| [`docs/research/article-summaries.md`](docs/research/article-summaries.md) | Summaries of the two Viz.ai papers Doaa found |
| [`docs/reports/Study2_Murray2020_AI_Stroke_LVO_summary.pdf`](docs/reports/Study2_Murray2020_AI_Stroke_LVO_summary.pdf) | Summary of Murray et al., "AI to diagnose ischemic stroke and identify LVO: a systematic review," *JNIS* 2020 |

### Key findings so far
- **AI alerts speed up the workflow:** the Viz.ai meta-analysis (12 studies, 15,595 patients) found shorter CT-to-treatment, door-to-groin and door-in-door-out times. It found **no significant change in clinical outcomes** [Sarhan et al. 2025].
- **The gain is in the notification step:** an independent meta-analysis of 38 studies found that AI shortens notification and door-to-puncture times [Zebrowitz et al. 2024]. Real-world AI sensitivity is lower than manufacturers claim [Kunst et al. 2024], so the human loop after the alert matters.
- **Transfer delays cost patients function:** a door-in-door-out time over 270 min gave 65% lower *odds* of thrombectomy [Royan et al. 2026].
- **The digital twin is feasible:** a Python discrete-event simulation of a stroke center cut door-to-needle time from 39.4 to 23.0 min [Koca et al. 2024].
- **ROI model:** Brainomix (a competitor) was shown to be cost-saving in NHS England, at £49 saved per patient [Naylor et al. 2026]. Thrombectomy saves about £2,297 per patient over 5 years [Balami et al. 2026].
- **Main risks:** alert fatigue, integration with hospital systems, regulatory classification, and existing patents on alert escalation.

### Corrections log
| Was | Now |
| --- | --- |
| Doaa summary 1 linked to PubMed 34417344 | The correct paper is Sarhan et al., *Transl Stroke Res* 2025: https://pmc.ncbi.nlm.nih.gov/articles/PMC12596299/ |
| "Above 4.5 h, the *chance* of thrombectomy fell 65%" | "65% lower *odds*" (aOR 0.35) |
| "Only 26% of transfers within 90 min" | Not in the Royan abstract; check the full text or drop it |

**Before citing any paper:** open it on ScienceDirect through the JCE library, check the numbers in the full text, and export the citation.

---

## AI use (required by the course)

The course **requires** critical use of generative AI, and **every use must be documented** with the tool name and the exact prompt (screenshots), in a separate appendix. Unreported AI use leads to a disciplinary committee.

Logged so far:
- **Perplexity / GPT:** the prompts in `VizAI_Project_Research.md` section 9 and the feasibility prompt in section 12.
- **Claude (Anthropic):** drafting the research file; searching the literature through the Crossref, PubMed and OpenAlex databases; setting up the GitHub issues and board; drafting this README.

Save a screenshot of every prompt you use for Appendix C (issue #4).
