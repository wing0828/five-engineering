---
name: five-engineering
description: Build reliable AI work through five nested layers—prompt, context, harness, loop, and graph engineering. Use for complex implementation, research, automation, debugging, or multi-agent work that needs explicit success criteria, bounded context, verification, retries, memory, or coordination.
---

# Five Engineering

Apply the smallest set of layers that makes the work reliable. Always include verification.

## 1. Engineer the prompt

Turn the request into a testable task contract:

- Define the role, objective, inputs, constraints, expected output, and useful examples.
- Convert vague goals into observable success criteria.
- Resolve conflicting instructions before execution.

Deliverable: a concise contract describing what must be true when the task is complete.

## 2. Engineer the context

Build a bounded working set:

- Gather only relevant files, decisions, tools, user constraints, and authoritative sources.
- Prefer current primary evidence.
- Compress findings into decisions, evidence, open questions, and risks.
- Remove stale, duplicated, or irrelevant context before acting.

Deliverable: the minimum context needed for the next decision.

## 3. Engineer the harness

Build an execution system around the task:

- Split the work into atomic, observable outcomes.
- Assign tools or agents only where they improve reliability.
- Define a verification method for every changed behavior.
- Include diagnostics, automated checks, and a manual observation when appropriate.
- Preserve existing user work and keep changes scoped and reversible.
- Separate implementation and approval passes for meaningful changes when an independent reviewer is available.

Deliverable: an executable plan whose outcomes each have a verification method.

## 4. Engineer the loop

Run a controlled improvement cycle:

1. Gather the next required context.
2. Act on one atomic outcome.
3. Verify the result.
4. Record evidence and changed assumptions.
5. Continue only while a success criterion remains unmet.

Do not repeat an unchanged failing attempt. Change the hypothesis, input, tool, or method first.

Stop and report when:

- all success criteria pass;
- the same blocking condition recurs three times;
- the available budget is exhausted; or
- further action requires user authority.

Deliverable: a verified result or a precise blocker with accumulated evidence.

## 5. Engineer the graph

Coordinate independent branches only when parallel ownership materially improves the work:

- Give each branch one concrete outcome, explicit ownership, required inputs, stop conditions, and evidence requirements.
- Store shared decisions and interfaces rather than raw transcripts.
- Define dependency and merge points before parallel work begins.
- Add review or approval gates where branches merge or external state changes.
- Re-plan when dependencies, interfaces, or assumptions change.

Deliverable: coordinated branch outputs merged into one coherent, reviewed result.

## Select the layers

| Situation | Layers |
| --- | --- |
| One clear outcome with small context | Prompt, context, harness |
| Unknown-size or iterative work | Add loop |
| Multiple independent outcomes | Add graph |
| External or high-impact change | Strengthen harness checks and approval gates |

Verification is part of the harness and is never optional, including for one-shot work.

## Run the default workflow

1. State the task contract and success criteria.
2. Gather and compress the minimum relevant context.
3. Define atomic outcomes and verification methods.
4. Execute the gather–act–verify loop until the criteria pass.
5. Use graph coordination only for genuinely independent work.
6. Report the result, evidence, limitations, and remaining risks.

## Report completion

Include:

- the outcome;
- the success criteria that passed;
- the strongest verification evidence;
- material assumptions or limitations; and
- any remaining risk or required follow-up.
