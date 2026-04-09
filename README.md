# RepoScoper

**GitHub through a recruiter's lens.**

RepoScoper is a free, open-source GitHub developer search tool built for recruiters. It uses GitHub's public search syntax but presents results the way a recruiter reads them — profile summary, location, primary language, public activity, and contact signals in one clean view — rather than the way a developer navigates them.

The primary skill filter lets you narrow by language or technology before running a search. Email reveal surfaces publicly listed contact details where available. A saved candidates drawer lets you shortlist profiles across a session without losing your place.

Part of the [Sourcer.club](https://sourcer.club) suite — free tools for serious sourcers.

---

## Using the tool

RepoScoper is a single HTML file with no dependencies, no backend, and no build step.

**Online:** [repo.sourcer.club](https://repo.sourcer.club)

**Offline / self-hosted:**
1. Download `index.html`
2. Open it in any modern browser
3. No server required

**GitHub API token (optional but recommended):**
Without a token, GitHub's API allows 10 requests per hour. With a free personal access token it increases to 5,000 per hour. Use the token bar inside the tool to add yours. Generate one at [github.com/settings/tokens](https://github.com/settings/tokens) — no scopes required for public data.

---

## Features

- Boolean-compatible text search using GitHub's full user search syntax
- Primary skill filter — narrow by language or technology before searching
- Recruiter-readable result cards — name, location, bio, language, activity signals
- Email reveal — surfaces publicly listed email addresses
- Saved candidates drawer — shortlist profiles within a session
- Light and dark mode
- No login, no tracking, no data sent anywhere except directly to the GitHub API

---

## Responsible use

RepoScoper accesses publicly available data via the official GitHub API. By using this tool you agree to:

- Use it solely for legitimate recruiting outreach
- Comply with [GitHub's Terms of Service](https://docs.github.com/en/site-policy/github-terms/github-terms-of-service)
- Not use it for spam, bulk email campaigns, data harvesting, or any purpose that violates applicable privacy laws including GDPR and CAN-SPAM

All data returned is publicly visible on GitHub profiles. Sourcer.club is not responsible for misuse of this tool.

---

## License

MIT License

Copyright (c) 2026 Sourcer.club

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

---

## Acknowledgements

- Data source: [GitHub REST API](https://docs.github.com/en/rest) — all data accessed is public and retrieved in accordance with GitHub's Terms of Service
- Fonts: [Syne](https://fonts.google.com/specimen/Syne) and [JetBrains Mono](https://fonts.google.com/specimen/JetBrains+Mono) via Google Fonts (SIL Open Font License)
- Built with vanilla HTML, CSS, and JavaScript — no frameworks
