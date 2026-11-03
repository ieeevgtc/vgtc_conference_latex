# VGTC Conference-Style LaTeX Template

LaTeX document class for papers submitted to conferences sponsored by the IEEE Visualization & Graphics Technical Committee (VGTC). You can use this template directly on Overleaf: [IEEE TVCG conference-style template](https://www.overleaf.com/latex/templates/ieee-tvcg-conference-style-template/rsdbysvbxksq).

Make sure your paper adheres to the [VGTC conference publication guidelines](https://tc.computer.org/vgtc/publications/conference/).

Conferences that use the `conf` document option:

- IEEE VIS: Visualization & Visual Analytics (Short Papers, Posters)
- IEEE Virtual Reality
- IEEE Symposium on 3D User Interfaces
- Symposium on Haptic Interfaces for Virtual Environment and Teleoperator Systems
- IEEE Symposium on Asia Pacific Visualisation
- IEEE Symposium on Interactive Ray Tracing
- IEEE Symposium on Volume Graphics

## Contents

| File | Description |
| --- | --- |
| `vgtc.cls` | the VGTC class file (keep it next to your paper or in the TeX search path) |
| `template.tex` | an example paper |
| `template.bib` | its bibliography |
| `template.pdf` | the compiled example (conference mode) |
| `abbrv-doi*.bst` | bibliography styles with DOI output (with/without hyperref, with/without narrow DOIs) |
| `makefile` | compiles the example with latexmk |
| `figs/` | sample images |

## Compiling

Compile with pdfLaTeX and BibTeX — on [Overleaf](https://www.overleaf.com/latex/templates/ieee-tvcg-conference-style-template/rsdbysvbxksq) or locally with any LaTeX distribution (e.g., [TeX Live](https://www.tug.org/texlive/), [MacTeX](https://www.tug.org/mactex/), [MiKTeX](https://miktex.org/)):

```sh
make          # compile to PDF
make watch    # recompile on every change
make clean    # remove generated files
```

The makefile uses [latexmk](https://ctan.org/pkg/latexmk) and detects the main file (the `.tex` containing `\documentclass`), so renaming `template.tex` is fine. Without make, run `latexmk -pdf template`.

## Notes

- Use PDF, PNG, or JPG figures; convert EPS files with `epstopdf`.
- All fonts must be embedded in the final PDF — the default with pdfLaTeX; verify with `pdffonts template.pdf`.
- Problems or questions? Please [open an issue](https://github.com/ieeevgtc/vgtc_conference_latex/issues).
