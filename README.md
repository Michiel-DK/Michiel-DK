# Michiel De Koninck

I build AI systems end to end: data pipelines, retrieval, post-training, agents, and
the product surfaces on top. The part I care most about is the one that usually gets
skipped: whether the system can prove it works.

Right now that's two production systems under one roof.
**[roger3000](https://michiel-dk.github.io/roger3000-demo/)** is a live investor-intelligence
platform: a matching engine over a knowledge graph of 25k+ companies and 134k edges, served
to AI agents through a 52-tool MCP server, with a claim auditor that fact-checks
every generated sentence against its own evidence.
**[restaurant-brain](https://www.roger3000.com)** is an operations brain for hospitality:
fail-loud SAF-T invoice ingestion, stock and consumption ledgers, and report cards that
disclose per metric whether they are actually graded or honestly ungradeable. 2,100+ tests.
The site calls it Roger Brain; roger3000 is the umbrella name for both systems.

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

The pinned repos below are the same method applied to evals, retrieval, RL rewards,
post-training and sports data. Each one carries its own receipts, failures included.
For the argument in visual form, start with the
[eval-suite walkthrough](https://michiel-dk.github.io/agent-exam-suite/eval-suite-is-the-asset.html)
(5-minute read).

Based in Ericeira, Portugal. Before this: five years teaching data science and ML at
Le Wagon (1,000+ learners, 75+ student projects), and before that logistics operations
at Katoen Natie.

📫 michieldekoninck2@gmail.com · [LinkedIn](https://www.linkedin.com/in/michiel-de-koninck)
