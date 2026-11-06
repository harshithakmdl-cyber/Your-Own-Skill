# Project 16 Test Plan

## Test A — Fresh session
1. Open a brand-new chat.
2. Paste the full `skill.md`.
3. Upload `sample_input_1.md`.
4. Enter `/viva`.
5. Confirm the skill identifies the note topics and asks one question only.
6. Answer, then test `hint`, `skip`, `review`, and `finish`.

**Pass:** it starts without previous conversation context and follows one-question-at-a-time behavior.

## Test B — Three different inputs
Repeat the skill in a fresh chat for each file:
- `sample_input_1.md` — Thermodynamics
- `sample_input_2.md` — Database Fundamentals
- `sample_input_3.md` — Machine Learning Basics

**Pass:** questions and model answers match each input, not the previous topic. Record evidence in `results_template.md`.

## Test C — Baseline without the skill
1. Open another new chat.
2. Upload one sample input, preferably Database Fundamentals.
3. Do not paste `skill.md`.
4. Ask: “Make viva questions from this file and quiz me.”
5. Observe whether it asks one question at a time, scores consistently, supports commands, and provides a final report.
6. Compare with the skill-enabled run.

**Pass:** document specific differences. Do not claim the skill is better in a feature unless your tests show it.

## Screenshots
Capture:
1. Fresh session starting with detected topics and Question 1.
2. Feedback with score and model answer.
3. Final report.
4. One test using each of the three input files.
5. Baseline chat without the skill.
