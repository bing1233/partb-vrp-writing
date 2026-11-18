# Figure and Table Design, Colors, and Abbreviations

Contents: G0 Design sequence; G1 Schematics; G2 Flowcharts; G3 Results plots; G4 Colors; G5 Table content; G6 Abbreviations; G7 Production and review; Sources.

First read the [Part B sample and location records](partb-evidence.md) to distinguish observations from the papers examined, the design advice in this file, and the author's preferences. The guidance below is not an official journal requirement for colors or layout. Retain an existing manuscript style when it is clear and consistent; implement changes when the user requests them. Figure and table content must be grounded in the current study.

## G0 Define the task before choosing the visual form

- **Signals**: Choosing an attractive chart before finding data; including many figures and tables without an argumentative purpose; repeatedly presenting the same content in different plots.
- **Assessment**: First write one sentence stating what the reader should understand or compare, then identify the evidence required. Use a schematic to explain objects and relationships; a flowchart to explain execution order and control relationships; a results plot to compare numerical relationships; and a table when readers need exact values or item-by-item comparisons.
- **Revision**: Determine the reading task, essential content, visual encoding, layout, labels, colors, and output dimensions, in that order. Connect each figure or table explicitly to the text, and do not treat decoration as information.
- **Review**: Is the main structure understandable with the title hidden? Can the reader identify the objects, metrics, and necessary conditions from the figure or table and its caption alone? Would removing it lose important information?

Before designing a figure or table, you may record five items in the working context: its purpose; the source of its data or definitions; the mapping from objects to positions, shapes, or colors; conditions that must be retained; and the claim in the text that it supports. There is no need to deliver a design report to the user every time.

## G1 Schematics: objects, relationships, and the key mechanism

Reference locations: P1, p. 3, Figs. 1 and 2; P3, p. 5, Fig. 2. First decide whether the figure explains network structure, interactions among participants, or temporal relationships, then choose a suitable layout. Do not turn all these different functions into algorithm block diagrams.

- **Signals**: The figure resembles an industry promotional poster; it contains many nodes and arrows with no defined meaning; a background map obscures the key mechanism; or the same arrow represents both travel and information feedback.
- **Assessment**: List the minimum objects and relationships needed to understand the problem, together with the decision or mechanism the paper aims to explain. Determine whether position represents actual geography, time, or layout alone.
- **Revision**: Express the structure with nodes, groups, and lines first, then add only the necessary symbols. Use shapes to distinguish object types, arrows to indicate direction, and line styles to distinguish explicitly defined relationship types. Assign color one declared primary classification role. Separate multiple relationships into panels when helpful; do not try to resolve crowding by continually adding colors.
- **Review**: Each shape, line style, and arrow has a clear meaning; the structure agrees with the model; and the layout does not imply distances, ordering, capacities, or feasibility that do not exist.

Practical steps:

1. Sketch only the necessary nodes and connections first. Check whether the mechanism is understandable before refining the visual style.
2. In route diagrams, use arrows to show the actual service sequence. If request associations and travel arcs appear together, distinguish them with line styles and explain the distinction. Do not force every possible arc into the figure.
3. Show temporal relationships on a shared time axis, clearly identifying time windows, service intervals, and travel periods. When time is not shown to scale, label the figure as schematic rather than inventing scale markings.
4. Compare mechanisms in side-by-side panels with the same object layout and legend. Change only the relationships being compared, so that rearranged nodes do not create false differences.
5. A small constructed example may explain a definition, but it must be explicitly labeled an "illustrative example" and checked against the conditions it claims to satisfy. It does not establish general correctness and must not be presented as a computational experiment result.

## G2 Flowcharts: inputs, state updates, decisions, loops, and outputs

Reference location: P1, p. 17, Fig. 5. Learn how the figure expresses nesting, conditional exits, and loops; do not copy its ordering of pricing, cutting, or branching.

- **Signals**: Paragraphs are squeezed into boxes; all steps are forced into a one-way chain; true and false branches are unlabeled; or stopping decisions conflict with the pseudocode.
- **Assessment**: Extract operations, state dependencies, decisions, loops, and termination conditions from the actual algorithm or process. Distinguish how the algorithm runs from how the authors conduct the research.
- **Revision**: Use recognizable shapes consistently for operations and decisions. Rectangles for operations, diamonds for decisions, and rounded shapes for start/end are usable conventions. Parallelograms for inputs and outputs are optional, not a required format established by this sample or Part B. Label decision exits with Yes/No or the actual conditions, and return loop arrows to the step that actually repeats. Draw parallel execution, feedback, and early termination only when they exist.
- **Review**: Manually trace normal termination, continued iteration, and any exceptional or early termination branches that actually exist. Every path must use the same state-update order as the text and pseudocode.

