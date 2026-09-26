# Mission: Impossible — Detective Reasoning Dataset

## What this is
A 30-case reasoning-game dataset built from the major missions represented in the project.
The mission table is film-derived. Clues, candidate decoys, question wording, and event abstractions
are intentionally adapted for a detective/reasoning game; they are NOT movie dialogue or transcripts.

## Files
- missions.csv — original case-level mission data
- case_index.csv — player-facing case catalog with difficulty
- suspects_and_subjects.csv — named actors/subjects plus controlled game decoy hypotheses
- clues.csv — 8 reasoning clues per case
- events.csv — 6 abstract event beats per case
- questions.csv — 5 player questions per case
- answer_key.csv — solution summaries; keep this out of the player-facing UI

## Suggested app flow
1. Select a case.
2. Show mission objective and initial evidence.
3. Reveal clues progressively.
4. Let the player identify a subject/hypothesis.
5. Ask for supporting clues and event order.
6. Collect confidence + written reasoning.
7. Score evidence selection, timeline, contradiction detection, and final conclusion.
8. Show the answer only after submission.

## Important modeling note
For missions that are not literal whodunits, "suspect" should be interpreted as a candidate explanation,
actor, target, or hypothesis. The game should test evidence-based reasoning rather than pretending every
mission has a hidden murderer/traitor.

## Suggested scoring
- 30% conclusion
- 25% evidence selection
- 20% timeline reconstruction
- 15% alternative/false-lead handling
- 10% confidence calibration

The answer key is a concise solution summary. A future version can replace it with machine-readable
claim/evidence mappings for automated scoring.
