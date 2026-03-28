# P01 · The Digital Twin Shell

**Section:** 01 — The Digital Twin Foundation

**Workflow step:** Step 1 of 4

**Current version:** v1.2

**Status:** ✅ Tested and approved

**Last updated:** March 2026

---

## 📌 Prompt Text (v1.2 — current)

```
Role: You are a Lead AI Architect and High-Performance Sports Consultant. Your expertise lies in creating "Digital Twins" for elite athletes to solve match congestion risks.

Action: Create an image of a generic "Digital Twin" for a professional football player. Strictly follow the next requirements:
- Body must be straight (facing the camera). 
- Create only the image of the body, don't add any boxes with invented data.
- Use a professional blue color highlighting every muscle in the body.

Context: This image will serve as a proposal for clubs in La Liga and the Premier League. We are in the middle of a congested season (3 games in 10 days). This "Digital Twin" must be a high-fidelity representation of a professional football player.

Constraints:
- Don't create a Dashboard, Only the body of the Digital Twin.
- No background, emphasising more in the digital twin architecture.
```

---

## 🏢 Intended Workflow or Task

This prompt is the Visual Foundation of the consultancy proposal.

**Trigger:** Initial presentation to club stakeholders (Coaches, Owners)

**Actor:** Sports Tech Consultant (generates visual asset)

**Timing:** Pre-analysis phaseNext step: P02 (Physical Pillar) overlays real-time biometric data onto this shell


```
Kick-off → [P01 runs] → Visual Shell Created → P02/P03/P04 Data Overlays
```

---

## ❗ Problem Being Solved

Performance departments struggle to communicate complex data to non-technical stakeholders (Coaches/Board Members).

Pain points addressed:

- Data fatigue from spreadsheets and raw GPS exports

- Lack of a unified visual "Source of Truth" for player health

- Difficulty in visualizing the "Body" behind the biometric numbers during congested fixtures

---

## ⚡ Automation Potential

**Level: Medium**

| Dimension | Assessment |
| :--- | :--- |
| Repetitiveness | `High` &nbsp; - &nbsp; Used as the base for every player profile |
| Human judgment needed | `Low` &nbsp; - &nbsp; Visual approval only |
| Integration possibility | `Medium` &nbsp; - &nbsp; Could be used as a dynamic UI element |

**Human-in-the-loop role:** Consultant reviews image for anatomical accuracy and brand alignment before presenting to the club.

---

## ⚠️ Risks and Limitations

| Risk | Level | Mitigation |
| :--- | :--- | :--- |
| Hallucination of Data Artifacts | `Medium` | System flags output if text is detected; re-run with higher negative prompt weighting. |
| Generic Anatomical Output | `Low` | Human-in-the-loop review by Lead Sports Scientist to ensure alignment with athlete's actual build. |
| Confidential Data Exposure | `Low` | Prompt explicitly excludes names/logos; integration passes only anonymized Player IDs. |
| Tone/Style Mismatch | `Low` |  Scoped for Performance Dept; use `P09` template for Executive-level visuals. |
| Placeholder Malformation | `Medium` |  Validate all player metrics in the Sports Management System before the prompt runs. |


**Overall Risk Rating: LOW** — The prompt is suitable for near-full automation within a professional football club's workflow, requiring only lightweight human review for visual accuracy.

---

## 🔄 Version History

### v1.0 — Initial Draft

**Date:** March 10 2026

**Prompt:** `Create a digital version of a football (soccer) player.`

**Output:** <img width="1408" height="768" alt="Gemini_Generated_Image_6xvg0y6xvg0y6xvg" src="https://github.com/user-attachments/assets/27259c17-88b3-4362-b9de-a5d6e49f8424" />

**Result:** Unusable action shot; too much background noise; looks like a video game.

**Observed effect:** Generated an artistic illustration rather than a functional tool; the dynamic pose makes it impossible to use for data overlays.

**Lesson learned:** Generic prompts without a defined Role or Task default to "Entertainment" mode; high-performance tools require specific structural constraints.

### v1.1 — Added RACE framework

**Date:** March 11 2026

**Prompt:** Added "Lead Sports Scientist" role and 5 data pillars, we ended up deciding that data pillars will be added later on.

**Output:** <img width="1408" height="768" alt="Gemini_Generated_Image_6turqh6turqh6tur" src="https://github.com/user-attachments/assets/e073facf-8399-44f4-b803-aa149b6baf89" />

**Result:** High visual quality, but "baked-in" hallucinated data (e.g., fake VO2 max) made it non-functional for real-time use. Not what we wanted right now.

**Observed effect:** The AI "hallucinated" fake data points and baked them into the image, rendering the asset non-functional for real-time data integration.

**Lesson learned:** Defining too many features in a single prompt causes "Dashboard Overload"; the visual shell must be separated from the data layer to remain modular.

### v1.2 - Added constraints and exclusions ✅ Current

**Date:** March 12 2026

**Change:** Added negative constraints ("Don't create a Dashboard, Remove background") and fixed body orientation.

**Output:** <img width="468" height="255" alt="Digital Twin Architecture" src="https://github.com/user-attachments/assets/335d2e73-b88e-41c6-bb4c-c04dda76d820" />

**Result:** A clean, professional muscular map ready for modular data integration.

**Observed effect:** Produced a consistent, high-fidelity shell that is "data-ready" for the subsequent overlay prompts in the library.

**Lesson learned:** Explicit exclusion clauses (negative prompting) and specific orientation instructions are essential to prevent AI hallucination in professional technical assets.

---

## 📊 A/B Test Results

| Criteria | v1.0 | v1.2 |
| :--- | :---: | :---: |
| Instruction adherence | `0.5 / 5` | `5 / 5` |
| Visual clarity | `4 / 5` | `4.5 / 5` |
| Completeness (prompt coverage) | `0.5 / 5` | `5 / 5` |
| Professional relevance | `1 / 5` | `4.5 / 5` |
| Send-ready without edit | `0 / 5` | `4 / 5` |
| **Overall** | **`1.2 / 5`** | **`4.6 / 5`** |

---

## 🔗 Related Prompts

- **Next in chain:** P02 — The Physical Pillar (Injects biometric and GPS data onto the shell)

- **Also uses:** P03 — Technical & Tactical Pillars (Injects technical and tactical data onto the shell)

- **Also uses:** P04 — Cognitive & Emotional Pillars (Injetcts cognitive and emotional data onto the shell and finalises the "Digital Twin".
