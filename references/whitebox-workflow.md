# Whitebox authoring workflow

Keep the original six-section method and detailed shot coverage. Output bindings,
preservation instructions and shot labels use ordinary language.

## Evidence

Inspect the supplied video with available media tools. Track duration, observed
coverage, stable figure/object roles, camera, real cuts and evidence confidence.
File names, model knowledge and three isolated frames cannot recover a complete
action/cut timeline. If media cannot be read, report that and do not invent a
scene-specific prompt. Partially visible evidence permits a limited draft, with
unobserved motion/timing kept out of the copy-ready text.

| Source, if supplied | Authority |
| --- | --- |
| Whitebox video | Supported blocking, action, space, camera and time |
| Appearance reference | Visible final identity, wardrobe, object/scene design |
| Explicit target instruction | Finished world, rendering style, light and sound |
| Authored/reviewed timeline | Actual cuts and action timing |
| Declared semantic annotation | Verified prop names, narrative context and reaction intent; not extra camera or action authority |

Video-only authoring is valid. Do not require pictures, a brief or a generation
model before drafting. Use neutral observed descriptions for anonymous figures
and ambiguous objects. A rectangular object does not automatically become steel,
a lab tray or a suitcase. Missing appearance information does not license actor
identity, demographics, outfit, emotion, additional props or a guessed background
as observed facts. An explicitly declared target or shared completion policy may
leave appearance choices to the generator; record them as choices, not observations.

## Evidence sufficiency and output status

In the authoring record distinguish direct observations, supported interpretations
(with their supporting observations), explicit generation targets, and unknowns.
An event such as "A transfers an object to B" establishes event roles, not the
first-frame holder, contact mechanics, response onset or holding duration.
"Follow the video's timing" is an instruction, not proof of verified timing.

Before drafting, build a common shot/action timeline from permitted evidence.
For each shot record its interval, framing/camera behaviour, initial spatial state,
action phases, interactions, end state and transition. Save source frames/time ranges
and uncertainty outside the prompt. Inspect densely near cuts, contact transitions
and rapid actions; overview contact sheets alone do not verify those boundaries.
Do not infer dolly versus zoom from subject size alone; state the observable change.

- `complete_storyboard`: every shot and critical action/camera phase has adequate
  evidence, including spatial continuity and ending. Supply verified intervals at
  the evidence's actual precision; approximate times are explicitly approximate.
- `evidence_limited`: only overall events or incomplete phases are supported. Write
  supported content and list missing fields outside the prose. An event synopsis
  is not a complete storyboard; do not manufacture phase durations.
- Unreadable media: `analysis_not_run`; no scene-specific copy-ready prompt.

For benchmark release, unresolved critical evidence sets `pending_review`.
Completeness is not release approval: record semantic review before `frozen`.

## Attribute-scoped reference contract

For each supplied asset record a stable ID, its function, the attributes it governs,
and attributes it must not transfer. Group larger bundles by function, not upload
order alone. Do not impose another service's asset-count limits.

| Assigned function | Inherit | Do not inherit unless separately authorized |
| --- | --- | --- |
| Structural whitebox video | Verified layout, blocking, events, contacts, camera and timing | Proxy surface finish, placeholder anatomy or lack of clothing as target appearance |
| Character appearance image | Visible identity and specified wardrobe/accessories of its bound role | Portrait pose, studio backdrop or portrait framing |
| Environment appearance image | Specified surface design, palette or lighting character | A conflicting room layout or camera |
| Composition reference | The explicitly assigned framing/layout attributes | Unassigned identity, wardrobe or story |
| Audio reference | Assigned voice, words, rhythm or ambience | Unspecified speakers, dialogue or visual events |

These are default scopes, not inherent properties of file types. One image may
have multiple declared roles. Resolve each attribute using its assigned source;
if two assigned sources conflict, flag the conflict before freezing rather than
silently favouring upload order. A requested layout change is a changed task, not
appearance completion. Keep role-to-image and proxy-to-role mappings explicit.

