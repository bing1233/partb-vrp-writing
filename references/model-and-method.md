# Problem, notation, model, and method

## M1 Problem description: introduce the system and decisions before the mathematics

- **Signals**: The first paragraph is crowded with symbols; the operational description does not match the objects in the model; key assumptions appear only after the model.
- **Assess**: Can readers identify the system, the decision maker, the available information, the decisions, and the objective used to evaluate them? Check for confusion among real-world facts, research assumptions, and experimental settings.
- **Revise**: Explain these relationships first, then introduce sets, the network, time, and resources as the narrative develops. For routing on a graph, describe the graph, nodes, arcs, and their meanings in the problem description. State important assumptions before they first affect the feasible region or theory.
- **Recheck**: Every important model object has a conceptual basis, and every assumption affecting the results can be found. Deliberate modeling choices are not presented as industry-wide facts. Do not require separate sections for the problem description and mathematical model.

## M2 Notation tables: reference and first definitions

- **Signals**: Several independent quantities share one row; parameters and variables are confused; index meanings are unclear; a model notation table includes temporary search states.
- **Assess**: Track each symbol's first use, meaning, category, subscripts, and units. Check for one symbol with multiple meanings or multiple names for the same object. Whether a quantity is known before a decision must be determined from the actual model, not guessed from its letter.
- **Revise**: Group notation into sets, parameters, and decision variables as appropriate for the current model. Explain indices with their sets or give them a separate category if needed. As a general rule, use one row per independent symbol, adding units, domains, and indices where necessary. Define algorithm states, temporary sets, and auxiliary proof quantities in the relevant text, with a local table if there are many. Move long conditions and derivations to the main text.
- **Recheck**: Readers can find a clear definition when they first need a symbol, and its meaning is consistent across prose, equations, tables, and pseudocode. A later notation table does not justify leaving a symbol unexplained at its first occurrence.

“Symbol | Meaning” is a starting point; add columns such as units, domains, or the location of the first definition when they offer real reference or comparison value. See [P1, Table 2](partb-evidence.md) for an actual example that differs from a fixed three-category, two-column layout. A large notation table is not mandatory, and unused categories should not receive empty groups.

## M3 Model: present it in full, then explain it in order

- **Signals**: Equations and explanations repeatedly interrupt one another; explanations jump back and forth; indices are incomplete; the text attributes functions to constraints that they do not perform.
- **Assess**: Check each group's actual mathematical role, applicable indices, variable domains, and verbal interpretation. Confirm only roles supported by the existing equations. When a concern arises, distinguish an omission in presentation from a substantive issue requiring a model change.
- **Revise**: Introduce the necessary variables and modeling relationships, then present the objective, logically ordered constraint groups, and variable domains. Follow with a consolidated explanation in equation-number order. Use connected prose by default rather than a bullet for each explanation. Whether the explanation should form one paragraph depends on the manuscript's preferences. Present and explain multiple independent models separately.
- **Recheck**: Every objective term, constraint group, and variable domain is accurately explained. Distinct functions are not collapsed into “the remaining constraints ensure feasibility.” Give the full scope of indexed constraints, using universal quantifiers consistently where appropriate; do not mechanically add quantifiers to the objective or every definition.

A possible structure for the explanatory prose is: what the objective measures and the role of each term → service and route relationships → time and resource relationships → links among decisions → variable domains. Follow the actual equation order in the manuscript. Explain groups through statements such as “Constraints (a)–(b) ensure the following relationship,” rather than translating each symbol individually.

If the manuscript requires “the objective and all constraints to be explained in one continuous paragraph,” record and follow that preference in the manuscript's context. Do not turn it into a mandatory rule for all Part B papers.

A verified example is [P1, model (1) on pp. 14–15 and the following text](partb-evidence.md). Learn from the transition between model presentation and explanation; the constraint groups and their roles must still follow the current manuscript's equations.

When examining mathematical concerns, relevant checks may include subscripts and set ranges, dimensional consistency, boundary nodes, variable activation conditions, bounds, and linking relationships. Report an issue only when evidence supports it. Do not claim that every model lacks a particular type of constraint merely to fill a checklist. Do not claim correctness has been proved without completing a proof.