A top-down layout with loops along the sides can help reduce crossing lines while respecting the actual dependencies. Use short verb phrases inside boxes; place long formulas, subprocess details, and correctness arguments in the text. A large process can be split into an overall framework and key subprocesses, or labeled group boundaries can distinguish nested levels. Use consistent names across levels. Follow G4 for colors; do not restrict flowcharts to black and gray or a single accent color.

If the algorithm is ambiguous, identify the conflict first. Do not choose an execution order merely to make the drawing flow smoothly. When a figure shows only the main modules, label it as a framework diagram and do not claim that it replaces complete pseudocode.

## G3 Results plots: question, metric, comparison unit, and visual form

Reference locations: P3, p. 13, Fig. 4, and p. 18, Fig. 5. The table below offers design advice organized by comparison task. Plot types absent from the sample must not be described as practices observed in those papers.

- **Signals**: Arbitrarily numbered instances are joined into a trend; every dataset becomes a bar chart; a smooth curve is fitted through only a few points; or timeouts and unfavorable results are removed for appearance.
- **Assessment**: Establish whether the horizontal axis and comparison units have a natural order, whether the data are paired, whether repeated measurements exist, whether the focus is on individual values or distributions, and which metrics and optimization directions are being compared.
- **Revision**: Choose a visual form using the table below, and verify metrics and missing-data statuses before plotting. Generate results plots from real data and reproducible code; do not replace numerical plots with generative images.
- **Review**: The question expressed by the plot matches the conclusion in the text; every value, aggregation, and error range is traceable; and unfinished computations have not been converted into proven results.

| Question to answer | Forms to consider first | Conditions that must be stated |
| --- | --- | --- |
| Exact differences among a few unordered methods | A table, dot plot, or grouped bar chart | The same comparison object, units, and budget; do not connect unordered categories into a trend |
| How a metric changes with an ordered parameter | A line plot with points; a table is also suitable for only a few levels | Use actual parameter values on the horizontal axis; do not smooth or extrapolate without justification |
| How two methods perform on the same set of instances | A paired scatterplot, with an equality line if needed | Each point represents the same instance on both axes; use the same metric on both axes and explain the preferred direction and handling of timeouts |
| The distribution of results across repeated runs or multiple instances | A box plot, scatterplot, or empirical distribution plot | State whether observations come from repeated runs or different instances; do not describe both indiscriminately as random variation |
| Solver performance over time or iterations | A convergence curve or step plot | Distinguish the current solution, the best known feasible solution, and bounds; time and iterations are not interchangeable |
| How two parameters jointly affect a metric | A heatmap or small multiples | Use a clear shared color scale; distinguish missing cells from zero values |
| Trade-offs between two objectives or metrics | A scatterplot | Do not call a collection of points the complete Pareto front without verifying nondominance and completeness |

When bar length represents magnitude, the axis should usually start at zero. If another plot requires rescaling, a truncated axis, or a logarithmic axis, label it clearly and preserve comparability. Do not arbitrarily change panel scales to amplify visual differences. Explain whether error bars represent standard deviation, standard error, confidence intervals, or another quantity; do not add them without repeated experiments or an applicable estimate. For many methods, consider grouping or small multiples first rather than using an ever-increasing number of colors to resolve all crowding.

## G4 Colors: define their meaning, informed by the figures and the author's preferences

- **Signals**: Colors change arbitrarily from one figure to another; color is purely decorative; unordered categorical colors encode continuous values; or red versus green is the only way to distinguish critical states.
- **Assessment**: Determine whether color encodes categories, ordered magnitudes, or positive and negative deviations from a meaningful reference. Check that the same method, object, or state retains a stable meaning across figures.
- **Revision**: Use discrete colors for categories, a sequential colormap for continuous magnitudes, and a diverging colormap with a correctly specified center for deviations around a meaningful central value. These are data-encoding principles, not a purported journal palette. Use a white background and black labels for new figures; give the main data clear, vivid colors and make auxiliary lines less prominent. Supplement categorical colors with markers, line styles, or direct labels.
- **Review**: The figure remains readable at its actual size in the paper; identifying categories does not depend on guessing colors in grayscale or with differences in color vision; and equal values use the same color scale in directly comparable panels.

**The author's explicit preference is for brighter figure colors.** This preference may carry across manuscripts until the user changes it; it is not a Part B requirement. Apply brighter colors to data curves, points, object categories, or group boundaries. Avoid large areas of bright background color that overwhelm the content, and do not interpret this preference as a request for colored text.

