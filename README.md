# Resume LaTeX Workspace

This workspace keeps `resume_swe.tex` as the main resume and uses the same layout for future resume variants.

## Structure

- `resume_swe/resume_swe.tex`: main software resume source
- `resume_swe/resume_swe.pdf`: compiled main software resume
- `resume_swe/resume_template.tex`: reusable template for future resumes
- `resume_swe/.build/`: generated LaTeX build artifacts
- `resume_swe/.latexmkrc`: LaTeX build configuration

Only the `.tex` source files and final `.pdf` files should stay visible in the main resume folder. Intermediate files are redirected to `.build/`.

## Build

From `/Users/jameshoang/Desktop/sfu/resume_latex/resume_swe`:

```bash
latexmk -pdf resume_swe.tex
latexmk -pdf resume_template.tex
```

## Create a New Resume From the Template

1. Copy the template:

```bash
cp resume_template.tex resume_new_role.tex
```

2. Replace the placeholder values:
- `[YOUR NAME]`
- `[PHONE NUMBER]`
- `[EMAIL ADDRESS]`
- `[LINKEDIN URL]`
- `[GITHUB URL]`
- `[PERSONAL WEBSITE]`
- `[SCHOOL NAME]`
- `[DEGREE OR PROGRAM]`
- `[COMPANY NAME]`
- `[PROJECT NAME]`
- `[SKILL GROUP]`

3. Build the new version:

```bash
latexmk -pdf resume_new_role.tex
```

The compiled file will appear as `resume_new_role.pdf` in the same folder.

## Notes

- Keep `resume_swe.tex` as the source of truth for your current main resume.
- Use `resume_template.tex` only as a starting point for new resume variants.
- Generated files such as `.aux`, `.log`, `.fls`, and `.fdb_latexmk` should remain inside `.build/`.
