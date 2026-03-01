<div align="center">
  <a href="#">
    <img src="img/logo/logo_uit_20-02.png" alt="HCMUIT Logo" width="300" />
  </a>

  <h3>HCMUIT Course Thesis Template</h3>

  <p>
    A free LaTeX template for end-of-semester course projects at UIT —<br/>
    Faculty of Computer Networks and Communications.
  </p>
  <a href="#getting-started"><strong>Explore the docs »</strong></a>

  <br/>
  <br/>

  ![LaTeX](https://img.shields.io/badge/LaTeX-008080?style=for-the-badge&logo=latex&logoColor=white)
  ![License](https://img.shields.io/badge/License-Academic%20Use-blue?style=for-the-badge)
  ![Platform](https://img.shields.io/badge/Overleaf-compatible-47A141?style=for-the-badge&logo=overleaf&logoColor=white)
</div>

---

## About The Project

This is a free, non-profit LaTeX template built specifically for students of the **Faculty of Computer Networks and Communications** when completing their end-of-semester course projects.

Writing a report that is correct, consistent, and well-formatted is a challenge — especially when working in a group with multiple people editing at the same time. Common problems when using Google Docs or Microsoft Word:

- **Math equations:** Difficult to type, prone to formatting errors when copying between sections.
- **Inconsistent formatting:** Font size, headings, captions, and numbered lists vary from chapter to chapter.
- **References:** Manual management is time-consuming and error-prone.

This template solves all of those problems. You only need to focus on the **content** — formatting is already taken care of.

---

## Project Structure

```
Template/
├── main.tex                  ← Entry point — compile this file
├── uit-thesis.sty            ← Style package (fonts, layout, packages)
├── README.md
│
├── misc/                     ← Front / back matter pages
│   ├── cover.tex             ← Title page
│   ├── abstract.tex          ← Abstract
│   ├── ack.tex               ← Acknowledgements
│   ├── abbrev.tex            ← List of abbreviations
│   └── council.tex           ← Defence committee info
│
├── chapters/                 ← Main chapter content
│   ├── chapter1.tex          ← Chapter 1: Introduction
│   ├── chapter2.tex          ← Chapter 2: Theoretical Background
│   ├── chapter3.tex          ← Chapter 3: Methodology
│   ├── chapter4.tex          ← Chapter 4: Implementation & Testing
│   └── chapter5.tex          ← Chapter 5: Evaluation & Future Work
│
├── references/               ← Per-chapter bibliographies
│   ├── chapter1/refs.bib
│   ├── chapter2/refs.bib
│   ├── chapter3/refs.bib
│   ├── chapter4/refs.bib
│   └── chapter5/refs.bib
│
├── appendix/                 ← Appendices
│   ├── appendix_a.tex        ← Appendix A: Work assignment table
│   ├── appendix_b.tex        ← Appendix B: Teamwork evidence
│   └── appendix_c.tex        ← Appendix C: AI usage transparency
│
└── img/                      ← Images and figures
    ├── logo/                 ← UIT and faculty logos
    ├── chapter1/
    ├── chapter2/
    ├── chapter3/
    ├── chapter4/
    └── chapter5/
```

---

## Getting Started

### Requirements

| Component            | Software                                                                 |
|----------------------|--------------------------------------------------------------------------|
| TeX distribution     | [TeX Live 2022+](https://www.tug.org/texlive/) or [MiKTeX](https://miktex.org/) |
| Compiler             | pdfLaTeX or XeLaTeX                                                      |
| Bibliography backend | Biber                                                                    |

### Recommended Editors

- **VS Code** + [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop) extension
- **TeXstudio**
- **Overleaf** (online, no installation required)

### Compiling

Using `latexmk` (recommended):

```bash
latexmk -pdf -bibtex main
```

Or manually (Biber must be run **twice** due to per-chapter bibliographies):

```bash
pdflatex main
biber     main
pdflatex main
biber     main
pdflatex main
```

Clean auxiliary files:

```bash
latexmk -c
```

---

## Workflow

| Step | Task                              | File                                        |
|------|-----------------------------------|---------------------------------------------|
| 1    | Edit group / supervisor info      | `misc/cover.tex`                            |
| 2    | Write chapter content             | `chapters/chapterN.tex`                     |
| 3    | Add references for each chapter   | `references/chapterN/refs.bib`              |
| 4    | Place figures for each chapter    | `img/chapterN/`                             |
| 5    | Fill in the list of abbreviations | `misc/abbrev.tex`                           |
| 6    | Write abstract and acknowledgements | `misc/abstract.tex`, `misc/ack.tex`       |

> Search for the keyword **`TODO`** in any `.tex` file to find placeholders that need to be filled in.

---

## Important Notes

- Citations use **BibLaTeX + Biber** (not classic BibTeX).
- Each chapter has its **own bibliography section** at the end, with citation numbers increasing continuously across the whole document (`[1]`, `[2]`, ...). This requires Biber to be run **twice** — see the compile instructions above.
- Logo files must be placed in `img/logo/` matching the exact filenames referenced in `misc/cover.tex` (`logouit20-02.png` and `logoKhoa_Basic_latex.png`).

---

## License

This template is free to use for academic purposes.  
Commercial use is not permitted without prior consent.
