# Vector Embedding Compatibility Design

**Author:** Harikrishnan M  
**University Number:** TCR24CS032

## Project Overview
This repository contains the formal design specification, technical report, and implementation details for the **Capability Composition Model and Vector Space Framework**. The primary objective of this experiment is to formulate a vector embedding framework that maps complex operational workflows into a unified, computable vector space, enabling formal compositional reasoning.

## Mathematical Formulation
Capabilities are embedded into a unified $2d+3$ dimensional vector space. This structure allocates:
* $d$ dimensions for preconditions ($\vec{p}$)
* $d$ dimensions for effects ($\vec{e}$)
* $3$ dimensions for operational attributes: cost ($c$), reliability ($r$), and availability ($a$)

For a given capability $C$, the vector is structured as:
$$\mathbf{v}_C = [\vec{p}^{\,T}, \vec{e}^{\,T}, c, r, a]^T \in \mathbb{R}^{2d+3}$$

## Repository Structure
* `docs/`: Contains the LaTeX source files for the formal design and technical reports.
  * `formal_design.tex`: Formal mathematical definitions of the vector space and composition operators.
  * `technical_report.tex`: Experimental methodology, implementation results, and architectural analysis.
  * `build_docs.sh`: Shell script to compile the LaTeX documents into PDFs.

## Experimental Results
The experiment validates:
1. **Compatibility metric evaluation** via inner products.
2. **Recursive composition operator correctness** preserving exact mathematical constraints.
3. **Cosine similarity distinction** across implementation variants.
4. **Filtering** of irrelevant capabilities.

## Build Instructions
To compile the LaTeX documentation into PDF format, ensure you have a LaTeX distribution (e.g., `texlive`) installed, then execute the build script:

```bash
cd docs
rm -f *.aux *.log *.pdf
./build_docs.sh
