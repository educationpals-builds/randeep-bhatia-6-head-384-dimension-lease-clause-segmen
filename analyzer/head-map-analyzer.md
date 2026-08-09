# The Head-Map Interrogator

> The Head-Map Interrogator

Worked example domain: 6-head, 384-dimension lease clause segmenter, launch pushed past fiscal year-end; two retrains planned in the gap, each of which re-learns every head's W_Q/W_K/W_V and therefore re-draws every subspace from scratch; no per-head map opened since the head count was chosen

## Spec
The analysis-suite artifact: takes a batch of inputs plus returned attentions, emits the routine's four per-head measurements for every head, the review card, and a pass/flag verdict against the learner's thresholds.

## Learner field bag
- **__desk_active_time_ms**: 404058
- **__desk_reached_compile**: true
- **__desk_reached_index**: 3
- **__desk_scenario_blurb**: The same clause tool still joins clauses, but launch slipped to later this year and everyone looked away. Rosalind Achterberg wants each head checked on its own now, while there is slack, not during the launch rush.
- **__desk_scenario_id**: s2
- **__desk_stage_index**: 3
- **__desk_view**: compile
- **__desk_wall_clock_ms**: 1329067
- **crack_findings**: {"slices_too_thin_to_hold_a_pattern":{"verdict":"pass","note":"clear — per-head dims unchanged from launch build, no evidence of thinning"},"heads_that_are_copies_not_colleagues":{"verdict":"fail","note":"heads 2 and 5 show cross-head similarity 0.94 on flattened per-head maps over 20 lease sentences"},"no_head_owns_the_relationship_you_need":{"verdict":"fail","note":"no head exceeds 0.3 attention mass on the clause-boundary token across the 20-sentence sample"},"the_stitch_flattens_the_spectrum":{"verdict":"pass","note":"clear — merged output retains distinct per-head peaks in the sampled runs"},"no_single_head_map_ever_rendered":{"verdict":"pass","note":"clear — every head's map rendered and was inspected individually this pass"}}
- **cycle_verdict**: Missed it initially — head 7 sat at 0.34, just under the old 0.35 threshold's rounding, letting the decay through the first pass; catching it on re-review cost an extra day and forced tightening the threshold to 0.4.
- **evidence_rule**: Reviews must include a stratified sample of 100 inputs (half short clauses, half nested clauses), per-head boundary accuracy numbers, and the raw attention maps attached to the audit doc.
- **review_cadence**: Trigger the audit on retrain, pruning, or architecture edits, and never let more than eight weeks pass without one even if nothing changed.
- **reviewer_rotation**: Rotation is: model engineer proposes findings, a QA reviewer outside the training team verifies, and a product owner confirms the fix matches the original clause-merging complaint.
- **severity_note**: Feed the clause merger a contract sentence with two 'unless' provisos in a row; the merged-head map blends both conditions into one clause boundary, so the summarizer drops the second exception, and the paralegal signs off on terms that no longer hold.
- **ship_call**: Ship with conditions: Rosalind's per-head checks run before the next retrain, not blocking today's release, and the model engineer owns confirming the checks land before launch week arrives.
- **specimen**: 6-head, 384-dimension lease clause segmenter, launch pushed past fiscal year-end; two retrains planned in the gap, each of which re-learns every head's W_Q/W_K/W_V and therefore re-draws every subspace from scratch; no per-head map opened since the head count was chosen
- **specimen_source**: Live traffic for Clause merging, no ship date yet: pulled from the same stream that drives ~2,400 lease pages/week today, expected 3,500 after launch — Model engineer owns the cut.
- **specimen_stakes**: A merged clause puts a repair obligation on the wrong party in a summary a partner signs; because each retrain re-derives every head's projection matrices, whatever individuation I verify now is a claim about this checkpoint's spectra only
- **specimen_text**: 6-head, 384-dimension lease clause segmenter, launch pushed past fiscal year-end; two retrains planned in the gap, each of which re-learns every head's W_Q/W_K/W_V and therefore re-draws every subspace from scratch; no per-head map opened since the head count was chosen
- **standard_line**: Separated means: at least one head places meaningful mass across a clause boundary, no head pair is near-identical under cross-head comparison, and the same two facts still hold after each of the two planned retrains rather than being re-argued from the stitched score
- **top_crack**: slices_too_thin_to_hold_a_pattern
- **usage_reality**: ~2,400 lease pages/week today, expected 3,500 after launch; 48-token average sentences, nested 'provided that', OCR noise on the 1990s scans
- **watch_tripwire**: Track per-head clause-boundary attention entropy on a weekly sample; if any single head's entropy drops below 0.35 the model engineer gets flagged and it posts to the model-health dashboard.
