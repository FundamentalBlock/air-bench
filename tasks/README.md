# Tasks

Each benchmark instance is one folder with exactly these files:

| File | What it is |
|---|---|
| `problem.md` | Optimization goal and constraints |
| `starter_policy.py` | The editable policy the agent starts from |
| `workload/` | Trace-driven task instance |
| `platform/` | Platform profile used by the evaluator |
| `evaluate.py` | Fixed evaluator (never edited by the agent) |
| `baseline.json` | Baseline metrics |
| `budget.yaml` | Experiment, time and optional API limits |

Target: about 8 to 10 instances per track, split roughly 60% dev, 20% validation, 20% hidden test.
