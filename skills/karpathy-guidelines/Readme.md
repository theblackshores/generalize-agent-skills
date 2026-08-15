From: https://github.com/multica-ai/andrej-karpathy-skills/blob/main/CLAUDE.md

Modified:
- Apply: https://x.com/Mnilax/status/2053116311132155938

<details>
  <summary>Prompts 1 (Github Copilot - GPT-5.6 Sol - Max):</summary>

  請以 SKILL.md 原本的風格 apply 以下新 rules:
  ```
  ## Rule 5 — Use the model only for judgment calls
  Use me for: classification, drafting, summarization, extraction.
  Do NOT use me for: routing, retries, deterministic transforms.
  If code can answer, code answers.

  ## Rule 6 — Token budgets are not advisory
  Per-task: 4,000 tokens. Per-session: 30,000 tokens.
  If approaching budget, summarize and start fresh.
  Surface the breach. Do not silently overrun.

  ## Rule 7 — Surface conflicts, don't average them
  If two patterns contradict, pick one (more recent / more tested).
  Explain why. Flag the other for cleanup.
  Don't blend conflicting patterns.

  ## Rule 8 — Read before you write
  Before adding code, read exports, immediate callers, shared utilities.
  "Looks orthogonal" is dangerous. If unsure why code is structured a way, ask.

  ## Rule 9 — Tests verify intent, not just behavior
  Tests must encode WHY behavior matters, not just WHAT it does.
  A test that can't fail when business logic changes is wrong.

  ## Rule 10 — Checkpoint after every significant step
  Summarize what was done, what's verified, what's left.
  Don't continue from a state you can't describe back.
  If you lose track, stop and restate.

  ## Rule 11 — Match the codebase's conventions, even if you disagree
  Conformance > taste inside the codebase.
  If you genuinely think a convention is harmful, surface it. Don't fork silently.

  ## Rule 12 — Fail loud
  "Completed" is wrong if anything was skipped silently.
  "Tests pass" is wrong if any were skipped.
  Default to surfacing uncertainty, not hiding it.
  ```

  以下是與 SKILL.md 風格不同但與新 rules 相同的 rules 1-4 謹供你進行風格參考, 不要更新原來的 rules 1-4:
  ```
  ## Rule 1 — Think Before Coding
  State assumptions explicitly. If uncertain, ask rather than guess.
  Present multiple interpretations when ambiguity exists.
  Push back when a simpler approach exists.
  Stop when confused. Name what's unclear.

  ## Rule 2 — Simplicity First
  Minimum code that solves the problem. Nothing speculative.
  No features beyond what was asked. No abstractions for single-use code.
  Test: would a senior engineer say this is overcomplicated? If yes, simplify.

  ## Rule 3 — Surgical Changes
  Touch only what you must. Clean up only your own mess.
  Don't "improve" adjacent code, comments, or formatting.
  Don't refactor what isn't broken. Match existing style.

  ## Rule 4 — Goal-Driven Execution
  Define success criteria. Loop until verified.
  Don't follow steps. Define success and iterate.
  Strong success criteria let you loop independently.
  ```
</details>

<details>
  <summary>Prompts 2 (Github Copilot - GPT-5.6 Sol - Max):</summary>

  把這行原本寫死的 tokens 數字改成一種較為模糊的描述, 不要讓其出現固定數字
</details>
