# Thesis and Final Project Proposal Template — Universitas Darussalam Gontor (LaTeX)

![LaTeX](https://img.shields.io/badge/Language-LaTeX-008080?style=flat-square&logo=latex&logoColor=white)
![Engine](https://img.shields.io/badge/Engine-XeLaTeX-be2d2d?style=flat-square)
![Status](https://img.shields.io/badge/Status-Active-success?style=flat-square)

This template is designed to help students prepare academic documents that comply with the university's formatting standards, covering margin settings, typefaces (including Arabic script), automatic page numbering, and structured bibliography management.

> **Note:** This repository is a **fork** of the original UNIDA Gontor LaTeX template. See the [Fork & Credits](#-fork--credits) section for attribution.

---

## 📋 Key Features

This template is preconfigured to meet academic writing requirements, including:

- **Format Compliance:** Page layout, margins, and Times New Roman typeface are aligned with the UNIDA Gontor thesis writing guidelines.
- **Arabic Language Support:** Uses the XeLaTeX engine and the `polyglossia` package to render Qur'anic verses and Arabic text (Amiri font) with precision.
- **Document Automation:** Table of Contents, List of Figures, and List of Tables are generated automatically.
- **Reference Management:** Integrated with `BibLaTeX` using the _Chicago Manual of Style_ citation style (footnotes) per university standards.

---

## 💻 System Requirements

Before using this template, make sure your machine has the following software installed:

| Software               | Windows                                 | Linux                     | Purpose                                         |
| :--------------------- | :-------------------------------------- | :------------------------ | :---------------------------------------------- |
| **LaTeX Distribution** | [MiKTeX](https://miktex.org/download)   | TeX Live (`texlive-full`) | Core LaTeX compilation engine.                  |
| **Text Editor**        | [TeXstudio](https://www.texstudio.org/) | VS Code / Neovim          | Development environment (IDE) for writing code. |
| **Reference Manager**  | [Zotero](https://www.zotero.org/)       | Zotero                    | Bibliography database management.               |

> **Note:** Windows users are advised to enable the _"Install missing packages on-the-fly"_ option in MiKTeX settings so required packages are downloaded automatically.

---

## 📂 Directory Structure

You only need to edit files in specific directories depending on which part of the manuscript you're working on. The project structure is as follows:

```text
📁 THESIS (or PROPOSAL)
├── 📄 main.tex                <-- Root file (compile from this file)
├── 📄 references.bib          <-- Bibliography database (exported from Zotero)
├── 📁 frontmatter/            <-- Document Front Matter
│   ├── cover.tex              (Title/Cover Page)
│   ├── authorization.tex      (Approval Sheet)
│   ├── abstract.tex           (Abstract)
│   └── ...
└── 📁 mainmatter/             <-- Document Main Content
    ├── chapter-1.tex          (Chapter I: Introduction)
    ├── chapter-2.tex          (Chapter II: Literature Review)
    └── ...etc
```

---

## ⚙️ Compilation Guide

Because this template uses BibLaTeX and Polyglossia, the build sequence is critical to producing a clean document.

### Option A: Using TeXstudio (Recommended)

Open `main.tex`.

Make sure the Build configuration under **Options → Configure TeXstudio → Build** is set to:

- **Default Compiler:** XeLaTeX
- **Default Bibliography Tool:** Biber

Press **F5** (Build & View).

### Option B: Using Visual Studio Code

Make sure the **LaTeX Workshop** extension is installed.

Open `main.tex`.

Open the Command Palette (`Ctrl+Shift+P`), type _"Build with recipe"_.

Select the recipe: **latexmk (xelatex)**.

### Option C: Using the Terminal (Command Line)

Run the following commands in sequence from inside the project directory:

```bash
xelatex main.tex
biber main
xelatex main.tex
xelatex main.tex
```

---

## 📝 Additional Notes

- **Inserting Images:** Place image files in the `assets/` folder, then reference them with `\includegraphics`.
- **Tables:** The `booktabs` package is recommended (`\toprule`, `\midrule`, `\bottomrule`) for a professional table appearance.
- **Troubleshooting:** If an error occurs or the bibliography doesn't appear, delete the auxiliary files (`.aux`, `.log`, `.toc`, `.bbl`) and recompile from scratch.

---

## 🌱 Fork & Credits

This repository is a **fork** of the original UNIDA Gontor LaTeX thesis template, maintained here by [`jaweed3`](https://github.com/jaweed3) for personal use and further customization.

### Original Author

- **Muhammad Dafi Al Haq** — Student of the Informatics Engineering Program, Faculty of Science and Technology, Universitas Darussalam Gontor.
- **Muhammad Rizqi Cahyono** — Student of the Informatics Engineering Program, Faculty of Science and Technology, Universitas Darussalam Gontor.
  Original repository: _(https://github.com/PPTIK-UNIDA-Gontor/latex-thesis-unida)_

### Fork Maintainer

- **[`jaweed3`](https://github.com/jaweed3)** — Fork maintainer; responsible for the English translation, structural adjustments, and any additions made in this copy.

If you use this template, please consider crediting the **original author** above, as the core formatting, layout, and configuration were their work.

---

### ✍️ Contributing

Contributions, fixes, and improvements to _this fork_ are welcome via Pull Requests. For changes that benefit the upstream project, please also open an issue/PR against the [original repository](.) so the broader community can benefit.