| Figure purpose | Reference figures | How to apply the reference in production |
| --- | --- | --- |
| Network schematic | P1, Fig. 1; P3, Fig. 2 | Distinguish objects and relationships with shapes and line styles first; when color is needed, use vivid fills or outlines for important categories |
| Algorithm flowchart | P1, Fig. 5 | Vivid blue, pink, or similar colors can distinguish group boundaries at different levels, while region fills remain pale; operations and decisions must still be identifiable by shapes and arrows |
| A few curves or multiple panels | P3, Figs. 4 and 5 | Blue, orange, and green can serve as reference hues, combined with markers and line styles; choose the number of colors according to the number of categories |
| Spatial distributions with multiple categories | P3, Fig. 6 | Blue, orange, green, purple, red, and similar categorical colors can serve as references, with point shapes separately identifying object types; group categories or split panels first when there are too many |

Do not prescribe dark gray text or present a fixed HEX palette that has not been checked against the figures as a "Part B configuration." Black text and a white background are production defaults chosen for this package in light of the sample and readability; they do not imply that every published figure uses them. There is no need to copy the gray text in P1, Fig. 6. The original color values have not been verified against source files, so only observed hues are recorded. Choose and record specific color values when drawing the figures, making clear that they are implementation choices for the current manuscript rather than exact reproductions of the papers.

Establish a mapping from method name to color, marker, and line style, then retain it in later figures. Do not reassign an existing method's color when fewer categories are shown. The hue references do not prescribe a particular color for the proposed method, and a prominent color does not imply statistical significance. Use line styles only when connecting lines have an interpretive purpose. General colormap resources may guide the choice of a continuous colormap, but do not force the discrete categorical colors above to represent continuous values. Finally, check contrast against the white background, distinguishability in grayscale, and legibility at reduced size.

## G5 Tables: rows define comparison units; columns define essential information

Reference locations: P1, Tables 1, 2, and 6; P2, Tables 1 and 3–6; P3, Table 2. Learn from the comparison tasks these tables perform, rather than copying their parameters, methods, or column counts.

- **Signals**: The reason for including particular columns is unclear; all experimental explanations are squeezed into a table; important statuses are removed to make it narrower; or mixed numbers and text impede comparison.
- **Assessment**: First define the observation or comparison unit represented by one row, then identify the columns needed to answer the question. Decide whether readers need to look up exact values, identify conditions, or compare methods.
- **Revision**: Select from the table below according to the study's needs; do not treat it as a mandatory checklist of tables for every paper. Main tables should support the claims. Detailed instance-level results may go in an appendix or supplementary material, but failures and important counterexamples must remain reflected in the main text's conclusions.
- **Review**: Readers can identify the comparison units, conditions, metrics, units of measurement, aggregation methods, and result statuses; every column serves a purpose.

| Table purpose | Content usually worth including | Content that should not be forced into the table |
| --- | --- | --- |
| Notation | Symbols and meanings for sets, parameters, and variables; separate indices or first-definition locations when needed | Long derivations, proofs, or every temporary algorithm state |
| Literature comparison | Sources, verifiable problem features or assumptions, objectives, methods, and relevant limitations | Long abstracts or advantage columns contrived to favor the current paper |
| Instance description | Instance or group names, sample sizes, and sizes and features that distinguish experimental groups | Information shared by all instances that one sentence in the text can explain |
| Parameter settings | Parameters needing a consolidated comparison, baseline values or levels, and necessary units | A sentence-by-sentence transfer of all hardware and implementation details |
| Method performance | Instance or group, method, solution or bound quality relevant to the claims, time, and result status | Every logged metric without an explanatory purpose |
| Component ablation | Component configurations and key quality and efficiency metrics under the same conditions | Changes to several factors presented as the effect of one component |
| Sensitivity analysis | Parameter levels, relevant response metrics, and necessary summaries and sample sizes | Lengthy mechanism explanations or unverified causal conclusions |

Place methods next to one another when comparing them on the same instance. For many methods, grouped columns or a long-format table may help; parameter comparisons should emphasize parameter levels. Put units in headers, align numbers by column, and match precision to data quality. Use simple horizontal rules and whitespace by default, with limited vertical rules and full-cell shading, but do not claim that a three-rule table is the only permitted format. If a table is too wide, remove redundancy, group content, or split the table before shrinking the font to an unreadable size.

Use table notes only to explain necessary abbreviations, statuses, calculation conventions, and exceptions. Before using bold to highlight results, define the comparison scope, preferred direction, and treatment of ties. The best numerical value does not automatically imply a statistically significant difference. Identify the actual statistic and sample scope for means, geometric means, medians, and similar summaries; do not label different definitions indiscriminately as Avg.

## G6 Abbreviations: reduce repetition without losing meaning

