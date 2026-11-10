# Branching and Conflict Notes

The lab uses two branches that make changes to the same `index.html` file:

- `feature/footer` changes the copyright year from 2025 to 2024.
- `feature/header` adds a short line below the heading and changes the copyright year to 2026.

Merge `feature/footer` into `main` first, then merge `feature/header`. Git cannot choose between the two year edits, so the second merge needs a manual resolution. Keep the new header line and one final copyright line, remove the conflict markers, then stage and commit the resolved file.

Use `git status` before and after the resolution. `git log --oneline --graph --all` shows the branch history.

Resolution used: keep the tagline from `feature/header` and retain the original 2025 copyright year. This preserves the header improvement while leaving one clean footer line.
