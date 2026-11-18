# Checked Part B Examples and Transfer Rationale

Inspection date: 2026-11-18. This record covers the locations actually checked, not a word-by-word review of entire papers. All three papers appeared in Transportation Research Part B: Methodological. The first two concern exact pickup-and-delivery algorithms; the third includes two-echelon vehicle routing in dynamic logistics and provides additional examples of visual organization.

## P1 Su et al. (2023): an exact pickup-and-delivery algorithm

Su, E.; Qin, H.; Li, J.; Pan, K. *An exact algorithm for the pickup and delivery problem with crowdsourced bids and transshipment*. 177, 102831. [DOI](https://doi.org/10.1016/j.trb.2023.102831); [repository record](https://ira.lib.polyu.edu.hk/handle/10397/106859); [full text](https://ira.lib.polyu.edu.hk/bitstream/10397/106859/1/Su_Exact_Algorithm_Pickup.pdf).

This is the pre-publication author manuscript in the institutional repository, with 47 pages. Printed and physical PDF page numbers coincide. The text and tables listed below were checked, and images of pages 3, 8, 9, 10, 15, 17, 32, and 39 were inspected. Prose and pseudocode on pages 4–7, 21, and 23 were also checked as text. Red text and blue citation links in this author manuscript are not treated as body-text color standards.

| Location | Observed organization | Transfer and limits |
| --- | --- | --- |
| p. 3, Figs. 1 and 2 | Shapes distinguish network objects and line styles distinguish relationships; a separate figure shows interactions along participant timelines | Separate spatial relationships from operational timing; do not confuse a business sequence with algorithm control flow |
| pp. 4–5, closing introduction | The mechanism leads to decisions, coordination difficulties, and a solution-method gap; a roadmap follows the contributions | Learn the connections without reusing the setting, gap, or contribution wording |
| pp. 5–8, Section 2 | An opening introduces two research directions and their intersection | Use when the research strands fit; author-led sentences and local chronology remain possible within a topic |
| p. 8, Table 1 | Check marks encode defined binary features; text or explained short codes encode other features | Match the representation to the information type; do not turn every column into check marks |
| pp. 9–10, Table 2 | Sets, indices, parameters, and variables are grouped, with first-appearance sections | Adapt categories and columns to retrieval needs rather than requiring three categories or two columns |
| pp. 14–15, model (1) and following paragraph | A complete formulation precedes one continuous explanation of the objective, constraint groups, and domains | Supports consolidated explanation, without requiring a single paragraph in every paper |
| p. 17, Fig. 5 | Blue outer and pink inner boundaries distinguish nested processes; decision exits, return edges, and termination paths are explicit | Draw control relationships first, then show hierarchy with group boundaries; do not copy the algorithm's conditions |
| pp. 21 and 23, Algorithms 1 and 2 | Control logic calls subroutines and refers complex criteria back to the text | Inputs and outputs can be conveyed through parameters and state changes, without separate fields |
| pp. 32–33, Table 6 and explanation | Component configurations form column groups; status, quality, and effort are reported separately | Explain short metric names nearby, limit the comparison scope, and independently check consistency between headers and explanations |
| p. 39, Fig. 6 | Blue and orange curves also use line styles; some figure text is gray | This is an observation, not a gray-text requirement; do not copy the placement of a special baseline category at the end of a numerical parameter axis |

## P2 Sun et al. (2018): time-dependent pickup and delivery

Sun, P.; Veelenturf, L. P.; Hewitt, M.; van Woensel, T. *The time-dependent pickup and delivery problem with time windows*. 116, 1–24. [DOI](https://doi.org/10.1016/j.trb.2018.07.002); [full text](https://pure.tue.nl/ws/files/103558039/1_s2.0_S0191261518301231_main.pdf).

This is the published version. The repository PDF has 25 pages including an initial cover, so physical page numbers are one greater than printed page numbers. The following locations were checked in extracted full text. Page images were not successfully obtained; this source does not support judgments about colors, font sizes, lines, or layout.

| Location (printed pages) | Observed content organization | Transfer and limits |
| --- | --- | --- |
| p. 15, Table 1 and experimental settings | The table gives attributes distinguishing instance groups; shared execution conditions appear in prose | Use tables for comparison rather than moving every setting into them |
| pp. 16–17, Tables 3–6 | Solved proportions, time, gaps, and component combinations are distinguished, with explanations for short codes | Organize tables by evaluation question; do not substitute time for quality or copy instance scales and variants |

## P3 Zamal et al. (2025): dynamic logistics with two-echelon routing

Zamal, M. A.; Schrotenboer, A. H.; van Woensel, T. *End-to-end logistics in metropolitan areas: A stochastic dynamic order-assignment and dispatching problem*. 199, 103249. [DOI](https://doi.org/10.1016/j.trb.2025.103249); [full text](https://pure.tue.nl/ws/portalfiles/portal/368200498/1-s2.0-S0191261525000980-main_1_.pdf).

This is the published version. The repository PDF has 22 pages including an initial cover, so physical page numbers are one greater than printed page numbers. The corresponding text and images on physical pages 6, 14, and 19 were checked. This is not a comparable performance benchmark for exact algorithms for static pickup and delivery; only relevant visual organization is transferred.

| Location (printed pages) | Observed presentation | Transfer and limits |
| --- | --- | --- |
| p. 5, Fig. 2 | A black-and-gray network diagram distinguishes objects and relationships through shapes, fills, and line styles | Encode structure geometrically first; not every relationship needs a color |
| p. 13, Fig. 4 | Blue, orange, and green accompany markers; current and best-so-far values are distinguished, with parameter trajectories in another panel | Name curves according to the actual quantity; separate quantities with different units when helpful |
| p. 13, Table 2 | Parameters are grouped, using horizontal rules and whitespace for hierarchy | Tabulate parameters that benefit from consolidated comparison, not every explanatory sentence |
| p. 18, Fig. 5 | Several panels show different responses to one varying parameter | Group panels around a research question rather than forcing them onto a dual-axis chart |
| p. 18, Fig. 6 | Red, blue, green, orange, and purple distinguish categories; point shapes encode object types separately | Vivid categorical colors are possible, not a journal-wide palette; check dense points and legends at final size |

## Applying these observations

- Use the locations above with G1–G6 of the [figure and table guidance](figures-and-tables.md). Color categories come from visual inspection; original RGB/HEX values have not been verified and must not be invented as source-derived values.
- Black body and table text is visible on inspected P1 and P3 pages, while some P1 result-plot text is gray. This difference does not establish a gray-text requirement. Black labels for new figures are a design choice informed by readability and the sample.
- The author explicitly prefers brighter figure colors. Keep this preference separate from source observations and apply it to data lines, markers, and category boundaries rather than coloring all text.
- Assess whether a published practice suits the current information. Publication alone does not justify copying crowded legends, particular axis treatments, or revision colors in an author manuscript.
- Store bibliographic details, locations, and original summaries only; do not bundle paper PDFs or copied figures. Check current submission rules separately against official guidance.
