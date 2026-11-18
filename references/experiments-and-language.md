# Experiments, figures and tables, language, and revision execution

## E1 Experimental design and settings: first establish the question

- **Signals**: Numerous experiments lack a clear evaluation question; comparators do not support the conclusions drawn; every setting is packed into a huge table.
- **Assess**: Map each experiment group to its research question, comparators, controlled or varied factors, metrics, results, and supportable conclusions. Check whether instance sources, stopping conditions, parameter choices, and execution conditions are sufficiently clear to interpret the comparison. Do not prescribe a fixed number of instances or experimental scale.
- **Revise**: Organize experimental subsections around questions and explain basic settings in connected prose. Tabulate parameters only when they need to be compared together. Describe the environment, data, methods, and metric definitions from available material; do not invent settings. Component experiments evaluate component effects, while overall comparisons evaluate the tested methods. Make actual differences in comparison conditions explicit.
- **Recheck**: Readers understand each experiment's purpose and conditions, and conclusions stay within the scope of the comparisons. Identify necessary but unreported material as missing; do not imply that an experiment has been run.

## E2 Result analysis: findings, data, explanation, and limits

- **Signals**: The text repeats tables row by row; only successful instances are selected; correlation is described as causation; fewer nodes or faster solution is interpreted as a stronger bound.
- **Assess**: Distinguish observations, possible mechanisms, and verified mechanisms. Assess bound quality, feasible-solution quality, runtime, and search effort separately. Improvement in one metric does not automatically imply improvement in another.
- **Revise**: Write connected analysis around the main finding, key supporting data, an evidence-based explanation of the mechanism, and the scope of applicability. This is not a mandatory four-sentence template. When evidence for a mechanism is insufficient, use precise qualifications rather than inventing a cause. Retain failures, timeouts, and unfavorable results.
- **Recheck**: Every number is traceable. Statistical coverage, comparison baselines, and conclusions agree. The text does not treat unsolved instances as solved to proven optimality or turn limited comparisons into claims of superiority over an entire algorithm class.

When using a gap, improvement rate, or speedup, check the actual definition, denominator, optimization direction, units, and available observations. For zero values, negative objective values, missing bounds, or time limits, explain how these cases were actually handled. Do not assume one solver's formula applies to every table. Do not treat a time limit as an actual completion time and then make an unqualified claim about average speedup.

## E3 Tables: make comparisons directly visible

For table content selection, headings, or abbreviations, also read G5–G6 in the [dedicated guidance on figures and tables](figures-and-tables.md).

- **Signals**: Too many columns, repeated identifiers, wrapping in narrow columns, or table notes that become long paragraphs; selective changes in the rules for boldface.
- **Assess**: Establish whether readers primarily need to compare methods on the same instance, parameter levels, or instance groups. Check whether each column adds information and whether removing one would conceal an important result status.
- **Revise**: Place results for methods on the same instance next to one another. For parameter comparisons, foreground the parameters and their levels. Give units in headings, standardize abbreviations, and move long explanations to the main text. Keep only necessary symbols, exceptions, and calculation details in table notes. Highlight values using consistent, explainable criteria.
- **Recheck**: The main comparison can be understood without searching across tables. Missing results, infeasibility, time limits, and normal completion are clearly distinguished. Optimal and best-known results are not confused, and numerical precision and statistical definitions are consistent.

## E4 Figures: let the relationship determine the chart

For the actual design or colors of schematics, flowcharts, or result plots, also read G0–G4 and G7 in the [dedicated guidance on figures and tables](figures-and-tables.md).

- **Signals**: Figures repeat tables merely to increase the figure count; unordered instances are joined by lines; a few points imply a complex trend; incomplete data are presented as settled results.
- **Assess**: First state in one sentence the comparison, distribution, trend, or structure the figure should reveal. Check whether the horizontal axis has a natural order and whether connections between adjacent points have an interpretable meaning.
- **Revise**: Use lines when the values are ordered and connecting them is meaningful. For unordered categories, consider dot or bar plots. Precise comparisons among a few levels may remain in a table. Generate result plots from actual data, prefer vector output, and use consistent fonts, colors, and method identifiers. Do not invent data, curves, or certainty to suit a figure.
- **Recheck**: Figures and tables report consistent values. Axes, units, legends, and necessary conditions are complete; captions are concise; unknown and failed outcomes are represented faithfully. Identify schematics as such rather than presenting them as experimental results.

## E5 Academic language: remove empty wording, retain scientific conditions

- **Signals**: Stacks of abstract nouns; formulaic transitions without a logical basis; repeated reminders to readers not to misunderstand; program identifiers carried directly into the manuscript.
- **Assess**: Identify the objects, actions, and relationships in each sentence. Check whether deleting a sentence would lose new information, assumptions, or the limits of the evidence. Determine whether repetition serves a necessary purpose across sections.
- **Revise**: Use established terminology from transportation and operations research, with concrete verbs. Remove promotional language, self-explanation, and repetition that adds nothing. Explain each mechanism fully in the most appropriate location, then summarize or cross-reference it elsewhere. Retain necessary conditions, assumptions, and scope limitations; do not create a context-free list of banned words.
- **Recheck**: Meaning and the strength of technical claims remain unchanged. Concision has not turned “on the tested instances” into “universally.” More complex vocabulary is not automatically more academic. Do not arbitrarily change established algorithm names because they resemble program identifiers.

## E6 Revision execution: check related occurrences and control the scope

- **Signals**: Only one sentence in a screenshot is corrected; the same symbol remains unchanged elsewhere; Chinese and English drafts or tables and prose fall out of sync; a local language edit leads to rewriting the whole manuscript.
- **Assess**: Identify the error category and the affected chain of references. Search related definitions, equations, figures, tables, the abstract, and conclusions. Distinguish verified conflicts from potential risks.
- **Revise**: Correct related occurrences within the user's authorized scope. Identify the locations of substantive issues outside that scope without expanding the rewrite unilaterally. Preserve equation labels, citation keys, and existing formatting; update all references when a necessary change affects them. Keep corresponding meanings aligned in bilingual drafts rather than enforcing word-for-word correspondence.
- **Recheck**: Inspect the final files, not only the proposed edits. Compile and inspect the layout when applicable and available. State which materials are still missing and which conclusions cannot be verified; do not replace specific issues with generic disclaimers.
