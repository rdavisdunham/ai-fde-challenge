# Track 2: Evaluation framework for a software engineering agent

## Problem

Build a small evaluation harness for a software engineering agent. It should run tasks, capture the agent's work, evaluate the result, and learn from its own logs by turning prior failures into useful feedback for later runs.

You may use an existing coding agent, a mocked agent, or a simple model-backed loop. The framework is the focus, not the brand of agent or model.

## Minimum requirements

- Repeatable task runner using one or more engineering tasks
- Capture prompts, model/tool calls, files changed, commands, tests, errors, retries, and final output
- Outcome-based evaluation, such as tests passing or required behaviour being present
- Separate quality or process evaluation
- Run summary showing success/failure, duration, estimated token/API cost, tool-call count, test results, and failure reason
- Way to compare runs
- Feedback loop that uses previous logs to identify recurring failures or improve a future run. A simple heuristic — for example, surfacing the most common failure categories from past runs as a prompt hint for the next one — is a valid minimal version of this; it does not need to be a learned model.
- Clear operator view into what happened behind the curtain

## Suggested tasks

Pick a small set of engineering tasks so you spend your time on the harness, not on task design. A few options:

- Fix a specific failing test in a small open-source repo
- Implement a well-specified pure function (e.g. parse a log format, reverse a linked list) with a fixed test suite
- Add a small feature to a toy repo with an existing test harness
- Fix a deliberately introduced bug in a repo you set up yourself

Two or three tasks of varying difficulty is enough to produce comparable runs.

## Optional extensions

- Local trace viewer or dashboard
- Replayable runs
- Regression suite
- Human review and correction
- Secret and sensitive-data redaction
- Per-step cost and latency breakdown
- Policy checks for risky commands
- Failure categorisation or clustering

## Discussion prompts

Be prepared to explain what good performance means, how you distinguish a bad solution from a bad process, which signals are direct measures versus proxies, how learning avoids reinforcing bad behaviour, how you prevent evaluation leakage, what operators should see, and how you handle non-determinism.
