# CryptoTeX

CryptoTeX is a LaTeX template which is optimized for writing LaTeX for cryptography research. It includes:
- common macros and packages (such as [cryptocode](https://ctan.org/pkg/cryptocode))
- formatting for common conference formats
- [cryptobib](https://cryptobib.di.ens.fr/) with cross-references for easy citation management

> [!TIP]
> If you'd like to use this template, please use the green **"Use this template" button** at the top right of this page (next to the Star button). This will give you a clean git history, allow your repo to be private, and credit this template :) Read more about repository templates [here](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template).

> [!CAUTION]
> This repo does not track changes in conference format requirements. You are responsible for ensuring your manuscript meets the conference submission guidelines.

## Setup
- This repo uses [latexmk](https://www.cantab.net/users/johncollins/latexmk/). Add the `-outdir=build` flag to your `latexmk` command (via [VSCode settings](https://github.com/James-Yu/LaTeX-Workshop/wiki/Compile#latex-tools), `latexmkrc` file, etc.).
- To set up cryptobib, run `git submodule update --init --recursive`

## Usage
- **Authors:** Enter the authors and their information (emails, affiliation, etc.) in `authors/authors.tex`. If you have a different number of authors or institutions than the sample (2 authors, 3 institutions), you can add/remove the corresponding portions of the author blocks in the format files (`authors/{ccs,eprint,iacr,ieee}.tex`).
- **Content:** Start writing your paper in `src/`! The template assumes one file per section and already includes `src/{abstract,intro,appendix}` files.
- **Format and Metadata:** Edit the overall paper structure and set flags in `main.tex`. This includes:
  - _Switches for the format:_ anonymous, full version, activate/deactivate author comments, paper layout (IEEE, IACR, ACM CCS conferences; default is full-page LNCS).
  - _Paper info:_ Title, keywords
  - _Structure:_ Organize the content from `src/` files into sections and appendices
