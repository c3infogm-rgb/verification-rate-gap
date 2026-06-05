# The Verification Rate Gap

A minimal research-note companion repository for:

**The Verification Rate Gap: A Conceptual Metric for AI Development Risk**

This repository provides example artifacts for the **Verification Kit** architecture proposed in the paper.

The core claim is:

```text
R_dev 竏・max(0, G_rate 竏・V_rate)
```

Where:

- `G_rate` is the rate at which AI systems generate development outputs.
- `V_rate` is the rate at which those outputs can be reliably verified.
- The difference between them creates the **Verification Rate Gap**.
- Accumulated unverified outputs become **unverified debt**.

## Purpose

This repository is not a production system, certification program, or safety guarantee.

It provides a minimal, inspectable structure for:

1. fixing execution context;
2. recording verdicts;
3. preserving evidence references;
4. making uncertainty explicit;
5. enabling deterministic decision replay;
6. supporting third-party or BYO-AI audit as an auxiliary review layer.

## Verification Kit

A Verification Kit is a replayable evidence package.

It is not a narrative report.  
It is not a trust badge.  
It is not proof that an AI system is safe.

It is a structured package that allows another party to inspect, reproduce, or challenge the decision path of an AI-led development workflow.

## Minimal Repository Structure

```text
verification-rate-gap/
  README.md
  docs/
    implementation_note.md
  paper/
    README.md
  verification-kit/
    examples/
      run_manifest.example.json
      verdicts.example.jsonl
      summary.example.json
      conformance.example.json
      undefined_report.example.json
      evidence_digest.example.json
    schemas/
      run_manifest.schema.json
      verdict_record.schema.json
    prompts/
      auditor_prompt.example.md
```

## Claim Boundary

This repository claims:

- decision paths can be recorded;
- execution context can be fixed by a manifest;
- verdict records can support replay or challenge;
- evidence can be referenced through raw data, hashes, or digests;
- uncertainty can be represented as `HOLD` or `UNDEFINED`;
- a deterministic verifier can improve verification throughput.

This repository does **not** claim:

- AI systems are always correct;
- AI systems are absolutely safe;
- all unsafe outputs will be detected;
- evidence digests prove universal truth;
- BYO-AI audit is the source of truth;
- this repository constitutes certification or production readiness.

## Source of Truth

The source of truth for verification should be deterministic artifacts:

- `run_manifest.json`
- `verdicts.jsonl`
- evidence references or digests
- schema definitions
- verifier version and hash
- signatures or integrity proofs

Human-readable summaries and AI-assisted audit are secondary interfaces.

## BYO-AI / Bring Your Own Verifier

This repository supports a Bring Your Own Verifier model.

A receiving institution may use:

- its own command-line verifier;
- its internal audit pipeline;
- a human reviewer;
- a BYO-AI auditor using a standardized prompt.

However, BYO-AI audit is **not** the source of truth. It is an auxiliary review layer.

## Implementation Status

Current status:

```text
status: draft
maturity: example artifacts and schema drafts
production_ready: false
certification: false
safety_guarantee: false
```

## Suggested Next Steps

1. Implement a minimal CLI verifier:

```bash
verify-kit --kit ./verification-kit/examples --strict
```

2. Add signatures over the manifest or kit index.
3. Add regression tests for schema validation and verdict consistency.
4. Publish the paper PDF and link it from `paper/README.md`.

## License / Use

No license is specified in this draft repository skeleton.  
Add an explicit license before public reuse.
