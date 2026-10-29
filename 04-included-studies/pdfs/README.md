# Included Studies — PDF Storage

Storage for full-text PDFs of included studies. Naming convention:

```
S###-citation_key.pdf
```

For example:
- `S001-fowler2024experience.pdf`
- `S002-brennan2025multicase.pdf`

## .gitignore note

If publisher licensing forbids redistribution of PDFs, add this to .gitignore:

```
04-included-studies/pdfs/*.pdf
```

DOIs are recorded in `../included-studies-list.xlsx` so collaborators can
retrieve papers through their own institutional access.
