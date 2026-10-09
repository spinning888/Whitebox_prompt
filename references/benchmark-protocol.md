# Shared-input comparison protocol

Neutral wording is an experimental control, not proof of fairness or a universal
conference standard. State the comparison question and information available to
the author before freezing prompts.

## Construction access

Distinguish whitebox-only, supplied-brief and externally enriched authoring. Record
which detail levels, reference images, annotations and audio the author could see.
Do not silently consult original coloured footage, transcripts or evaluation targets.
Authorized external semantics are common released inputs, not observations recovered
from the proxy. Freeze them across all compared systems.

Author without generator identity, generated outputs or evaluation scores. Revisions
based on development outputs create a new prompt-bank version; assess on held-out
cases rather than presenting tuned cases as an untouched comparison.

## Shared prompt and media

For the same scene across coarse/medium/fine whiteboxes, establish one common
verified timeline and freeze one prompt. Extra geometry visible at one level must
not change the generation target for other levels. Record construction access;
level disagreement or unresolved critical action/camera evidence blocks freezing.
Select a shared [visual target](visual-target.md) before proxy-leakage evaluation.

- Freeze one semantic prompt per source and reuse its exact text across compatible
  generators. Fix language; translations preserve facts rather than reanalyzing media.
- For a pure detail-level study, reuse that prompt, appearance images and within-model
  settings across levels; change only the structural video. Verify temporal/spatial
  alignment and disclose which source level informed the shared prompt.
- Independent prompts or semantic compilation per level measure a combined pipeline,
  not the isolated effect of geometric detail.
- Keep target finish, allowed appearance completion and motion naturalization policies
  common. Do not give one system extra identity, prop or environment information.
- Text duplicating precise trajectories is an additional control channel. Keep its
  information budget consistent and label richer motion-caption conditions separately.

## No-video conditions

A no-video run receiving a video-derived caption is caption-conditioned, not free
of video-derived information. Do not leave unconditional references to missing media.
For an identical-text pair, use event-role descriptions and the same conditional
video-following clause in all arms. Record attachment wiring outside prose. If text
or task mode must change, disclose the changed comparison rather than claiming an
isolated video ablation.

## Input compatibility

Confirm each system actually consumes all supplied assets in their declared roles.
Unsupported video or appearance inputs are not silently discarded. Keyframe, depth,
pose, image-guide, crop or retiming conversions constitute distinct input conditions;
report the transformation and compare only under a stated protocol. This skill does
not implement those conversions or prescribe model-specific interface formatting.

Identical step counts are not equal compute. Save native execution settings, seeds,
output duration/resolution and hardware separately; define quality or compute budgets
before comparison. Check effective submitted text for truncation or semantic changes.

## Optional semantic compilation

If an intermediate representation or semantic compiler is used, preserve its inputs,
backend/version, analysis policy, raw response and effective output. Keep source access
fixed. A semantic rewrite after compilation is a separate corrected treatment, not
an invisible formatting operation. Predefine bounded retry/failure rules; retain all
attempts and do not select only favourable runs.

## Records and evaluation

Save prompt-bank version, stable sample/role IDs, ordered asset paths, source provenance,
effective text, settings, attempts and outcomes. Respect requests not to hash: direct
byte comparison can establish local equality; byte size alone cannot.

Assess structural following, appearance adherence, finished-environment quality and
temporal coherence separately. Report failures and repeated-seed variability. Static
prompt review, successful input ingestion and visual generation quality are different
evidence levels; none substitutes for the others.