Reference locations: P1, p. 8, Table 1, for short-code explanations, and pp. 32–33, Table 6, for metric explanations; P2, p. 17, for component configurations. These examples support explaining abbreviations; they do not establish that every paper must use the same short names.

- **Signals**: Headers consist entirely of letters; one abbreviation has multiple meanings; a term used only once receives an abbreviation; or a dash represents timeouts, missing data, and infeasibility alike.
- **Assessment**: Consider whether a term recurs, whether a standard abbreviation exists, whether the figure or table is understandable apart from the text, and whether shortening the term would remove conditions that affect interpretation. Distinguish technical abbreviations, mathematical symbols, unit symbols, and result statuses.
- **Revision**: Follow the table below. Define abbreviations at first use in the abstract and the main text according to their respective reading contexts. Provide brief explanations needed to understand each figure or table in its legend, caption, or notes, so readers do not have to search across many pages.
- **Review**: Expand every header, legend entry, and status to its full meaning and check that the values and conclusions remain consistent. No term should have conflicting meanings, and distinct terms should not be conflated.

| Content | Decision on abbreviation | Usable practices and limits |
| --- | --- | --- |
| Established terms used repeatedly | Usually suitable for abbreviation | For example, LP, MILP, and CG, with their full terms at first use; include specific algorithms only when they are actually used |
| Common metrics such as upper and lower bounds | Suitable after definition | UB and LB denote numerical upper and lower bounds; identify the problem and stage to which they apply; do not mechanically equate primal or dual bounds with the same upper or lower bound in both maximization and minimization |
| Units and defined mathematical quantities | Use their standard symbols directly | For example, Time (s), Gap (%), and an explicitly defined n; do not drop units to save width |
| The proposed method and ablation variants | Name them only when repeated use makes it necessary | Preserve published algorithm names; map each manuscript-specific variant's short name to its full configuration, and avoid several nearly identical abbreviations |
| Ordinary short headers | Usually retain readable words | Prefer Time, Cost, Nodes, and Objective value; do not replace them with obscure T, C, N, or O merely to save a few characters |
| Objectives, operational mechanisms, and research assumptions | Usually use brief descriptions | Do not arbitrarily shorten long objective names into undefined letter strings; do not replace all objectives and algorithms in a review with check marks and crosses |
| Qualifiers that determine a metric's meaning | Must not be omitted without explanation | Do not conflate Root gap with Final gap, Best known with Proven optimal, or Wall time with CPU time; long definitions may move to table notes |
| Solver status | Explicitly defined short codes are usable, but statuses must remain distinct | For example, TL may mean that the time limit was reached, while feasibility and optimality statuses are recorded separately; distinguish not run, missing, not applicable, and proven infeasible |

There is no permanent context-free list of words that must never be abbreviated. Clarity and necessity are the criteria. For example, Obj. is acceptable when defined, but Objective value is more direct when table width permits. If an ordinary word is used as a mathematical variable, follow the model definition rather than using this table to prohibit the letter. Tables should omit repetitive wording, not conditions, units, or the meaning of results.

## G7 Production, saving, and final checks

When actual figure production is required, use data-driven plotting libraries for results plots. Use editable vector drawing or structured drawing tools, such as TikZ, Graphviz, or an existing drawing tool, for precise schematics and flowcharts. Choose tools available in the existing environment; do not introduce new dependencies without reason for a simple figure. Generative images must not replace exact connections, formulas, labels, or experimental data.

Retain editable source files or plotting code, input-data locations, and color mappings. Prefer retaining vector masters such as PDF or SVG. For an actual submission task, check the official guidelines for accepted formats, dimensions, resolution, and fonts; do not fix those details here as journal requirements.

Check figures and tables at their final inserted size in the manuscript: readable labels, consistent symbols, no clipping or overlap, matching panel labels and references, unobstructive legends, comparable color scales, distinguishability in grayscale, and agreement with the source data. Captions should state what is shown, explain panels and encodings, and give necessary conditions; leave longer explanations in the text. Do not report a check as passed unless it was actually performed.

## Verified general sources

For observations from the papers, see the [sample records](partb-evidence.md). The sources below supplement color classification and distinguishability only. They do not replace inspection of the Part B figures and must not support claims about the journal's customary style. Verification date: 2026-11-18.

- [Matplotlib: Choosing Colormaps](https://matplotlib.org/stable/users/explain/colors/colormaps.html): Distinguishes colormap types according to data meanings, including categories, ordered magnitudes, and meaningful central values.
- [Okabe and Ito: Color Universal Design](https://jfly.uni-koeln.de/color/): Recommends combining color with shapes, line styles, and labels; used here only as a reference for distinguishability, not as a prescribed palette for papers.
