# David Salazar portfolio: notes for Claude Code

New portfolio site for davesal.me, built from scratch to replace the old one (its source is the private repo `davesal0710/davesal.me`; do not copy its look). Read `PORTFOLIO_HANDOFF.md` and `PORTFOLIO_CASE_STUDY_TETSU.md` first. They are the source of truth for facts, positioning and guardrails. If a fact is not in them or the resume, ask David; never invent metrics, clients or outcomes.

## Goal and audience

Get interviews for Business Analyst and Project/Program Manager roles (David is an FDM consultant, open to other roles and to leaving). Readers are hiring managers with about 60 seconds. Tetsu is the centerpiece case study. Position David as an analyst who turns messy operational problems into clear requirements and working prototypes, with AI in the workflow and a human reviewing.

## Rules for content

- Use only claims in the handoff's evidence bank. Respect its "do not claim" list (no Tetsu user numbers, the Amazon pilot did not run, no hand-written-code claims).
- Tetsu: say openly that David owned the product and AI assistants wrote the code under his direction.
- SQL is not claimed until David says he has finished it. Power BI and SAFe are claimable.
- Link the live Tetsu demo (https://tetsugym.ai.studio). Never link the Tetsu source; that repo is private.
- Do not commit `PORTFOLIO_HANDOFF.md` to this public repo. Keep it out of the deployed files.

## Design workflow

- Before any UI code, get the design brief from David: reference sites he likes, adjectives wanted and unwanted, and a "no" list. Do not start from a default aesthetic.
- Use the installed skills: `frontend-design`, `taste-skill`, and Impeccable (run `npx impeccable install` once in the repo, then `/impeccable init`). Read any new third-party skill's `SKILL.md` before installing it.
- Optional skills, both wanted for this project (install in the new repo, reading each `SKILL.md` first): Emil Kowalski's design-engineering skills (`emilkowalski/skills`, MIT) for motion and polish, and Vercel's `web-design-guidelines` (in `vercel-labs/agent-skills`) for an accessibility and UI-guideline pass before launch. Install with `npx skills add <repo-url>` (Vercel's: add `--skill web-design-guidelines`).
- Avoid the old site's look and common AI defaults: grain overlays, gradient blobs, generic card grids, lime-on-black, stock hero copy.
- Must work on phones, be fast and accessible, and read well in under a minute. Verify in a real browser at phone and desktop widths, not only by reading the code.

## Hosting and workflow

- Public repo, deployed to GitHub Pages with the custom domain davesal.me (needs a `CNAME` file). One deploy source only; the old site drifted because it deployed from two places.
- Making a repo private unpublishes Pages, so keep this one public.
- One branch and one pull request per change. Commits and PRs use the `davesal0710` GitHub account (`git config user.name` and `user.email` in the repo).
- Read a file before editing it; keep existing line endings (Windows files may use CRLF).
