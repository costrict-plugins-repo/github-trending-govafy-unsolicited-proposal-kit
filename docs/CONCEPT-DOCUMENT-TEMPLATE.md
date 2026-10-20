# OKF v0.2 Concept Document Template

This reusable template is an explicit frontmatter exception until copied and instantiated as a durable concept document.

Copy the YAML block and body outline into the destination file.

Replace every placeholder.

Delete optional fields that lack evidence.

Never invent trust or freshness signals.

```yaml
---
type: "{{ARTIFACT_TYPE}}"
title: "{{DOCUMENT_TITLE}}"
description: "{{ONE_SENTENCE_40_TO_60_WORD_ROUTING_DESCRIPTION}}"
# Choose draft, stable, or deprecated.
status: "{{STATUS}}"
tags: ["{{TAG}}"]
generated:
  by: "{{ACTOR}}"
  at: "{{ISO8601_DATETIME_WITH_TIMEZONE}}"
# Optional local routing fields:
# Use canonical or reference only when the governing role is known.
# authority: "{{AUTHORITY}}"
# read_when:
#   - "{{OPERATIONAL_ROUTING_CONDITION}}"
# required_refs:
#   - "{{PATH_TO_MANDATORY_REFERENCE}}"
# canonical_for: "{{EXACT_GOVERNED_SCOPE}}"
# Optional Google OKF v0.2 evidence fields:
# resource: "{{CANONICAL_URI_FOR_UNDERLYING_ASSET}}"
# sources:
#   - id: "source-{{STABLE_SOURCE_ID}}"
#     resource: "{{SOURCE_URL_OR_PATH}}"
#     title: "{{SOURCE_TITLE}}"
# verified:
#   - by: "{{ACTUAL_VERIFIER_ACTOR}}"
#     at: "{{ACTUAL_VERIFICATION_TIME}}"
# stale_after: "{{EVIDENCE_BASED_YYYY_MM_DD}}"
---
```

```markdown
# {{DOCUMENT_TITLE}}

## Purpose

{{DOCUMENT_PURPOSE}}

## Content

{{DOCUMENT_CONTENT}}
```

When a body claim derives from `sources`, add a Markdown footnote whose `source-` prefixed label matches the source ID:

```markdown
The process requires the recorded approval.[^source-policy]

[^source-policy]: Approved policy
```

Use `human:<id>`, `<producer>/<version>`, or `process:<id>` for actors.

Use only `draft`, `stable`, or `deprecated` for lifecycle status.

Do not add `okf_version` to the instantiated concept.
