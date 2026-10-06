# Resume repository

## Purpose

This repository is the main workspace for editing and maintaining my personal
resume. The resume will be authored in LaTeX, with the `.tex` source as the source
of truth and a PDF as the generated output.

## Current content

- `resume.tex` is the main LaTeX source. Make resume edits there.
- `resume.pdf` is the generated, single-page resume.
- `Resume-2026-docx.md` is the original content export. Keep it unchanged as a
  reference, not a second maintained version.
- The initial LaTeX conversion must preserve the export's wording. Match the
  supplied visual reference through formatting, not by shortening the content.

## Editing guidelines

- Preserve factual accuracy. Do not invent achievements, metrics, dates, roles,
  qualifications, or contact details. Ask when information is missing or unclear.
- Use clear, concise language. Improve wording without changing the meaning or
  overstating the work.
- Keep changes focused on the requested content or layout. Do not remove content
  or make substantial layout changes without direction.
- Keep resume content in the LaTeX source. Do not edit generated PDFs directly.
- Use 10-point Arial body text, equal 0.65-inch side margins, and no more than
  two bullet levels. Experience headings have no bullets, with dates aligned
  to the right.
- Do not upload resume files or personal information to external services without
  explicit permission.

## Build the PDF

- Use Tectonic to compile locally. The persistent compiler location on this
  machine is `~/.local/bin/tectonic`, outside the repository and session folders.
  It does not require a Homebrew installation.
- After saving changes to `resume.tex`, run this command from the repository
  root to generate the PDF:

  ```sh
  "$HOME/.local/bin/tectonic" --keep-logs resume.tex
  ```

- A successful build creates or replaces `resume.pdf` and writes `resume.log`
  in the repository root.
  Tectonic can download required TeX packages on the first build; compilation
  runs locally.
- The source uses the installed Arial font and a US Letter page.

## LaTeX checks

- After LaTeX changes, compile the resume and inspect the PDF for clipped text,
  overflow, spacing, broken links, and unexpected page breaks.
- Confirm that the PDF has exactly one page and that the exported content is
  preserved.
- Report build errors or missing tools. Do not claim to have checked a PDF that
  was not generated and inspected.
