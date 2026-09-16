# ACOMPA 2026 camera-ready LaTeX project

This repository contains two independent LaTeX deliverables:

- `manuscript/main.tex`: IEEE conference paper in US Letter, two-column format.
- `author-response/response.tex`: point-by-point response to the supplied reviewer comments.

The manuscript uses the official `IEEEtran` conference class. Both revised figures use author-supplied/redrawn vector artwork. The editable SVG sources and cropped vector-PDF derivatives used by LaTeX are stored at:

- `manuscript/figures/fig1.svg`
- `manuscript/figures/fig1.pdf`
- `manuscript/figures/fig2.svg`
- `manuscript/figures/fig2.pdf`

## Build

```sh
cd manuscript
latexmk -pdf -interaction=nonstopmode -halt-on-error main.tex

cd ../author-response
latexmk -pdf -interaction=nonstopmode -halt-on-error response.tex
```

Final PDFs:

- `manuscript/ACOMPA2026_PQC_IoT_IEEE_CAMERA_READY.pdf`
- `author-response/ACOMPA2026_Author_Response.pdf`

The paper is seven US Letter pages in IEEE two-column conference format. Submit it through the IEEE CPS link supplied by ACOMPA 2026. Run a separate PDF eXpress check only if the CPS workflow or the conference provides a Conference ID; that external validation is not part of the local build.
