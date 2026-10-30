# Michiel De Koninck

I build AI systems end to end: data pipelines, retrieval, post-training, agents, and the
product surfaces on top. The part I care most about is the one that usually gets skipped:
whether the system can prove it works.

I co-run **[roger3000](https://roger3000.com)**, a product studio in Ericeira, Portugal,
with André. Four products, each one shows its work and grades itself:

- **[wilco](https://roger3000.com/wilco)**, for AI teams. Validates open-source models on your
  own tasks so the model you run is picked on your cases, run where you choose, and re-sat the
  day it gets worse. The public cut is [Michiel-DK/wilco](https://github.com/Michiel-DK/wilco):
  eight tasks, 282 cases (171 held out), deterministic grading, no LLM judge.
- **[honey](https://roger3000.com/honey)**, for restaurants. The operating layer over POS and
  inventory: invoice ingestion that fails loud, stock and consumption ledgers, report cards that
  say per metric whether they are graded or ungradeable. 2,100+ tests. Private; now onboarding
  its first restaurant.
- **[gurren](https://roger3000.com/gurren)**, for robot fleets. Send a week of fleet log, get back
  what each robot did, which stalls were real, and where robots block each other. The measurement
  record is public: [warehouse-rl](https://github.com/Michiel-DK/warehouse-rl), negatives left in.
- **[emmet](https://roger3000.com/emmet)**, for contractors. A priced quote from the client's
  email against your own price book, every line with its reason and its IVA source. Private.

## The harness

Everything above is built inside an agentic harness I maintain as its own versioned repo and
consume as a git submodule across projects. The agents do the work; the harness makes them
prove it:

- **Adversarial before and after the build.** A criterion gate attacks the acceptance criteria
  before any code is written, halting on letter-traps, ungated paths and ambiguous quantifiers.
  A panel of refuter agents then tries to break each claim on the diff. Findings are classified
  blocking vs advisory, so review pressure scales with blast radius.
- **Pre-registered predictions, graded on a date.** Every behavioural change to the harness
  ships with a falsifiable prediction and a review-by date. 51 grades over 40 predictions so far:
  17 passed, 14 partial, 6 failed, 14 ungradeable. The failed fixes are the most useful entries.
- **Red before green.** A test is trusted only after it has been shown failing against the exact
  defect it pins: reverted fix, injected wrong-fix, or declared gap.
- **Instrumented, and the instruments get audited too.** A run ledger mined from real session
  transcripts feeds a weekly public readout, counts only:
  [dev-harness-public](https://github.com/Michiel-DK/dev-harness-public). 887 merges, 15 weeks,
  $15 per credited merge over the last five.

The pinned repos are the same method applied to evals, retrieval, RL rewards and fleet logs. Each one carries its own receipts, failures included. For the argument in visual
form, start with the
[eval-suite walkthrough](https://michiel-dk.github.io/wilco/eval-suite-is-the-asset.html)
(5-minute read).

Earlier: roger3000 began as an investor-intelligence matching engine with a claim auditor that
fact-checks every generated sentence against its own evidence. Its evaluation layer is public as
[pierre](https://github.com/Michiel-DK/pierre); the
[scrollytelling demo](https://michiel-dk.github.io/roger3000-demo/) is still live.
Before that: five years teaching data science and ML at Le Wagon (1,000+ learners, 75+ student
projects), and before that logistics operations at Katoen Natie.

📫 michieldekoninck2@gmail.com · [LinkedIn](https://www.linkedin.com/in/michiel-de-koninck) · [roger3000.com](https://roger3000.com)
