# Michiel De Koninck

I build AI systems end to end — data pipelines, retrieval, post-training, agents, and
the product surfaces on top — and I care most about the part that usually gets skipped:
whether the system can prove it works.

Right now that's two production systems under one roof:
**[roger3000](https://michiel-dk.github.io/roger3000-demo/)**, a live investor-intelligence
platform (a matching engine over a knowledge graph of ~25k companies and 134k edges,
served to AI agents through an MCP server), and
**[restaurant-brain](https://www.roger3000.com)**, an operations brain for hospitality —
fail-loud SAF-T invoice ingestion, stock and consumption ledgers, and report cards that
disclose per metric whether they are actually graded or honestly ungradeable.

## The harness

Both systems are built inside an agentic harness I maintain as its own versioned repo
and consume as a git submodule across projects. The agents do the work; the harness
makes them prove it:

- **Adversarial before and after the build.** A criterion gate attacks the acceptance
  criteria before any code is written — halting on letter-traps, ungated paths,
  ambiguous quantifiers — and a panel of refuter agents then tries to break each claim
  on the diff. Findings are classified blocking vs advisory, so review pressure scales
  with blast radius: booked-money code gets the full panel, copy changes get one pass.
- **Pre-registered predictions, graded on a date.** Every behavioural change to the
  harness ships with a falsifiable prediction and a review-by date; a weekly digest
  surfaces what's due, and grades are kept whichever way they land — 20+ graded so far,
  failures included. The failed fixes are the most useful entries.
- **Red before green.** A test is trusted only after it has been shown failing against
  the exact defect it pins — reverted fix, injected wrong-fix, or declared gap.
- **Instrumented, and the instruments get audited too.** A run ledger of 3,000+ typed
  rows mined from real session transcripts (merges, criterion halts, refuter verdicts)
  feeds the weekly readout — and when a metric stops being true, fixing the instrument
  is first-priority work, measured the same way as everything else.

The pinned repos below are the same method applied to evals, retrieval, RL rewards and
post-training — each one carries its own receipts.

📫 michieldekoninck2@gmail.com