## Six-section output contract

Emit six sections once, in this order, using readable headings in the user's
language. The sections are the original semantic responsibilities, not mandatory
endpoint field names:

1. **Subject definitions / 主体定义**: bind stable people, relevant props and
   environment roles to their actual evidence sources. Define the whitebox's
   whole-video structural role separately from final appearance. Optional images
   govern only the visible appearance they supply; without them keep unknown
   identity, wardrobe and materials unspecified or explicitly free under the
   shared target policy, rather than claiming them as source observations.
   For key props include supported name/category, distinguishing appearance,
   initial holder/location, and narrative or interaction role when known.
2. **Summary / 内容概述**: state the target event, including
   duration and aspect ratio when verified or explicitly requested.
   Keep requested output properties distinct from source metadata. No native task
   prefix is needed; inference steps and architecture settings stay outside prose.
   Describe the clip's situation, event progression and endpoint, plus supported
   intent or reaction contrast. Do not substitute style adjectives or a list of
   walking/sitting/turning motions for what the scene is about.
3. **Preservation and replacement / 保留与替换要求**: describe, by defined role,
   the structure, action, contacts, camera, timing and supplied appearance that
   must persist, and the unfinished proxy appearance replaced by the target look.
   Include each asset's scope and any allowed completion. Use sentences instead
   of retention enums; do not promise measured fidelity.
4. **Detailed shot description / 详细分镜描述**: establish the visible environment
   under the already defined visual target. Describe every verified shot in order; a continuous
   shot can contain multiple action-phase paragraphs without invented cuts.
   Express narrative meaning as visible performance and prop-state changes in the
   appropriate shot, without repeating the synopsis or adding explanatory cutaways.
5. **Overall soundscape / 整体声景**: include analyzed source sound or explicitly
   declared target sound policy. Without either, record "not specified"; unknown
   sound is not a request for silence or permission to invent dialogue/foley.
6. **Non-diegetic music / 画外配乐**: state supplied audience-only music policy.
   Without one, record "not specified"; use "none" only when no score is actually
   requested. Keep this separate from sounds belonging to the scene.

Allocate content once: definitions own identity/appearance and the global visual
target; summary owns the clip-level event; preservation owns reference duties;
shots own temporal execution and local changes. Spend most scene-specific detail
on shots, not repeated preservation boilerplate. Unknown audio can simply say
"未指定" in each audio section; evidence notes stay outside the prompt.

The six-section shape is the user's chosen reusable method. Neutralizing syntax
keeps its content, scope and information density; it does not flatten it into a
brief synopsis. Detail follows the available evidence, not a forced word count.

## Role bindings, without native markers

Use stable names such as person A, person B, the carried object and the reference
video. A first-frame left/right cue is not a permanent identity after crossing
or cuts. Preserve who acts, who receives and which object persists.

Where an appearance image exists, say "person A's appearance follows the supplied
image, while their action and position follow the corresponding figure in the
reference video". Without an image, bind person A to the observed video role and
leave identity/wardrobe unspecified or free under the declared completion policy;
do not assert a specific identity or wardrobe as an observation without evidence.

Replace a retention token with its actual meaning: "preserve blocking, action
phases, spatial relationships, camera motion and timing; replace unfinished proxy
surfaces with the specified finished appearance". A requested relationship is
not proof that the renderer achieved it. Do not merely delete tags and lose the
binding/preservation instruction.

## Final world, not proxy leakage

Read [visual target](visual-target.md) when defining an appearance class or evaluating
proxy leakage. Broad "finished" language alone does not establish that standard.

Establish the supported final look in one or two sentences, then instantiate
visible final subjects, objects and scene surfaces. Positively describe intended
finished content instead of adding a large negative-prompt list. Preserve
legitimate white fabric, pale walls and grey finished props when actually specified.