## M4 Algorithm framework: make interfaces and guarantees explicit

- **Signals**: The section starts with acceleration techniques before explaining the solution framework; the roles of the master problem and subproblems are confused; branching rules are disconnected from pricing; every removal is called pruning.
- **Assess**: Trace how inputs lead to the final output, distinguishing core solution steps from optional acceleration steps. Compare the prose, pseudocode, flowchart, and any available implementation records.
- **Revise**: Present the overall framework first, followed by the core subproblems and acceleration strategies. For decomposition, explain each problem's variables, inputs, outputs, and feedback. For branching, explain the branching objects, rules, and how the resulting constraints enter subsequent solution steps. Elaborate on these mechanisms only when they are part of the actual method.
- **Recheck**: Modules use consistent objects and update orders. Guarantees of exactness, feasibility, termination, or optimality have corresponding conditions; empirical performance cannot establish such guarantees.

Classify and describe operations by their actual roles: when preprocessing occurs and the basis for its reductions; which infeasible extensions feasibility pruning rules out; what alternative states dominance rules retain; and which bounds objective-bound pruning compares and under which optimization direction it is safe. Preprocessing may itself rely on feasibility or objective bounds, so do not treat “stage of execution” and “logical basis” as mutually exclusive categories.

## M5 Pseudocode and flowcharts: make state changes traceable

- **Signals**: Pseudocode consists only of long prose; states or updates are undefined; stopping conditions are absent; the flowchart shows only sequential boxes even though the text describes loops.
- **Assess**: Manually trace one iteration or pass through the procedure. Check initialization before use, the point in time represented by states used in conditions, loop return points, outputs after stopping, and incomplete execution cases. Check against the actual algorithm; writing conventions must not determine the author's execution order.
- **Revise**: Specify the inputs, initialization, loops, conditions, state updates, stopping rules, and outputs actually needed. Inputs may be explained through parameters or context, and outputs may be return values or explicit state updates. Do not require separate input/output fields or add meaningless return values to subroutines that update in place. Refer nontrivial steps to subroutines or propositions defined in the text, keeping rationale and proofs outside the pseudocode. Retain the project's existing LaTeX algorithm environment rather than changing packages without a reason.
- **Recheck**: Every symbol and subroutine is defined. Prose, code, and figures use the same conditions and order. What is returned upon early stopping, and the associated guarantees, are clear. Do not require every algorithm to contain upper bounds, lower bounds, branching, or labels.

For pseudocode, see how the control logic connects to the criteria in the text in [P1, Algorithms 1 and 2 on pp. 21 and 23](partb-evidence.md). For flowchart shapes, hierarchy, and colors, see [G2 and G4](figures-and-tables.md). Keep graphical conventions consistent, label decision exits with conditions, and make arrow directions and loop closure explicit. If a figure adds no structural information, do not duplicate the pseudocode merely to include another figure.

When execution orders conflict, locate both versions and the conflicting state dependencies. Check an existing implementation if one is available. If the current material is insufficient to decide, preserve the unresolved conflict and request the minimum information needed. Do not choose the version that reads more smoothly and then declare consistency.

## M6 Propositions and proofs: do not lose conditions through concise wording

- **Signals**: Results lack conditions or quantifiers; corollaries are counted again as independent innovations; proofs are long, but the actual algorithm uses different assumptions.
- **Assess**: Check the objects, conditions, conclusions, and dependencies. Determine whether the theoretical results actually cover the cases used by the implemented algorithm.
- **Revise**: Retain complete propositions and the intuition needed for understanding in the main text. Long technical proofs may move to an appendix with accurate references. Fill obvious gaps in derivations only from the available material. Mark unfinished derivations as unverified; examples cannot replace proofs.
- **Recheck**: After proofs move, readers can still understand the guarantees and their conditions from the main text. The algorithm remains within the theory's scope. Numerical observations, intuitive explanations, and proved results remain distinct.
