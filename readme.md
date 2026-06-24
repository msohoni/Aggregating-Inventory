# NovaCare Local RAG Tutor — Case-Brief Preamble Version

Open `novacare_rag_class_personas_case_brief.html` in a browser.

This version builds on the live-window NovaCare RAG tutor and adds a separate **Full case brief** preamble window. The main page still keeps the tutor as the primary workspace and shows the case questions first, while the separate preamble window provides the complete case narrative, decision rules, input data, current scenario snapshot, and expected student deliverable.

## What changed

- Added an **Open full case brief** button directly in the preamble.
- Added **Full case brief** to the information-window control panel.
- The full case window includes:
  - company and service-parts setting,
  - current RDC network and proposed Indianapolis NDC,
  - student decision alternatives: RDC, NDC, and SS → NDC,
  - rule that RDC-to-RDC movement is not allowed,
  - condition for earning RDC fixed-footprint savings,
  - part-family data,
  - regional transportation and network-cost data,
  - demand table with μ, σ, CV, and annual demand,
  - current scenario snapshot, including CSL, z, T, L, correlation-matrix status, current cost, NDC flow, and active RDCs,
  - expected recommendation deliverable.
- The case-brief window auto-refreshes when students change CSL, review interval, lead time, stocking choices, or regional correlations.

## Classroom use

1. Open the HTML file locally in a browser.
2. Ask students to begin with the preamble and the five case questions.
3. Use **Open full case brief** when students need the complete case statement and data in a separate window.
4. Keep the RAG tutor as the main workspace.
5. Use the other separate windows only when students want specific evidence: data, formulas, CV charts, cost dashboard, network diagram, correlation matrix, sensitivity, or symbol glossary.
6. At the end, open **Print learning PDF sheet** and use the browser print dialog to save the summary as a PDF.

No remote API, CDN, analytics, `fetch`, or `XMLHttpRequest` calls are used.
