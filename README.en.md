# goodWriter

Turn experiment notes into clear Chinese lab reports that show evidence, reasoning, and learning.

[中文](README.md) · [Skill](good-writer/SKILL.md) · [Example](examples/reflection.md) · [Pilot](benchmarks/README.md)

**Alpha.** The primary audience is students writing Chinese coursework and lab reports. This is not an English-writing benchmark or a guarantee of grades.

goodWriter helps writers explain a concrete problem, the choice they made, how they checked it, the course concept it clarifies, and what they can reuse later. It supports full reports, conclusion-only revisions, prose editing, and review.

It keeps observations, the writer's own account, hypotheses, and future plans distinct. A passing score alone is not evidence of a personal learning journey.

## Installation

Download and extract this repository, or clone it:

```sh
git clone https://github.com/g-sleeper/goodWriter.git
cd goodWriter
```

Then install it for Codex:

```sh
mkdir -p "$HOME/.codex/skills"
cp -R good-writer "$HOME/.codex/skills/"
```

Compare and back up an existing skill with the same name before replacing it. Reload skills or start a new session, then ask:

```text
Use $good-writer to revise the conclusion of my Chinese lab report.
Use these experiment notes and preserve the numbers and my voice.
```

The core skill is Markdown with relative references. It needs no API key, executable helper, or network service. It has been exercised in a Codex subagent environment; other Agent Skills hosts have not been individually tested. Document rendering requires the host's own document tools.

## Evidence

The repository includes synthetic examples and development fixtures. A two-case exploratory comparison is documented in [benchmarks](benchmarks/README.md). It does not establish superiority over plain prompting or Humanizer. There is no teacher-grading study or repeated cross-model evaluation yet.

Contribute a minimal input, actual output, precise failure, model/version, and desired behavior. Share only material you are allowed to publish. Original classroom reports and feedback screenshots are not included.

See [NOTICE](NOTICE.md) for provenance. Original project files are available under the [MIT license](LICENSE).
