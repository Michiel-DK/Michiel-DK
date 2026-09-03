# Michiel De Koninck

I build AI systems end to end: data pipelines, retrieval, post-training, agents, and
the product surfaces on top. The part I care most about is the one that usually gets
skipped: whether the system can prove it works.

Right now that's two production systems under one roof.
**[roger3000](https://michiel-dk.github.io/roger3000-demo/)** is a live investor-intelligence
platform: a matching engine over a knowledge graph of 25k+ companies and 134k edges, served
to AI agents through an MCP server of about 60 tools, with a claim auditor that fact-checks
every generated sentence against its own evidence.
**[restaurant-brain](https://www.roger3000.com)** is an operations brain for hospitality:
fail-loud SAF-T invoice ingestion, stock and consumption ledgers, and report cards that
disclose per metric whether they are actually graded or honestly ungradeable. 2,100+ tests.

## The harness

Both systems are built inside an agentic harness I maintain as its own versioned repo
and consume as a git submodule across projects. The agents do the work; the harness
makes them prove it:

- **Adversarial before and after the build.** A criterion gate attacks the acceptance
  criteria before any code is written, halting on letter-traps, ungated paths and
  ambiguous quantifiers. A panel of refuter agents then tries to break each claim on the
  diff. Findings are classified blocking vs advisory, so review pressure scales with
  blast radius: booked-money code gets the full panel, copy changes get one pass.
- **Pre-registered predictions, graded on a date.** Every behavioural change to the
  harness ships with a falsifiable prediction and a review-by date. A weekly digest
  surfaces what's due, and grades are kept whichever way they land: 20 graded so far,
  11 passed, 4 partial, 3 failed, 1 ungradeable. The failed fixes are the most useful entries.
- **Red before green.** A test is trusted only after it has been shown failing against
  the exact defect it pins: reverted fix, injected wrong-fix, or declared gap.
- **Instrumented, and the instruments get audited too.** A run ledger of 3,500+ typed
  rows mined from real session transcripts (merges, criterion halts, refuter verdicts)
  feeds the weekly readout. When a metric stops being true, fixing the instrument is
  first-priority work, measured the same way as everything else.

## Public repos

The same method applied to evals, retrieval, RL rewards, post-training and sports data.
Each repo carries its own receipts, failures included.

| Repo | One line |
|---|---|
| [agent-exam-suite](https://github.com/Michiel-DK/agent-exam-suite) | Agents are disposable, eval suites are the asset. Six local-model office agents (2B to 14B, one laptop) and the deterministic, judge-free exam harness that decides which model ships. [Visual walkthrough](https://michiel-dk.github.io/agent-exam-suite/eval-suite-is-the-asset.html), 5 minutes. |
| [rag-retrieval-lab](https://github.com/Michiel-DK/rag-retrieval-lab) | Retrieval methods explained by running them. Predictions registered before each experiment, nulls reported with the same confidence intervals as the wins. Reranking lifts nDCG@10 0.32 to 0.41 on 323 human-labelled queries; BM25 lost, RRF was a null. |
| [rlvr-codegen](https://github.com/Michiel-DK/rlvr-codegen) | Test the tests before you train on them. Audits a test-pass RL reward before any RLVR training: roughly one in eight visibly-passing solutions from an untrained base model fails the held-out suite. Ran for $0 on a laptop. |
| [roger3000-demo](https://github.com/Michiel-DK/roger3000-demo) | Scrollytelling demo of the investor-intelligence engine on synthetic data. The only real numbers on the page are the claim-auditor calibration figures. |
| [cycling_manager](https://github.com/Michiel-DK/cycling_manager) | Predicting Grand Tour results since 2022. Two neural generations (LSTM encoder-decoder, image autoencoders) benchmarked on one held-out race, bugs included. [Architecture digest](https://michiel-dk.github.io/cycling_manager/). |
| [lora_llama](https://github.com/Michiel-DK/lora_llama) | LoRA fine-tune of Llama-3.2-1B for EN to PT, plus an LLM-judge distillation with a documented leakage flaw. Past work, frozen, with a retracted metric left visible. |
| [environmental_sound](https://github.com/Michiel-DK/environmental_sound) | ESC-50 sound classification: supervised CNN vs COLA-style contrastive self-supervision, with a write-up of why SSL needs scale and a stage-2 bug I found afterwards. |
| [repo-radar-public](https://github.com/Michiel-DK/repo-radar-public) | Daily GitHub-trending radar with HN and Reddit demand signals, and per-repo notes on what's reusable. How I keep up. |

Based in Ericeira, Portugal. Before this: five years teaching data science and ML at
Le Wagon (1,000+ learners, 75+ student projects), and before that logistics operations
at Katoen Natie.

📫 michieldekoninck2@gmail.com · [LinkedIn](https://www.linkedin.com/in/michiel-de-koninck)
