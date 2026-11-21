# Setup & Compilation Guide

Instructions for the [UNIDA Gontor LaTeX thesis template](README.md).

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

[← Back to README](README.md)
