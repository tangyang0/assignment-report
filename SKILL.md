---
name: assignment-report
description: Create or edit course homework and assignment reports with a Markdown/LaTeX source, a clean PDF submission, and visual layout checks. Use for Chinese or bilingual academic assignments that need readable formulas, structured original-question/answer sections, and compact, non-template-like typography.
---

# Assignment Reports

Use this skill when the user asks to complete, revise, or format a course assignment, homework, lab report, or similar submission artifact. Do not apply it to ordinary explanations or unrelated reports.

## Preferred deliverables

- Keep an editable `.md` source as the primary authoring file.
- Write mathematics directly in Markdown LaTeX (`$...$` and `$$...$$`); do not turn formulas into images in the Markdown source.
- Produce a PDF submission when the user needs a fixed, printable artifact. Use images only for actual figures or diagrams. If cross-reader font substitution causes overlap, rasterize the visually checked pages into the final PDF.
- Do not create a Word file unless the user asks for Word specifically.

## Content structure

For multiple questions, preserve the exact prompt or a faithful transcription first, then place the answer beneath it:

1. Question title
2. **原题**
3. The supplied question text
4. **解答**
5. The solution or report

Keep the requested content and evidence. Avoid inventing a cover subtitle, a separate “说明” section, a generic “参考资料” section, or a date line unless the user or course requires it. If references are needed for correctness, place them briefly at the end without ornamental framing.

## Compact academic layout

- Start the first question on page one after the title and personal information; do not force a cover page unless requested.
- Use bold for the title, question headings, section headings, “原题/解答” labels, and table headers.
- Keep headings with the paragraph that follows; never leave a heading alone at the bottom of a page.
- Let content flow naturally. Avoid manual page breaks between questions or subsections unless a figure or a major section genuinely requires one.
- Add moderate blank space between questions, headings, paragraphs, figures, and equations. Avoid dense walls of text and large empty cover pages.
- Use ordinary paragraph text and clear numbered sections. Keep the prose direct and concise so the artifact does not read like a generic AI template.

## Chinese typography and contrast

- For Chinese PDF output, use Songti/Songti SC regular for body text and a real bold Songti face for headings.
- Use Kaiti/Kaiti SC for personal information when requested by the user.
- Use a math font with textbook-like forms for displayed equations, such as STIX; keep displayed equations only modestly larger than body text.
- Avoid unsupported Unicode subscripts, superscripts, norm glyphs, or Greek letters in ordinary body paragraphs. Put complex notation in LaTeX display equations instead.
- Before delivery, scan the rendered/source text for unrendered linear math left in prose, such as `r^p`, `R_i`, `D=min(...)`, or literal `1/2` when a displayed equation is intended. Rewrite the prose or move the expression into Markdown LaTeX and a rendered PDF equation. Do not count LaTeX delimiters in the Markdown source itself as a defect.
- Tables should use a light gray or light blue fill with black text, visible light borders, and alternating pale rows. Avoid dark backgrounds with low-contrast text.
- For mixed Chinese/Latin paragraphs, use a CJK-aware line-breaking/justification strategy so English words, numbers, and formulas are not stretched apart.

## Verification before delivery

Render the final PDF and inspect every page at readable resolution. Check:

- no overlapping or clipped text;
- no missing Chinese glyphs or font substitution boxes;
- headings are not stranded at page bottoms;
- question boundaries and blank spacing are clear;
- formulas have readable superscripts, subscripts, and symbols;
- tables have sufficient contrast and do not split awkwardly;
- figures and captions are aligned and readable;
- personal information is correct.
- Formula QA includes both a visual check and a lightweight text scan of the source or extracted PDF text for stray caret/underscore notation. If the final PDF is rasterized, perform the scan before rasterization because an image-only PDF has no searchable text layer.
- For multi-round model tests, label each finding by source: model-generated output, external program/visual measurement, assistant analysis, or user feedback. Do not present a later human correction as an independent model call.

If the source is Markdown, verify that all display formulas remain valid LaTeX and that linked figures exist beside the source file.
