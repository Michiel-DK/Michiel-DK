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
- **restaurant-brain** — production operations brain for hospitality: fail-loud SAF-T
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

Pre-registered predictions with review dates. Tests demonstrated red before they are
trusted green. Kill criteria written before the experiment runs, so a dead end dies
cheap. And a weekly digest that grades every open prediction — including the ones that
failed.

📫 michieldekoninck2@gmail.com
