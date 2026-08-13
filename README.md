# research

An unlisted personal archive of research write-ups — the kind of thing that used to
live as one-off Claude Artifacts. Plain static HTML, no build step, no Jekyll
(`.nojekyll` keeps GitHub Pages from touching it). Not linked from
[todhilton.com](https://todhilton.com) and blocked from search indexing via
`robots.txt` and per-page `noindex` — unlisted, not access-controlled.

Published at [todhilton.com/research](https://todhilton.com/research/).

## Adding a new research note

1. Fetch the Claude Artifact and strip the claude.ai iframe/frame-runtime wrapper,
   keeping the raw `<title>`, inline `<style>`, and body content.
2. Save it as `<slug>/index.html` in this repo.
3. Add a back-link to the landing page inside the new page itself, right after the
   opening `<div class="shell">` (or equivalent top-level wrapper):
   `<a class="back-link" href="/research/">&larr; Research</a>` — see
   `leaving-lightroom/index.html` for the accompanying `.back-link` CSS to copy in.
4. Add `<meta name="robots" content="noindex, nofollow">` to its `<head>`.
5. Add one entry to the list in the root `index.html`, linking to `/research/<slug>/`
   (paths must be prefixed with `/research/` — this is a project page under
   todhilton.com, not its own host, so a bare `/<slug>/` resolves to the domain root).
6. Commit and push.
