# A Literature Survey on AI Tools and Their Impact on Software Quality

**Author:** Filippo Castagnola  
**Institution:** Athens University of Economics and Business  
**Date:** January 2026  

---

## Overview
This repository contains the LaTeX source code and compiled PDF of my literature survey examining the role of Artificial Intelligence in modern software engineering. The study analyzes how AI-assisted development tools impact critical software quality characteristics—such as maintainability, reliability, and security—evaluating them against the **ISO/IEC 25010** software quality model.

While modern AI tools significantly accelerate developer productivity and reduce repetitive tasks, this survey concludes that a **human-in-the-loop** paradigm remains essential to prevent quality degradation, manage long-term technical debt, and avoid over-reliance on automated systems.

## Repository Structure
The document is written and typeset in LaTeX. The project files are organized as follows:

```text
├── main.tex           # Root document structuring the survey and importing subfiles
├── introduction.tex   # Introduction to software quality and AI adoption trends
├── chapter1.tex       # Background: ISO/IEC 25010, technical debt, and ethical/legal aspects
├── chapter2.tex       # Taxonomy and classification of AI development tools
├── chapter3.tex       # Code Generating AIs (GitHub Copilot, Claude, Cursor IDE)
├── chapter4.tex       # Code Analysis AIs (Qodo, CodeRabbit, CodeAnt AI)
├── chapter5.tex       # Test Automation AIs (Mabl, Testim, Testsigma)
├── chapter6.tex       # Future directions: evaluation metrics, maintainability, trust, and ethics
├── conclusion.tex     # Final synthesis of findings and trade-offs
├── ref.bib            # BibTeX bibliography of referenced reports, docs, and benchmarks
└── images/            # Figures, charts, and IDE/UI screenshots
```

## Key Findings
* **Code Generation:** Tools such as Cursor, Claude, and GitHub Copilot streamline boilerplate implementation and rapid prototyping, but can introduce subtle logical flaws or security vulnerabilities without thorough human code review.
* **Code Analysis:** AI-driven static analysis platforms (Qodo, CodeRabbit, CodeAnt AI) help curb technical debt and enforce coding standards during pull requests, though human judgment is still required for complex architectural decisions.
* **Test Automation:** Tools leveraging smart locators and natural language processing (Mabl, Testim, Testsigma) improve regression coverage and reduce UI test fragility, at the trade-off of less fine-grained control compared to traditional script-based testing.

## Building the PDF
To compile the document locally from the LaTeX source files:

1. Ensure you have a TeX distribution installed (e.g., **TeX Live**, **MiKTeX**, or **MacTeX**), or import the repository into **Overleaf**.
2. Compile `main.tex` using `pdflatex`:
   ```bash
   pdflatex main.tex
   ```
3. Run `bibtex` (or `biber`, depending on your bibliography backend) to process `ref.bib`:
   ```bash
   bibtex main
   ```
4. Re-run `pdflatex main.tex` twice to resolve all cross-references, table of contents entries, and citations.