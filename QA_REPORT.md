# ACOMPA 2026 project QA report

Date checked: 2026-09-16 (Asia/Ho_Chi_Minh)

## Scope and source precedence

- The PDF V2.1 was treated as the older submitted version seen by the reviewer.
- The DOCX V4.0 was treated as the latest content source. Its prose, measurements, tables, title, author order, and 18-reference order are the basis of the LaTeX manuscript.
- The central contribution remains the same as in V2.1: a tiered IoT deployment model that assigns ML-KEM to session establishment, ML-DSA to regular authentication, and SLH-DSA to infrequent high-assurance tasks.
- The four raster figures in V2.1 were consolidated into two vector schematics, following the two-figure organization in V4.0. This changes presentation, not the architecture or measured results.
- No experiment, baseline, numerical result, or cryptographic performance claim was invented.

## Content audit

- Order-independent normalized-token comparison against V4.0 gives 0.9184 multiset Jaccard similarity and 95.87% retention of V4.0 tokens. Differences are dominated by figure text, IEEE bibliography/layout extraction, and a small number of explicit technical clarifications.
- V4.0 is a substantive expansion and rewrite of V2.1, not merely a figure refresh. It adds the explicit placement table, migration metadata/policy, failure handling, and more bounded evaluation language; it also omits some older implementation-detail wording such as explicit DMA/PCIe and design-for-test discussion. The final paper follows V4.0 on these points while preserving V2.1's central tiered-placement argument and measurements.
- The final PDF contains all 21 checked experimental values from V4.0: QEMU memory/test counts; ML-KEM, ML-DSA, and SLH-DSA single-operation timings and object sizes; all seven Table II elapsed/RSS/payload rows; and the 29.46 s observation.
- Title and author order are unchanged. Paper ID #4 is retained in PDF metadata and displayed in the Author Response.
- Deliberate textual corrections are limited to: naming AES-GCM and ChaCha20-Poly1305 as AEAD schemes; distinguishing AXI/AHB/APB bus interfaces from MMIO; clarifying that the gateway does not receive a device-bound private key; and aligning the Fig. 2 description with the direct 64-bit versus gateway-assisted constrained-node paths.
- All 18 citations resolve. Standards references were spot-checked against the official NIST, W3C, and RFC records; no reference was silently replaced.

## Mechanical and visual checks

- Paper: local official `IEEEtran.cls`, conference mode, 10 pt, US Letter, two columns, 7 pages. This is within the stated Regular Paper limit of 8 pages.
- Author Response: US Letter, single column, 2 pages.
- Figures: exactly two final vector figures. Both SVG files contain vector paths with no embedded raster image, and `pdfimages -list` reports no raster image in the final paper.
- Figure source hashes:
  - Fig. 1 SVG: `e630a503227cea7d23b8f590cb0105f93c4aede290f27588bac775f5da89e0e5`
  - Fig. 2 SVG: `c1d4765523b558436b5a25d1fa7d0748149d080d8dac77cc2ba818bae5613054`
- Fig. 1 is on page 4; Fig. 2 is on page 5. Both were reviewed at full-page resolution. Labels, arrows, boundaries, and captions are legible, and neither figure is cropped or distorted.
- All paper and response fonts are embedded Type 1 fonts. Both PDFs are 612 x 792 pt US Letter, unencrypted, and contain no forms or JavaScript.
- No undefined citation/reference, missing file, overfull box, or compilation error remains. Three nonfatal underfull-box warnings do not create visible gaps, clipping, or margin violations.
- Every page of the 7-page paper and 2-page response was rendered and visually inspected. Tables remain within the two-column grid; captions stay with their figures; no text overlaps the artwork.

## Reviewer-response audit

- The response quotes each reviewer concern and identifies the corresponding manuscript change.
- It explains the four-to-two figure consolidation, states that the final files are vector redraws, and maps each revised figure to Sections III-C and III-D.
- It preserves the paper's architectural novelty claim and does not portray the standardized PQC primitives as new algorithms.
- It acknowledges the remaining absence of a matched physical-board or accelerator baseline. The response does not claim this limitation was experimentally resolved; the paper bounds the QEMU evidence and lists the missing board-level work explicitly.

## Scores

| Criterion | Score | Basis |
|---|---:|---|
| Content fidelity to DOCX V4.0 | 9.4/10 | 95.87% V4.0 token retention; title, authors, tables, values, conclusions, and reference order retained. |
| Core fidelity to submitted PDF V2.1 | 9.3/10 | Same scope and tiered placement argument; V4.0 adds substantial detail but does not replace the study. |
| IEEE paper formatting | 9.7/10 | Official conference class, US Letter, two columns, 7/8 pages, embedded fonts, clean margins. |
| Technical and argumentative discipline | 9.3/10 | Trust-boundary and interface wording corrected; claims remain bounded to QEMU evidence. |
| Figure readiness against reviewer concern | 9.6/10 | Two sharp vector schematics, no embedded raster, full-page visual QA completed. |
| Author Response readiness | 9.5/10 | Complete, specific, and honest about the unresolved experimental baseline. |

**Overall camera-ready readiness: 9.4/10.** The two local PDFs are complete and internally consistent. The remaining external gate is IEEE PDF eXpress and the conference submission-system metadata check. The scientific limitation that remains is the lack of a matched physical-board/accelerator baseline; resolving it would require new experiments rather than editorial revision.
