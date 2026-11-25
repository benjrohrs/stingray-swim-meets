# stingray-swim-meets

Public website for the Stingray Swim Meets iOS app: three static pages (`index.html`, `privacy.html`, `support.html`) served by GitHub Pages from `main` at `https://benjrohrs.github.io/stingray-swim-meets/`. The App Store listing links to the privacy and support pages, so these URLs must keep working. This file is public, like the rest of the repo.

## Git

- Every change goes on its own branch and through a PR. Never push to `main`.
- Merge with `gh pr merge --squash --delete-branch`; no review is needed. There is no CI and no required check. `main` currently has no branch protection, so nothing stops a direct push; follow the rule anyway.
- Merging publishes: GitHub Pages rebuilds from `main` and the change is live within a few minutes.
- Commands given to Ben go on one line, with no `\` continuations.

## Checks before merging

- No build step. Open the changed pages in a browser and check the links between them (`./`, `privacy.html`, `support.html`) still resolve.
- Don't rename or move `privacy.html` or `support.html`: the App Store listing points at them.
- The pages are copies of files kept in the app's own (private) repo. A change made here also has to be made there, and the other way round; say so in the PR description.

## What a cloud session can't do

- Change the App Store listing or its URLs: that's Ben's, in App Store Connect.
- Read the app's design and metadata docs, which are not in this repo. When a cloud session makes a decision worth recording, put it in the PR description so a Mac session can copy it into the docs.
- A change to the privacy policy's substance (what data is collected or where it goes) needs Ben's OK before merging.
- Never print secret values; check them by length or prefix only.
