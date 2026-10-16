# Coding prompts

Free copy-paste prompts from [AgentKit Co](https://agentkitco.com/free-prompts/). Replace anything in [BRACKETS] with your own details.

## The session starter

**When to use:** Paste this at the start of a new chat, before any other prompt, so the assistant knows your setup.

```text
CONTEXT FOR THIS SESSION
- I'm working in: [LANGUAGE + VERSION], [FRAMEWORK / ENGINE if any]
- On: [OS], using [EDITOR / IDE]
- My level: [e.g. "beginner, 3 months, mostly tutorials"]
- Project: [ONE SENTENCE — what I'm building and for whom]

HOW I'D LIKE YOU TO HELP
- Explain your reasoning in plain English; define jargon the first time.
- Prefer the smallest change that works. Don't rewrite whole files unless I ask.
- Don't add new libraries or services without telling me why and asking.
- If you're not sure, say so and tell me how to check. Never invent functions, flags or library features.
- If a command or script could delete, overwrite, install, or send data online, warn me first and suggest a safe way to test it.
- I'll never paste real secrets. If you see one, tell me to remove it.

Reply "Ready" and wait for my first request.
```

## Explain this code line by line

**When to use:** You found, inherited or were given code you don't fully understand.

```text
I'm learning [LANGUAGE] (my level: [LEVEL]). Explain the code below line by line in plain English. Then:
1. Summarise what the whole thing does in 2 sentences.
2. Name up to 5 concepts in it that I should look up.
3. Ask me one question to check I understood.
Don't rewrite or "improve" the code yet.

Code:
[PASTE CODE]
```

## Learn-by-building roadmap

**When to use:** You want a sequence of small projects instead of another tutorial playlist.

```text
I want to learn [LANGUAGE / TOPIC] by building small projects. I have about [HOURS] per week. I already know: [WHAT YOU KNOW].
Suggest 6 projects in order of difficulty, each finishable in a weekend.
For each project give:
- What it does (1 sentence)
- The 2–3 new concepts it teaches
- A "done when" checklist (3–5 items)
Avoid projects that need paid services, API keys or accounts.
```

## Error message decoder

**When to use:** You have an error message and no idea what it means.

```text
I got this error running [LANGUAGE + VERSION] on [OS]:
[PASTE FULL ERROR / TRACEBACK]
Here is the code it points to (plus a few lines around it):
[PASTE CODE]
1. Explain what the error means in plain English.
2. Tell me which line is the real cause. It may not be the last line shown.
3. List the 2–3 most likely causes, ranked, and how to check each one.
4. Suggest the smallest fix for the most likely cause.
```

## Expected vs. actual

**When to use:** No error appears, but the result is wrong.

```text
My code runs without errors but gives the wrong result.
Expected: [EXPECTED RESULT]
Actual: [ACTUAL RESULT]
Input used: [INPUT]
Code:
[PASTE CODE]
Don't fix it yet. First list the assumptions the code is making. Then tell me exactly where to add print/log statements to find the first point where the expected and actual values split apart.
```

## Smallest-diff fix

**When to use:** You've found roughly where the bug is and want a clean, minimal fix.

```text
Find the bug in this [LANGUAGE] code and fix it with the smallest change possible. The code is supposed to: [GOAL].
- Show only the changed lines, with 2 lines of context and a comment on each change.
- Explain why the bug happened.
- Name one habit that would have prevented it.
If you spot more than one bug, list them all but fix only the first.

Code:
[PASTE CODE]
```

## "Safe to run?" check

**When to use:** Before running any command, script or fix you didn't write yourself, including one the AI wrote.

```text
Before I run this, review it for safety:
[PASTE COMMAND / SCRIPT / FIX]
1. Explain in plain English what it will do.
2. Flag anything that: deletes or overwrites files, changes system settings, installs packages, sends data over the network, needs admin/sudo, or downloads and runs code (e.g. curl ... | sh).
3. Rate the risk Low / Medium / High.
4. Tell me how to test it safely first (dry run, backup, sandbox, copy of the data).
```

## What should I test?

**When to use:** Before writing tests, to get a list of cases you might not think of.

```text
Here is a function:
[PASTE FUNCTION]
List the test cases it needs, grouped as:
- Normal cases
- Edge cases (empty, zero, negative, very large, duplicates, unusual characters, wrong type)
- Error cases (what should happen with invalid input)
Format as a table: Input | Expected result | Why this case matters.
Don't write test code yet. If the expected result is unclear, say so.
```

## Turn a bug into a test

**When to use:** You just found a bug and never want to see it again.

```text
I found this bug: [DESCRIPTION, including the input that fails].
Code: [PASTE CODE]
1. Write a test that reproduces the bug and FAILS on the current code.
2. Show the fix.
3. Explain how this test now guards against the bug coming back (a "regression test").
```

## Scope to an MVP

**When to use:** Your idea is big and you want something working this week.

```text
I want to build: [PROJECT IDEA]. I have [TIME AVAILABLE] and I know [SKILLS]. Cut it down to the smallest version that is still useful (an MVP):
- The one core feature
- Must / Should / Later lists
- What I can fake, hard-code or do by hand at first
- A build order where something works by the end of day 1
```

## Secrets and .gitignore check

**When to use:** Before your first push to a public repo, or if you're not sure what's been committed.

```text
Here is my project's file tree and config files. I've replaced real values with XXXX:
[PASTE FILE TREE + CONFIG]
1. Which files should never be committed?
2. Write a .gitignore for a [LANGUAGE / FRAMEWORK] project.
3. Show how to load secrets from environment variables (or a .env file that's ignored).
4. If a secret was already committed, explain why deleting it in a new commit isn't enough and what to do, starting with revoking or rotating the key.
```
