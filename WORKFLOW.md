# Branching and Conflict Notes

The lab uses separate branches for the navigation bar, footer, hero section, contact form, and testimonials. The footer and header branches both make changes to the same copyright line in `index.html`:

- `feature/footer` changes the copyright year from 2025 to 2024.
- `feature/header` adds a short line below the heading and changes the copyright year to 2026.

Merge `feature/footer` into `main` first, then merge `feature/header`. Git cannot choose between the two year edits, so the second merge needs a manual resolution. Keep the new header line and one final copyright line, remove the conflict markers, then stage and commit the resolved file.

The other feature branches add a home-link state to the navigation, a background to the hero section, contact-form guidance, and one more placeholder testimonial. Each branch is merged into `main` after its change is committed.

Use `git status` before and after the resolution. `git log --oneline --graph --all` shows the branch history.

Resolution used: keep the tagline from `feature/header` and retain the original 2025 copyright year. This preserves the header improvement while leaving one clean footer line.
