# Progress

Last updated October 31, 2026.

## Where it stands

- October 31, 2026: Dan chose a private repository published by Cloudflare (see `DECISIONS.md`) and made this repository. Pull request 1 adds a test page ("coming soon," in English and Korean), Cloudflare's settings file (`wrangler.jsonc`) and these notes.
- Next: Dan merges pull request 1, then connects Cloudflare to this repository. The test page then shows at the workers.dev address, which also confirms that Cloudflare publishes from a private repository (Claude couldn't find that in Cloudflare's docs).

## The plan (Claude's suggestion, not decided)

1. A short fact sheet for Dan's parents: about 10 questions, in Korean and English.
2. Version 1: one short page, phone first: ages, hours, where, how to reach the center, the license number, with Call, Text and Directions buttons.
3. Then one pull request at a time: photos without children's faces, a day at the school, the programs, more languages if someone at the center can answer in them, a tour request.
4. At launch: the web address, in Dan's parents' name; turn off the workers.dev address (it shows the Cloudflare account's name); remove the noindex line; check the center's Google Maps listing.

## Open questions

- Which languages (only ones someone at the center can answer the phone in).
- The center's license type, and whether it's licensed for toddlers.
- Who updates the site. Claude's assumption: Dan, with Claude, from changes his parents send him.
- The look (colors and type). The test page uses a plain, temporary look.

## Where things are

- `site/`: the website's files. Everything in this folder goes on the site.
- `wrangler.jsonc`: Cloudflare's settings. Its `name` must match the Worker's name in Cloudflare.
