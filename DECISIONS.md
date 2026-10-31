# Decisions

Each decision with its reason, oldest first. Only add to this file; if a decision changes, add a new entry that says which one it replaces.

### October 31, 2026: its own private repository, published by Cloudflare
- Decision: the site lives in this private repository (`danielyoonwrites/school-website`), and Cloudflare publishes it (Workers Builds, static files only). Its own web address comes later, in Dan's parents' name. Dan's choice: "A."
- Why (Claude's reasons, which Dan chose from): it keeps the family business separate from Dan's public GitHub and writing; Cloudflare already publishes Living in the Word's server for him; static files on Cloudflare are free and unlimited (Cloudflare's docs, read October 31, 2026); each pull request can get a preview link to open on his phone before merging.
- How: Cloudflare runs its deploy tool, Wrangler, on its own computers, the same exception Dan chose for Living in the Word's server on October 29, 2026. Nothing runs on Dan's computer, and the code stays plain files.
- Turned down: a public repository on GitHub Pages (GitHub Pages is free only for public repositories, so the files and draft photos would be public under his name); a folder in the website's repository (public, under his personal site's address, and moving it later breaks links).
- Unverified when chosen: that Cloudflare publishes from a private repository (a community post said so). The first publish after pull request 1 confirms it.
