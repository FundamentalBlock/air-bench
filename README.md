# air-bench

Benchmark for AI agents that research infrastructure optimizations under fixed budgets.

AIR-Bench gives a research agent starter policy code, an objective and an experiment budget. The agent edits the policy, runs experiments in a trace-driven cluster emulator, reads machine-checkable metrics and iterates. We measure whether it finds valid improvements, whether they generalize to held-out workloads, and whether they transfer to a real cluster (CloudLab).

UConn Senior Design.

## Tracks

| Track | Decision | Objective |
|---|---|---|
| A. Branch Scheduling | Which agent branches get resources | Lower p95 latency, keep task success |
| B. Sandbox Resource Management | Warm-pool size, keep vs. release | Fewer memory-seconds, limited startup latency |
| C. Retry / Verification Control | Retry, wait, verify or stop | Lower CPU cost, keep task success |

## Layout

```
airbench/
  core/        evaluator + emulator          Saanvi
  workloads/   trace format + pipeline       Ivan
  platforms/   platform profiles             Ivan
  runner/      runner, budgets, logging      Chris
  baselines/   random search, tuning         Chris
  agents/      LLM agent adapters (Sem 2)    Chris
tasks/
  track_a/  track_b/  track_c/               one folder per instance
docs/  spec/                                 Ethan
tests/
```

## Setup

Requires Python 3.11+.

```bash
python -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate
pip install -e ".[dev]"
pytest
```

## How we work

- Never push to `main`. Open a pull request.
- One pull request per hub task, with the task title in the PR.
- The folder owner (see `.github/CODEOWNERS`) reviews changes to their folder.
- Run `pytest` and `ruff check .` before opening a PR.
