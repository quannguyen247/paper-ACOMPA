# ACOMPA 2026 camera-ready LaTeX project

This repository contains two independent LaTeX deliverables:

- `manuscript/main.tex`: IEEE conference paper in US Letter, two-column format.
- `author-response/response.tex`: point-by-point response to the supplied reviewer comments.

The manuscript uses the official `IEEEtran` conference class. At the author's request, the two current figure files are the raster images extracted verbatim from DOCX V4.0 and are visibly marked as placeholders in the compiled PDF. Replace both files before camera-ready submission:

- `manuscript/figures/fig1_placeholder_docx.png`
- `manuscript/figures/fig2_placeholder_docx.png`

The Author Response is likewise marked as a working draft because it would be inaccurate to claim that the reviewer's figure-quality concern has been resolved before the final redraws are supplied.

## Build

```sh
cd manuscript
latexmk -pdf -interaction=nonstopmode -halt-on-error main.tex

cd ../author-response
latexmk -pdf -interaction=nonstopmode -halt-on-error response.tex
```

The current placeholder PDFs are named:

- `manuscript/ACOMPA2026_PQC_IoT_IEEE_PLACEHOLDERS.pdf`
- `author-response/ACOMPA2026_Author_Response_DRAFT.pdf`
