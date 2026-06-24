# NovaCare Medical Service Parts — Answer-Trained, Audited RAG Tutor

Open `novacare_rag_class_personas_answer_trained_audited.html` locally in a browser.

This version improves the NovaCare inventory-aggregation RAG tutor and the four persona answer styles: Tutor, Inventory Analyst, CFO Reviewer, and Operations Manager. It preserves the local-only classroom design: no remote API calls, no CDN, no analytics, no `fetch()`, and no `XMLHttpRequest()`.

## What changed

- Generated 18,240 persona-aware student Q&A examples for the local answer-training bank.
- Every generated training question now has a student-facing `answerTrainingText`.
- The live tutor retrieves against generated question text, generated answer text, embedded case concepts, symbol definitions, and live scenario calculations.
- Persona answers are more interpretive and managerial rather than short formula templates.
- The tutor gives direct definitions for symbols and notation, including units and current-scenario values when relevant.
- Symbol routing now distinguishes short symbols and English words that can otherwise collide: `μ` versus the verb “mean,” `z` versus capital `Z`, `H` versus `h`, `SS` versus `SS → NDC`, and `λ_min` versus the newsvendor shadow-price λ.
- The app correctly treats `λ_min` in NovaCare as the minimum eigenvalue used to audit correlation-matrix validity, not as the newsvendor capacity shadow price.
- Added audit files for common live-session symbol and intent questions.
- Kept the separate synchronized information windows: full case brief, data, formulas, CV views, cost dashboard, network diagram, correlation matrix, sensitivity analysis, symbol glossary, training-bank review, and printable learning sheet.

## Important note about external LLMs

The classroom app intentionally does not send uploaded course material or student questions to any external service. The execution sandbox used to create this package cannot call a separate external LLM API. The included prompt pack, `novacare_external_llm_answer_prompt_pack_final.md`, is provided so you can run an institution-approved external-LLM audit or regeneration pass outside this sandbox if desired. The delivered app itself is answer-trained locally and browser-only.

## Included files

- `novacare_rag_class_personas_answer_trained_audited.html` — standalone local app.
- `novacare_tutor_training_corpus_answer_trained_audited.json` — generated Q&A answer-training corpus.
- `novacare_tutor_training_corpus_answer_trained_audited.csv` — generated Q&A answer-training corpus for review.
- `novacare_tutor_answer_audit.csv` — symbol/intent audit checklist.
- `novacare_rag_answer_symbol_audit.csv` — symbol-routing audit with expected versus actual primary matches.
- `novacare_training_answer_collision_audit.csv` — answer-corpus collision audit for symbols that previously risked misrouting.
- `novacare_external_llm_answer_prompt_pack_final.md` — external LLM prompt pack for independent answer audit or regeneration.

## Classroom use

Use the tutor/persona window as the main workspace. Students can open supporting charts and tables only when they need them. Open windows remain synchronized as students change CSL, review interval, lead time, stocking choices, and regional correlations. At the end, students can open the printable learning sheet and use the browser print dialog to save it as a PDF.
