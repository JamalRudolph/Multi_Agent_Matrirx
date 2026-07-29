# SI-MAOS v5.1 | Single-Instance Multi-Agent Orchestration System

An interactive dashboard demonstrating a single-instance, shared-context multi-agent
architecture — 10 functional roles deliberating inside one model execution pass instead
of routing across separately-called agent instances.

## v5.1 revision note
v5.0 stated a specific "92% cost reduction" claim with no supporting test, and an
internal contradiction between "roles execute concurrently" and "deliberation is
sequential." Both are corrected in v5.1: the cost claim is replaced with an actual
logged benchmark (real content generated, real token counts, methodology and raw
data disclosed), and the execution model is described accurately (sequential, single
shared context — not concurrent).

## What's actually demonstrated
- **No inter-role network hops:** all 10 roles deliberate inside one shared context
  window instead of separate API calls — a structural fact, not a performance guarantee.
- **Logged, not assumed, efficiency gain:** a real test on a representative task
  measured a 60.3% total token reduction and 73.1% input-token reduction versus a
  naive multi-agent equivalent (9 calls collapsed to 1). Full methodology and raw
  per-call data are in the companion PM Portfolio & Case Study document, not just
  asserted here.
- **Single-Point Mutation Protocol:** only one role (Cee) has write authority for
  final artifacts, mitigating the race-condition/file-corruption risk real in
  multi-writer agent systems.
- **Virtual Enterprise Matrix:** 10 roles across 5 paired layers — infrastructure,
  governance, strategy, revenue risk, and product/brand.

## Known limitations (stated directly, not buried)
This is a prompting pattern, not a runtime architecture — it doesn't add parallelism
and doesn't exceed the host model's context window. Published research (cited in-app,
Logged Benchmark section) shows multi-agent coordination actually *outperforms*
single-context approaches on genuinely parallelizable tasks; SI-MAOS is designed for
sequential, single-reviewer workflows, not positioned as a universal replacement.

## Live Demo
https://jamalrudolph.github.io/Multi_Agent_Matrirx/
