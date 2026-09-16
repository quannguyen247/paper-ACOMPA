# ACOMPA 2026 camera-ready LaTeX project

This repository contains two independent LaTeX deliverables:

- `manuscript/main.tex`: IEEE conference paper in US Letter, two-column format.
- `author-response/response.tex`: point-by-point response to the supplied reviewer comments.

The manuscript uses the official `IEEEtran` conference class. Figure 1 now uses the redrawn vector artwork supplied by the author; its SVG source and cropped PDF derivative are stored at:

- `manuscript/figures/fig1.svg`
- `manuscript/figures/fig1.pdf`

Figure 2 remains the raster image extracted from DOCX V4.0 and is visibly marked as a placeholder in the compiled PDF. Replace `manuscript/figures/fig2_placeholder_docx.png` before camera-ready submission. The Author Response remains marked as a working draft until the final Figure 2 artwork is supplied and checked.

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
