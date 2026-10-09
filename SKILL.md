---
name: whitebox-prompt-skill
description: Use when writing or auditing model-neutral, shot-by-shot prompts from whitebox, clay, proxy, previs, Blender or Unreal reference videos, including shared prompts for fair video-generation comparisons.
metadata:
  version: "3.1.0"
---

# whitebox-prompt-skill

Turn a whitebox video into a model-neutral six-section prompt. The video governs
action, space, camera and time; supplied appearance references govern their assigned
visible attributes. Describe a coherent finished world, including the environment.
Do not choose a generator or require appearance images before beginning.

## Authoring

Read [whitebox workflow](references/whitebox-workflow.md) before drafting or auditing.
Apply its phase-level shot contract and evidence-sufficiency gate. Record
`complete_storyboard` or `evidence_limited` outside copy-ready prose;
critical unverified motion/camera evidence means `pending_review`, not frozen.
For appearance evaluation, select a declared [visual target](references/visual-target.md).

1. Inspect actual media and establish stable roles, meaningful events, key props,
   real cuts and ending. Filenames are not visual evidence. Report unreadable or
   partial evidence rather than inventing a complete scene.
2. Separate observed structure, supplied target design and permitted completion.
   Assign each reference its role, inherited attributes and excluded attributes;
   a portrait supplies appearance, not its backdrop or pose.
3. Write the six sections below. Define who/what, summarize the clip-level event,
   then describe its visible execution shot by shot. Keep prop ownership and state
   changes explicit. Do not move later discoveries or off-screen backstory into
   the shot schedule.
4. Cover all visible environment surfaces and the final frame under the shared
   target policy. Unknown materials need not stay unfinished; allowed design
   choices are target choices, not recovered observations.
5. Audit source bindings, shot coverage, uncertainties and consistency. Keep the
   copy-ready prompt separate from evidence notes and execution configuration.

## Output contract

Use these six semantic sections in order, with ordinary-language headings in the
user's chosen language:

```text
主体定义：
内容概述：
保留与替换要求：
详细分镜描述：
整体声景：
画外配乐：
```

This is a local authoring convention, not an official conference or universal model
format. Preserve detailed coverage of every verified shot; action phases within a
continuous view are not new cuts. Use stable natural-language role names, not
endpoint tokens, asset tags or retention enums. No model names, inference settings
or model-specific length quotas belong in the prompt.

Unknown sound remains unspecified, not automatically silent. Optional semantic
enrichment may supply verified prop names and narrative context only when authorized;
record its sources separately and do not represent it as whitebox-only understanding.
See [neutral example](references/neutral-example.md) for video-only authoring and
[scene record](references/scene-contract.md) when provenance needs a saved record.

## Fair comparison

Freeze one prompt per source and reuse identical text across compatible generators.
Read [benchmark protocol](references/benchmark-protocol.md) for multi-model, detail-level
or no-video comparisons. Keep common inputs and completion policy fixed; disclose
unsupported modalities instead of silently dropping or converting them.

This skill produces and audits semantic prompts only. It contains no model-specific
adapter, API schema, deployment recipe or inference validator. Actual media ingestion
and generated fidelity require separate execution checks. Reference inspiration is
documented in [sources](references/sources.md).
