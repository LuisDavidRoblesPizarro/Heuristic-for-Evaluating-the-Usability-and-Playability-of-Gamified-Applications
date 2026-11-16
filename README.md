# A Heuristic Proposal for Evaluating the Usability and Playability of Gamified Applications: An Educational Case Study

**Manuscript: IEEE Latin America Transactions — Submission ID: 11066**

This repository contains the data and scripts needed to reproduce the results reported in the paper. It covers the two literature reviews, the analysis of existing heuristics, the proposed and refined heuristic sets, and the expert evaluation of the case study.

## Authors
- Juan Marcos Altamirano
- Claudia Zapata Del Río
- Luis David Robles Pizarro
- Gloria Baños Díaz
- Víctor Enrique Chiroque Landayeta

All authors are with the Pontificia Universidad Católica del Perú (PUCP), Lima, Peru.

## Summary of the study
The study follows a six-stage methodology for developing usability heuristics: exploratory, descriptive, correlational, explicative, evaluation, and refinement. A systematic literature review identified 60 heuristics in 9 primary studies. Those heuristics were correlated with Nielsen's heuristics and other traditional sets, which produced a preliminary proposal of 12 heuristics. Three experts applied the proposal to a gamified mobile application for Spanish reading comprehension used by PUCP university students. After the experts' feedback, the set was refined into a final proposal of 14 heuristics.

## How to reproduce the results

The results can be reproduced with the two Excel files in this repository.
They open in Microsoft Excel, Google Sheets, or LibreOffice Calc. No additional software is needed.

### 1. `Heuristics_Catalog.xlsx`: the heuristics evaluated

| Sheet | Content | Paper |
|---|---|---|
| `Preliminary Heuristics (H1-H12)` | The 12 heuristics applied by the experts, with their associated gamified elements. | Table VII |
| `Refined Heuristics (H1-H14)` | The final 14 heuristics after expert feedback, with a brief description. | Table IX |

Use the IDs H1–H12 to match each heuristic with the ratings in `Expert_Evaluation.xlsx`.

### 2. `Expert_Evaluation.xlsx`: the expert ratings and Table VIII

| Sheet | Content |
|---|---|
| `Experts` | The three anonymized evaluators (E1–E3) and their professional roles. |
| `Ratings` | Source data: 180 scores (3 experts × 12 heuristics × 5 criteria) on a 1–5 Likert scale (rows 4–183). The table in columns I–J defines each criterion. |
| `Evaluation` | Mean score per heuristic and criterion, computed with `AVERAGEIFS` from `Ratings`. |
| `Frequencies` | Number of experts who chose each value (1–5) per heuristic and criterion, and the resulting weighted mean. |

### 3. Steps to reproduce Table VIII

1. Open `Expert_Evaluation.xlsx` and go to the `Ratings` sheet to review the individual scores.
2. Go to the `Evaluation` sheet. Each cell is the average of the three experts' scores for one heuristic (row) and one criterion (column), for example:
   `=AVERAGEIFS(Ratings!$E$4:$E$183, Ratings!$C$4:$C$183, $A4, Ratings!$D$4:$D$183, C$3)`
3. Compare the `Evaluation` sheet with Table VIII of the paper. All 60 values match (rounded to two decimals).
4. Optionally, open the `Frequencies` sheet to see the distribution of scores behind each mean. The weighted mean in column I equals the value in `Evaluation`.
