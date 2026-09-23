# goodWriter

### Help your Chinese lab report show your reasoning

Turn experiment notes, debugging records, and comparisons into a report that explains **why you made a choice, what the results mean, and what you learned**.

[中文](README.md) · [Quick start](#quick-start) · [Full example](examples/reflection.md) · [Skill](good-writer/SKILL.md)

You have done the experiment, but the conclusion still says little beyond “I completed the task and learned a lot.” goodWriter helps you find the observations worth discussing and connect your decisions to course concepts.

Designed for Chinese lab reports, programming assignments, and course projects. Draft a full report or revise just its conclusion while keeping key data and your voice.

## See what changes

In a synthetic caching example, the writer initially suspected disk reads. Profiling instead identified repeated computation. With the same input and only caching changed, runtime fell from 4.8 to 1.6 seconds, memory rose from 18 to 41 MB, and the output stayed the same. Only one input size was tested.

The original conclusion called caching a universally excellent technique. The rewrite explained how the bottleneck was identified, connected the result to the time-space tradeoff, and kept the conclusion within the tested conditions.

[Read the complete Chinese input and an actual generated output](examples/reflection.md).

## Quick start

With Node.js installed, add the skill using the [Skills CLI](https://github.com/vercel-labs/skills):

```sh
npx skills add https://github.com/g-sleeper/goodWriter/tree/main/good-writer
```

Then ask in Codex:

```text
Use $good-writer to revise the conclusion of my Chinese lab report.
Use these notes to explain my decisions, course understanding, and learning.
Preserve the numbers and my voice.
```

Useful inputs include the assignment, experiment conditions and results, your draft, and the problems or design choices you actually encountered. Short notes are enough to start.

<details>
<summary>Manual installation for Codex</summary>

```sh
git clone https://github.com/g-sleeper/goodWriter.git
cd goodWriter
mkdir -p "$HOME/.codex/skills"
cp -R good-writer "$HOME/.codex/skills/"
```

Compare and back up an existing skill with the same name before replacing it. Reload skills or start a new session, then invoke `$good-writer`.

</details>

## Choose the scope

| Task | What to ask |
|---|---|
| A conclusion that reads like a task list | Connect the important findings to course concepts. |
| Scattered debugging notes | Organize the problem, investigation, change, and verification; explain each decision. |
| Stiff prose | Keep the data and terminology, and match the voice of my draft. |
| An unclear argument | Review which conclusions have evidence and which paragraphs remain vague. |

## What it focuses on

- **Reasoning behind a result:** surface meaningful comparisons, counterexamples, and choices.
- **Connections between concepts:** explain how the observations relate to course knowledge and other parts of the assignment.
- **The writer's own account:** preserve real decisions and insights instead of imposing a generic reflection template.
- **Reusable methods:** turn learning into a concrete way to investigate a similar problem next time.

Final prose is the default. Ask separately for a review or score. When the only input is a passing grade, the skill starts with a supported result statement and helps identify what is needed for a personal reflection.

## Project status

**Alpha.** Synthetic cases have been exercised in a Codex subagent environment. Methods, raw outputs, and limitations are documented in [evaluation notes](benchmarks/README.md). The core skill is Markdown and requires no API key. Document rendering uses the host's own tools. Feedback from other hosts is welcome.

## Contribute

Open an [issue](https://github.com/g-sleeper/goodWriter/issues) with a minimal input, actual output, the sentence you want improved, and the model/version. Share only anonymized or synthetic material you are allowed to publish.

If goodWriter helps you explain your work, a **Star** or a useful example helps others find and improve it.

[Writing sources](good-writer/references/sources.md) · [Provenance](NOTICE.md) · [MIT License](LICENSE)
