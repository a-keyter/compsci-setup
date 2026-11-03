# AI Essentials for CompSci: setup guide

Pre-session setup guide for the CompSoc x Generative Minds workshop (Wed 4 Nov 2026, Gilmour Room, Guild of Students).

Same pattern as `lcc.genminds.co.uk`: one self-contained `index.html` (inline CSS and JS, no build step) plus `vercel.json`.

## What's in it

Eight pages with a contents sidebar, Back/Next bar and arrow-key navigation:

1. Welcome: event details and a Mac or Windows choice (only that laptop's steps are shown afterwards)
2. What you're setting up
3. Part 1: Install the tools (Mac: Homebrew, `brew install opencode node gh`. Windows: WSL, OpenCode 2, nvm, GitHub CLI)
4. Part 2: GitHub and Vercel accounts, Git identity, `gh auth login`
5. Part 3: Create the `my-portfolio` Next.js project and check free models
6. Ready for Wednesday? One-line check command plus a checklist
7. If something goes wrong
8. After the session: Boot.dev Learn AI Coding

Every step has a Done tick and every command has a Copy button. Ticks, the laptop choice, the theme and the last page are saved in the visitor's browser only (localStorage prefix `gm-compsci-v1-`). No backend, analytics or personal data.

## Deploy

```bash
cd opencode-setup
git init && git add -A && git commit -m "AI Essentials setup guide"
gh repo create compsci-setup --private --source=. --push
```

Then import the repo at https://vercel.com/new (framework: Other, no build command) and add a subdomain such as `compsoc.genminds.co.uk` under Project > Settings > Domains.

## Editing

Edit `index.html` directly. To show steps for one laptop only, wrap content in an element with `data-os="mac"` or `data-os="win"`.
