# School website

The website for Dan's parents' toddler and preschool center in Koreatown, Los Angeles. Plain HTML and CSS, with JavaScript only where it helps. This repository is private. Cloudflare publishes the `site/` folder after each merge to main.

## Start here

- At the start of a session, read `PROGRESS.md` (where things stand, the next step) and `DECISIONS.md` (each choice and its reason). Read only the parts the task needs.
- The checked facts and their sources are on Dan's Notion page "Parents' preschool website (Oct 2026)," under Master Notes.

## Working with Dan

### Who you're working with

- Daniel Yoon (writes as "Dan"): a writer and pastor in Southern California, Korean American, new to coding. He builds small projects with AI and makes the design decisions: what to build, what to leave out, and why.
- He learns by doing: explain every change in plain words, one small change per pull request, and give him a check he can do himself before merging.
- How he likes instructions:
  - Numbered steps, with the full link inside each step (never "the link above") and the exact button or tab to click.
  - Every answer stands on its own: repeat every step, link, name and value in full each time. Never "see above" or "as before."
  - Ask one question at a time, with options and a recommendation.
  - Accuracy matters most. Check facts against official sources before stating them, say clearly when something couldn't be checked, and never guess.
  - Start feedback with what works, then up to three ranked problems, each with a fix.
  - End each reply with one concrete next action.
- He wants as little friction as possible: Claude does the follow-up work on its own, and he doesn't want to be the messenger.
- He tests on his phone (Android, Chrome, sometimes inside the KakaoTalk in-app browser) and sends screenshots. His phone uses the three buttons at the bottom (|||, ○, <), not swipe gestures, so test steps say "tap <" for Back. Show screenshots before every pull request.
- His design rules: keep pages short on a phone (tabs, fold-outs, one level per screen); no long lists.
- He keeps notes in Notion (Master Notes, one page per topic). Save important decisions and checked facts there, in one write per finished piece of work.

### How the work flows

1. Claude works on its branch and restarts it from `main` after each merge: `git fetch origin main && git checkout -B <branch> FETCH_HEAD`.
2. Claude opens a pull request with a plain-words description and a "How to check it" list. Right after opening it, Claude subscribes to the pull request's activity (`subscribe_pr_activity`), so the merge wakes the session, and sets one backup check-in about 50 minutes later (`send_later`), cancelled when the merge arrives.
3. Cloudflare comments on each pull request with a preview link, so Dan can open the change on his phone before merging.
4. Dan reviews and merges on GitHub (Conversation tab, Merge pull request, Confirm merge).
5. Cloudflare publishes `site/` (Workers Builds: Cloudflare runs its deploy tool, Wrangler, on its own computers; nothing runs on Dan's computer). Its check, "Workers Builds: school-website," shows next to the merge.
6. When the merge wakes the session, Claude checks that the publish worked, restarts the branch from main, updates the Notion page, then tells Dan in one short message.

Only one pull request at a time.

## Rules for this site

- Only facts Dan's parents have confirmed go on the site. Never fill a gap with a guess: write [needs your parents' answer] instead.
- The center's California license number goes on every page: 22 CCR § 101162 requires it in all advertisements (checked through search results, October 31, 2026).
- No made-up or undisclosed insider reviews (the FTC's rule, 16 CFR Part 465). Real parent quotes only, with their permission.
- No children's faces on the public site, and no children's names anywhere. Remove location data from photos before they're added (converting to WebP doesn't remove it).
- Accessibility: well-built pages (real headings, labels, alt text, strong contrast, usable with a keyboard). Never an accessibility widget or "overlay."
- Every page must look good on a phone first (360 pixels wide), then on a computer.
- No build tools: no npm, no frameworks, no generators. The one exception: Cloudflare runs Wrangler on its own computers to publish. The code stays plain files, simple and commented, so Dan can edit them.
- Keep every page hidden from search engines (`<meta name="robots" content="noindex">`) until launch.

## Privacy

- Never show or mention Dan's own kids, in text, images or file names.
- Keep this site separate from Dan's personal site and writing: don't link it from danielyoonwrites.github.io, and don't mention this project in that repository (it's public).
