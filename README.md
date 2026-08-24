# Michiel De Koninck

**I build AI systems that measure themselves.**

Evals before agents, predictions before experiments, audits before training. Everything
below carries receipts — committed numbers, including the unflattering ones.

## Now

- **[roger3000](https://michiel-dk.github.io/roger3000-demo/)** — investor-intelligence
  platform, live and in use: a VC/startup matching engine over a knowledge graph of ~25k
  companies and 134k edges, served to AI agents through an MCP server, and built under an
  agentic review harness (pre-registered predictions, adversarial verification, weekly
  graded readouts). Public demo: [roger3000-demo](https://github.com/Michiel-DK/roger3000-demo).
- **[restaurant-brain](https://www.roger3000.com)** — production operations brain for hospitality: fail-loud SAF-T
  invoice ingestion, stock and consumption ledgers, and report cards that disclose, per
  metric, whether they are actually graded or honestly ungradeable. Private repo — the
  build methodology behind it is what the public repos below demonstrate.

## Receipts

| repo | the claim, measured |
|---|---|
| [agent-sandbox](https://github.com/Michiel-DK/agent-sandbox) | Agents are disposable, eval suites are the asset — 86 deterministic exam cases, no LLM judge, and saturated scores reported as instrument defects, not wins |
| [rag-retrieval-lab](https://github.com/Michiel-DK/rag-retrieval-lab) | Predictions registered before each experiment — reranking's gain is real (+0.089 nDCG@10, p ≈ 0); the BM25 and RRF nulls get the same confidence intervals as the win |
| [rlvr-codegen](https://github.com/Michiel-DK/rlvr-codegen) | The test-pass RL reward audited before anything trains on it — 12–18% of visible-passing completions fail a held-out suite, measured for ~$0 on a laptop |
| [lora_llama](https://github.com/Michiel-DK/lora_llama) | LoRA fine-tuning of Llama-3.2-1B for EN→PT: BLEU 4 → 23, with an LLM judge distilled into Qwen2.5-3B |
| [environmental_sound](https://github.com/Michiel-DK/environmental_sound) | ESC-50 sound classification: supervised CNN vs COLA-style contrastive SSL, with a measured writeup of why SSL needs scale |

## How I work

Everything above is built inside an agentic harness I maintain as its own versioned
repo and consume as a git submodule across projects — a build/review pipeline where the
agents do the work and the harness makes them prove it:

- **Adversarial before and after the build.** A criterion gate attacks the acceptance
  criteria before any code is written (halting on letter-traps, ungated paths, ambiguous
  quantifiers); a panel of refuter agents then tries to break each claim on the diff.
  Findings are classified blocking vs advisory, so review pressure scales with blast
  radius — booked-money code gets the full panel, copy changes get one pass.
- **Pre-registered predictions, graded on a date.** Every behavioural change to the
  harness ships with a falsifiable prediction and a review-by date; a weekly digest
  surfaces what's due, and grades are kept whichever way they land — 20+ graded so far,
  failures included (the failed fixes are the most useful entries).
- **Red before green.** A test is trusted only after it has been shown failing against
  the exact defect it pins — reverted fix, injected wrong-fix, or declared gap.
- **Instrumented, and the instruments get audited too.** A run ledger (3,000+ typed rows
  mined from real session transcripts: merges, criterion halts, refuter verdicts) feeds
  the weekly readout — and when a metric stops being true, fixing the instrument is
  treated as first-priority work, measured the same way as everything else.

📫 michieldekoninck2@gmail.com
