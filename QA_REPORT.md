# ACOMPA 2026 project QA report

Date checked: 2026-09-16 (Asia/Ho_Chi_Minh)

## Scope and source precedence

- The submitted PDF V2.1 was treated as the older conference version.
- The DOCX V4.0 was treated as the latest content source.
- The manuscript prose, measurements, tables, and 18-reference order follow V4.0. No new experiment, baseline, or measured value was invented.
- At the author's latest instruction, the two images embedded in DOCX V4.0 are used as temporary placeholders. The prior TikZ redraws were removed.

## Mechanical checks

- Paper: official local `IEEEtran.cls`, conference mode, 10 pt, US Letter, two columns, 6 pages.
- Author Response: US Letter, single column, 2 pages, visibly marked as a working draft.
- Paper figures: exactly two PNG source images, both on page 4.
- Placeholder source hashes:
  - Fig. 1: `83eed47ee7fec9dd2724ed940c416f2359565330e6218e408bd93c5248e23324`
  - Fig. 2: `10a4ec6c85ec13e8b455da093bd63adb760fdb835b6a8d67b93ec84889e796e2`
- The hashes match the two PNG files extracted from DOCX V4.0.
- Effective image resolution in the compiled paper: approximately 142 ppi (Fig. 1) and 247 ppi (Fig. 2).
- All PDF fonts are embedded Type 1 fonts.
- No undefined citation, missing reference, overfull box, compilation error, form, JavaScript, or encryption was detected.
- Four nonfatal underfull warnings remain in the paper. Visual inspection of all six pages found no clipping, overlap, or text outside the IEEE margins.
- References are numbered [1]--[18] in the V4.0 order. DOI fields remain in `references.bib`; the official `IEEEtran.bst` omits many DOI fields in rendered entries.
- Key experimental values in V4.0 were checked against the final PDF, including QEMU memory/test counts, single-operation timings, signature/ciphertext sizes, stress timings, RSS values, and the 29.46 s observation.
- Normalized word-sequence comparison between DOCX V4.0 XML and the compiled manuscript produced 0.9257 similarity. The remaining differences are dominated by figure text, bibliography formatting, headings, and LaTeX/PDF extraction order.

## Visual and editorial review

- Pages 1--3: title, authors, abstract, keywords, related work, architecture text, and Table I are readable and aligned.
- Page 4: both placeholders, captions, notices, and the transition into Section IV are readable; neither image is cropped or distorted.
- Page 5: Table II and experimental analysis are aligned within the two-column grid.
- Page 6: conclusion and all 18 references fit without an orphaned final reference page.
- Author Response: reviewer statements are separated from author responses; no claim is made that final vector artwork already exists.
- The Author Response must be revised after the final figures are supplied. Its working-draft warning is intentional.

## Scores

| Criterion | Score | Basis |
|---|---:|---|
| Content fidelity to DOCX V4.0 | 9.4/10 | Body, values, tables, and reference order retained; normal IEEE bibliography formatting changes remain. |
| IEEE paper formatting | 9.7/10 | Official conference class, US Letter, two columns, 6 pages, embedded fonts, clean margins. |
| Technical and argumentative discipline | 9.2/10 | Claims are bounded to the QEMU/prototype evidence; no unperformed baseline is invented. |
| Figure readiness against reviewer concern | 4.5/10 | Two DOCX images are intentionally placeholders; the reviewer concern is not yet resolved. |
| Author Response readiness | 7.5/10 | Complete and factual as a working draft, but the figure response must be finalized after redraw. |

**Current camera-ready readiness: 7.8/10.** The paper structure and text are near ready, but the two placeholder figures and the corresponding Author Response language must be replaced before submission. PDF eXpress validation has not been run.
