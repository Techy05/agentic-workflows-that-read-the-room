---
name: update-github-info
description: Draft GitHub Info website updates for Mona using official GitHub sources and open a pull request for review.
on:
  workflow_dispatch:
  schedule:
    - cron: '17 9 * * *'
safe-outputs:
  create-pull-request:
    title-prefix: "[mona] "
    draft: true
    fallback-as-issue: false

tools:
  edit:
  web-fetch:

network:
  allowed:
    - github
---

# Update Mona's GitHub Info website

Read notes/mona-notes.md before drafting any changes.

Use these sources:
- notes/mona-notes.md
- GitHub Blog: https://github.blog/latest/
- GitHub Changelog: https://github.blog/changelog/

Update site/content/github-info.md with concise, practical updates for readers.
When the content comes from the GitHub Blog or GitHub Changelog, mention that source clearly.

Open a pull request for Mona to review. Do not write directly to main; rely on safe-outputs with create-pull-request.