When no final look is supplied, a declared bank-wide neutral policy may request
"a finished, physically plausible version of the reference scene". This is a
shared target instruction, not a source observation. It allows coherent finished
surface, lighting and appearance choices where unspecified, without asserting a
particular source material, room function, wardrobe or identity. Such choices must
not change object roles, layout, events or camera. Keep that policy identical
across models/levels, or omit it consistently. Do not infer a cinematic genre
from a whitebox or optimize style words for a particular generator.

Before drafting, inventory the visible environment: enclosing surfaces/open space,
openings, supporting surfaces, major props, depth/occlusion and relation to actors.
Name only verified elements; an unknown room is not automatically a café, corridor
or laboratory. The prompt must still state how ALL visible proxy surfaces become
the target world, including background-only views, openings and the ending.
When geometry is not recoverable, do not invent an inventory; record the limitation.

Keep three categories in the authoring record: observed structure; supplied target
design; unspecified attributes open to completion. With a photoreal target, request
coherent surface response, illumination and contact shadows across people, props
and environment rather than finished actors pasted onto an unfinished background.
Other declared styles use their own coherent finish; photorealism is not universal.
Without a scene image, exact background decor may remain free, but completion is
not optional when the target policy asks for a finished world. Do not add objects
or stories simply to make the description richer. Use only a few scoped exclusions
for known conflicts, not a generic negative-prompt catalogue. White/grey colours,
plastic or minimal sets are legitimate if they belong to the target design.

Keep declared macro trajectories, events, contacts and timing, while allowing
plausible local body/cloth motion under a common naturalization policy. Coarse
geometry does not establish detailed joints. Describe verified semantic action
phases, spatial changes and camera behaviour in full; caution must not suppress
available evidence. Numerical 3D paths/joint trajectories are a separate additional
control condition, not a requirement for detailed natural-language storyboards.

## Events, cuts and end coverage

For each shot, write its verified time range and initial framing/spatial state,
then consecutive action phases: onset, development, other subjects' responses,
visible contact or state transition, completion and end-state hold. Include only
applicable, observed phases; a landscape shot need not contain a handover. Give
phase time ranges and hold duration when verified, otherwise mark the missing timing
in the evidence record. Do not turn a plausible sequence into verified mechanics.
Describe camera movement and subject movement separately: direction, relative
positions, changes in framing, entry/exit/occlusion and relevant prop ownership.
At cuts state what changes in view and what continues in action/object state.
Cover the final frame without inventing stillness or off-screen retrieval.

The acceptance question is whether a reader can recover the supported execution
sequence, not merely name its overall event. If critical phases remain unknown,
deliver evidence_limited and pending_review rather than a nominal full storyboard.

### Narrative scope and key props

Keep the six sections; no seventh plot section is needed. Use three levels:
definitions establish entities, the summary establishes the clip-level event,
and shot descriptions establish its visible realization. A practical summary is
"initial situation → event/reaction → clip endpoint"; use only the parts supported
by the inputs. Plot-driven drama may have a turn; a demonstration, landscape or
simple handover need not have a hidden motivation, conflict or dramatic climax.

For each interaction-critical prop, track name/category, necessary appearance,
initial holder, handling/transfer and last visible state. Mention it again when
its state matters, not in every sentence. Unknown category is not an excuse to
omit visible shape, scale, material cues or grip; known category is not a reason
to invent contents, brands or counts. Avoid exact hand assignment when unverified.

When a supplied brief or permitted source establishes narrative intent, translate
it into modest compatible performance (attention, hesitation, surprise, urgency).
The reference still controls movement, contacts and timing. Context such as a
past outing does not request a flashback; an impending discovery does not happen
early; later dialogue or new characters must not enter this clip. Do not invent
off-screen prop retrieval, placement or transformation to bridge an occlusion.

### Optional semantic enrichment

Default video-only authoring remains valid and does not automatically retrieve
the original film, transcript or evaluation target. Use supplemental sources only
when the user or declared input protocol permits them. Verify an external match
against the actual clip; a filename, familiar plot or suggestive proxy shape alone
is insufficient. Save source URL/file, location/time, claims used and confidence
outside copy-ready prose. Unresolved identity stays descriptive or is flagged
for clarification; do not force a specific category into a freeze-ready prompt.

