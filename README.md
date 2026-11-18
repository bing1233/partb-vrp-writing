# Part B VRP Writing

**English** | [简体中文](README.zh-CN.md)

**Version: v1.0.0** · [Release notes](CHANGELOG.md)

A writing skill for vehicle routing and related transportation operations research papers intended for **Transportation Research Part B: Methodological**.

The skill turns recurring writing problems into a practical workflow: **locate the problem, assess it, revise the manuscript, and recheck the result**. It learns organizational and explanatory techniques from checked papers while keeping each manuscript's research setting, assumptions, and evidence separate.

The skill instructions are in **English**. Use the links above to switch the README language; manuscript revisions and explanations can be in either language.

## Why this skill exists

A grammatically correct draft can still leave a reader unsure why a routing problem matters, how a constraint works, or what an experiment establishes. Repeated reminders such as "follow Part B style" do not identify the problem or explain the required change.

This skill records those writing problems as reusable assessment and revision procedures. It focuses on transportation operations research: decision trade-offs, mathematical definitions, algorithm logic, and the evidence behind contributions. Individual manuscripts supply their own research setting and results.

## What it covers

| Area | Main focus |
| --- | --- |
| Title, abstract, and conclusions | Match the claimed scope to the actual research and evidence |
| Introduction and contributions | Build motivation from decision difficulties; explain what is new |
| Literature review | Organize research relationships, assumptions, and boundaries |
| Problem description and notation | Introduce the system before notation; make definitions easy to find |
| Mathematical models | Present coherent formulations and explain objectives and constraint groups in order |
| Algorithms and proofs | Explain the framework, state updates, pseudocode, conditions, and guarantees |
| Experiments and results | Connect each comparison to a research question and supported conclusion |
| Figures and tables | Choose appropriate visual logic, table content, abbreviations, and colors |
| Revision and consistency | Check affected definitions, references, claims, and bilingual passages |

## A revision example

**Illustrative example only.** This is a small mathematical example written for the documentation, not an excerpt from a reference paper or an empirical evaluation of the skill.

Suppose a model has customer set $C\subseteq V$, node set $V$, and vehicle set $K$. The binary variable $x_{ij}^{k}$ equals one when vehicle $k$ uses arc $(i,j)$. One constraint group is:

$$
\sum_{k\in K}\sum_{j\in V\setminus\{i\}}x_{ij}^{k}=1,\qquad i\in C.
$$

**Before:** "These constraints guarantee that the routes are feasible."

**Assessment:** The explanation is broader than the displayed equations. This group specifies the number of outgoing customer arcs; it does not establish every condition needed for route feasibility.

**After:** "These constraints require exactly one outgoing arc from each customer across the vehicle fleet."

**Recheck:** Confirm the index sets and variable meanings against the actual formulation, then explain the remaining constraint groups according to what they enforce. The same procedure applies when revising a contribution claim or interpreting a result table: identify the supported meaning before polishing the sentence.

## How it works

1. **Locate** the sentence, equation, figure, table, or section that needs attention.
2. **Assess** the issue using the actual manuscript, evidence, and relevant writing guidance.
3. **Revise** within the requested scope, producing replacement text or edited files.
4. **Recheck** the change and directly affected definitions, claims, and references.

| Request | What to provide | Expected output |
| --- | --- | --- |
| Plan a paper or section | Research question, established method, available findings, and constraints | An argument outline, section functions, and missing information |
| Revise prose | Current passage, relevant evidence, and wording or scope restrictions | Replacement text with brief reasons for substantive changes |
| Review a model or algorithm description | Definitions, equations, pseudocode, and relevant implementation details | Located issues, grounds, and proposed corrections |
| Improve figures or tables | Data or source files, comparison question, and visual preferences | A justified design or revision; figures use the available appropriate tools |
| Learn from reference papers | Papers or links and the writing problem to study | Checked locations, their writing functions, and transferable actions |

For sustained manuscript work, the optional [context template](assets/manuscript-context.template.md) records known facts, claims and evidence, checked sources, and author preferences. Keep the completed record with the manuscript.

