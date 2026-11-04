# Capability Definition

> Status: draft for Ethan to edit. Based on the primary research question in the project plan.

AIR-Bench measures **automated infrastructure research ability**: whether an AI research agent, given an infrastructure optimization task, starter policy code and a fixed experiment budget, can discover policy changes that improve a measurable system objective, and whether those improvements generalize to held-out workloads and transfer to a real cluster. The benchmark scores the research process, not only the final policy. A capable agent understands the task, inspects the starter policy and experiment results, proposes and implements changes, runs experiments within the budget, interprets machine-checkable metrics, and selects a final candidate that holds up beyond the workloads it was tuned on.

## Source

Project plan, section 1 (Project Goal): "Can an automated research agent discover infrastructure optimizations that improve measurable system objectives, generalize to held-out workloads, and transfer to a real cluster?"

## Related

- How a result becomes a score: [research/2a-score-formula.md](research/2a-score-formula.md)
- What every task must include: [research/1d-task-specification.md](research/1d-task-specification.md)