An authorized annotation can identify a crudely modelled prop more reliably than
its proxy shape. Record this semantic/geometry mismatch. The prompt may request
the confirmed object and plausible final form while preserving reference holding
position, approximate occupied space, role and event timing; it should not demand
both an incorrect rigid silhouette and incompatible final material behaviour.
Do not claim this resolves the model's conflicting visual conditioning.

External scene knowledge makes an enriched-input condition, not whitebox-only
automatic understanding. Freeze the same annotations across compared generators
and levels, and disclose their source access. Do not use target-video knowledge
silently to improve one model, one level or an evaluation target's scores.

For k verified internal cuts, describe k + 1 shots individually in section four.
Use natural labels such as "First shot" or "第一镜头", not native bracketed tags.
For every shot cover its starting state, visible final subjects/environment,
semantic events and relevant prop changes, camera/framing, and end state or
cross-shot continuity. Later shots explicitly preserve established role identities,
target appearance, object state and world continuity. The final shot covers the
remaining event and finished world through the final frame.

Pan, zoom, occlusion and action phases are not cuts. Within a continuous shot,
describe meaningful action phases as consecutive paragraphs, not new shots. Use
natural language for supported cuts, e.g. "At 4 seconds, the view cuts to ...";
map verified times after any declared retiming. Do not invent cut counts or exact
times. If cuts are unverified, keep six sections but label the output as an
evidence-limited draft outside the copy-ready text; do not certify full shot coverage.

## Language, length and sound

Use the six sections and individually covered shots above. A reference-generation
task tag, retention enum and 350–500-word model quota do not apply to neutral output.
Keep the original method's useful detail: positive final-world conversion, stable
bindings, semantic actions, state changes, local naturalization and continuity.
Keep the prompt as detailed as evidence allows; do not pad or shorten it just to
simplify formatting. Language is selected once per benchmark bank; translations share
the same facts rather than independent analyses.

Specific sound is included only from inspected audio or explicit common target policy.
Do not infer dialogue/music from frames. Exact supplied words stay exact; native
dialogue/speaker formatting is outside this authoring skill. Keep both audio
sections even when the appropriate entry is "not specified".

## Fair use

Compile one frozen prompt from the source, without target-generator identity,
model recipes, generated outputs or scores, and reuse its exact text across
models with the same supported input bundle. If an analyzer is used, keep its
analysis policy/backend/source access fixed across generators.

Independent captions of L1/L2/L3 compare captioner plus video, not pure detail;
a pure-detail study reuses one caption with disclosed construction access. NOV
with a video-derived caption is caption-conditioned NOV, not a source-video-free
baseline. These controls are separate from writing style.

For an identical-text NOV pair, name people by their described event roles and
keep attachment wiring outside the prose, or make the same video-following clause
conditional in all arms. A video instruction cannot refer unconditionally to
an absent input; merely deleting that clause would change the prompt condition.

Mechanical checks do not establish semantic fidelity. Provenance checks and manual
semantic review have distinct scope; neither alone verifies rendering. Respect a
user's no-hashing requirement: paths, ordered asset IDs, byte sizes and direct
byte comparisons can document pairing without computing digests.

## Preflight review

Check all six sections, stable role bindings, source/target/completion separation,
environment coverage, every verified shot and ending, and explicit audio status.
Check that the summary communicates the actual event, important props are named
or meaningfully described, prop ownership remains coherent, reactions occur in
the correct clip, and supplementary semantics are disclosed rather than guessed.
Check that timings do not fabricate evidence and that motion phases are not cuts.
Confirm every attached asset is actually consumed in its declared role. Save the
final effective prompt; truncation, silent asset loss and semantic adapter changes
invalidate a claimed shared-input comparison. This is authoring review, not proof
of a successful generation or a universal benchmark standard.