## Design principles

- Distinguish academic requirements, adaptable writing practices, and author preferences.
- Keep facts, assumptions, experimental settings, and interpretations separate.
- Preserve genuine contributions while limiting claims to their evidence.
- Respect requests to revise wording without adding experiments.
- Check actual paper passages before attributing a writing practice to them. Inspect images before making claims about colors or layout.
- Keep a manuscript's business setting, parameters, and algorithm choices out of reusable rules.

## Use with Codex

Give Codex's skill installer this repository's URL and specify that `SKILL.md` is at the repository root. For example:

```text
Install the skill from https://github.com/bing1233/partb-vrp-writing.
Its SKILL.md is at the repository root.
Use partb-vrp-writing as the installed skill name.
```

After installation, invoke `$partb-vrp-writing` and provide the current manuscript or relevant passage. GitHub publication and installation in a particular Codex environment are separate steps.

Example requests:

```text
Use $partb-vrp-writing to revise this introduction and contribution section.
Keep the research assumptions unchanged. Do not add experiments.
Deliver replacement text and briefly explain substantive changes.
```

```text
Use $partb-vrp-writing to check this notation table, formulation,
and pseudocode. Give the objective and constraint explanations in
one continuous paragraph after the complete formulation.
```

```text
Use $partb-vrp-writing to redesign these figures and tables using
appropriate, checked Part B examples. Use brighter figure colors,
and explain which visual choices serve which comparison.
```

## Files

| File | Purpose |
| --- | --- |
| [SKILL.md](SKILL.md) | Entry point, workflow, scope, and reference routing |
| [VERSION](VERSION) and [CHANGELOG.md](CHANGELOG.md) | Package version and bilingual release notes |
| [agents/openai.yaml](agents/openai.yaml) | Codex display metadata and suggested prompt |
| [argumentation.md](references/argumentation.md) | Motivation, contributions, reviews, and section structure |
| [model-and-method.md](references/model-and-method.md) | Definitions, formulations, algorithms, and proofs |
| [experiments-and-language.md](references/experiments-and-language.md) | Experimental interpretation, language, and consistency |
| [figures-and-tables.md](references/figures-and-tables.md) | Schematics, flowcharts, result plots, colors, tables, and abbreviations |
| [partb-evidence.md](references/partb-evidence.md) | Checked papers, versions, page locations, and inspection limits |
| [source-learning.md](references/source-learning.md) | How to learn from references without inventing journal conventions |
| [manuscript-context.template.md](assets/manuscript-context.template.md) | Optional working record for one manuscript |

## Reference basis and visual preferences

The [evidence record](references/partb-evidence.md) includes selected material from Su et al. (2023), Sun et al. (2018), and Zamal et al. (2025). It distinguishes actual image inspection from text-only checks and author manuscripts from published versions. These examples support specific writing choices; they are not a comprehensive survey of Part B practice.

The skill retains the author's preference for **brighter figure colors**. New figures use black labels on white backgrounds as a configurable design default, with colors, shapes, and line styles chosen for the information being shown. No fixed palette is claimed to be required by Part B, and unverified color codes are not presented as exact reproductions of published figures.

## Scope and limits

This is an independent writing resource, with no claimed affiliation with the journal or its publisher. It does not implement algorithms, run experiments, prove mathematical results, or guarantee acceptance. Current submission requirements must be checked against the journal's official guidance when needed.

The repository contains instructions, a blank template, and original notes with links to sources. It does not redistribute the reference papers or their figures. When improving the skill, keep manuscript-specific data and completed context records outside this repository, and distinguish new source observations from author preferences.

Version 1.0.0 does not include automated manuscript-checking scripts, ready-made LaTeX or plotting templates, or a behavioral evaluation suite. File-format checks alone do not establish writing quality or mathematical correctness.

The README organization draws on the public [Academic Humanizer README](https://github.com/AIScientists-Dev/academic-humanizer/blob/main/README.md): explain the writing problem, show a concrete example, and document use and scope. The instructions and illustrative example in this repository are written for this project.
