# SourcerBot 🔍

**A free, open source GitHub developer search tool built for recruiters and talent sourcers.**

SourcerBot helps you find developers on GitHub using the full power of GitHub's search syntax — with a clean recruiter-focused UI on top. No backend. No database. No installation. Just open the file in your browser and start searching.

Built by [Sourcer.club](https://sourcer.club) — a growing community of talent sourcers.

---

## What It Does

- **Search GitHub developers** using GitHub's native search syntax — location, language, keywords, followers, repos and more
- **View enriched profiles** — bio, followers, repos, location, company, website, Twitter, join year
- **Primary skill filter** — intelligently filters developers where the searched language appears in their top 3 languages (accounts for supporting languages like JavaScript alongside Ruby)
- **Click-to-reveal email** — shows public emails on demand, never exposed in the page source
- **Save candidates** — shortlist developers during your session with a slide-out saved panel
- **Light and dark mode** — defaults to light, toggle anytime
- **Zero cost** — uses your own free GitHub token, 5,000 API requests per hour

---

## Getting Started

### Step 1 — Download the file

Download `sourcerbot.html` from this repository and open it in any browser (Chrome, Edge, Firefox, Safari). No installation needed.

### Step 2 — Generate a free GitHub token

1. Go to [github.com/settings/tokens/new](https://github.com/settings/tokens/new)
2. Give it a name — e.g. `SourcerBot`
3. Set expiration — 90 days or no expiration
4. Under **Scopes**, check only `read:user`
5. Click **Generate token**
6. Copy the token immediately — GitHub won't show it again

### Step 3 — Add your token to SourcerBot

1. Open `sourcerbot.html` in your browser
2. Paste your token in the token bar at the top
3. Click **Verify & Save**
4. You should see a green confirmation — you're ready to search

---

## How to Search

SourcerBot uses GitHub's search syntax directly. Type your query in the search box and hit Search.

### Basic examples

```
location:Chennai language:Python
location:Bangalore language:Java
location:India language:Go followers:>=100
```

### Using OR for multiple keywords

```
location:Bangalore spring OR microservices language:Java
location:Chennai kafka OR airflow language:Python
```

> ⚠️ Use OR **without brackets**. Brackets break GitHub's user search and return 0 results.
> GitHub supports up to **5 OR operators** per query — SourcerBot warns you if you exceed this.

### Combining filters

The **Min Followers**, **Min Repos**, **Sort By**, **Order**, and **Per Page** fields below the search box are applied automatically on top of your query. You don't need to type `followers:>=50` manually — just set the Min Followers field to `50`.

### Full GitHub search syntax

For advanced queries, refer to [GitHub's official user search documentation](https://docs.github.com/en/search-github/searching-on-github/searching-users).

---

## Primary Skill Filter

Toggle the **Primary skill filter** to show only developers where the searched language appears in their **top 3 languages** by repo count.

This is smarter than checking just the #1 language — a Ruby developer will naturally have JavaScript repos (frontend), Shell scripts (deployment), and Ruby repos (backend). The filter recognises this and correctly includes them.

**How it works:**
- Fetches each developer's public repos (up to 100)
- Counts language distribution, excluding forked repos
- Checks if searched language appears in top 3
- Hides non-matching developers, shows final count once analysis is complete

> ⚠️ The primary skill filter uses 1 extra API call per developer. With 20 results per page, that's 20 additional calls per search.

---

## API Usage

| Action | API calls |
|---|---|
| 1 search (20 results) | 1 call |
| Enriching 20 profiles | 20 calls |
| Primary skill filter (20 devs) | 20 calls |
| **Total per page (filter OFF)** | **~21 calls** |
| **Total per page (filter ON)** | **~41 calls** |

With a free GitHub token you get **5,000 calls/hour** — enough for roughly **120 standard searches** or **60 filtered searches** per hour.

---

## Important Notes

### Data & Privacy
- SourcerBot only accesses **publicly available** GitHub profile data via GitHub's official API
- Your GitHub token is stored in your **browser's localStorage only** — it never leaves your device
- Saved candidates exist only for the duration of your browser session — refreshing the page clears them
- Email addresses shown are only those developers have chosen to make **publicly visible** on their GitHub profile

### Responsible Use
SourcerBot is built for **direct, relevant recruiting outreach** — reaching out to developers about genuine opportunities that match their skills and interests. Please use it responsibly and in accordance with [GitHub's Terms of Service](https://docs.github.com/en/site-policy/github-terms/github-terms-of-service).

### Limitations
- GitHub's user search searches **bio text, name, username, and location** — not repo content or commit history
- The primary skill filter is based on **public repo count** — it's a strong signal but not a perfect measure of skill depth
- GitHub caps search results at **1,000 per query** (20 pages × 50, or 50 pages × 20)
- The primary skill filter applies **page by page** — not across all results at once

---

## Tips for Recruiters

- **Start broad, then filter** — search `location:India language:Python` first, then enable the primary skill filter to narrow down
- **Use the saved panel** — shortlist candidates as you browse, act on them before ending your session
- **Click 🌐 Website** on cards — many developers list their portfolio or resume there
- **Click ✉ View Email** — reveals public email on demand for direct outreach
- **Click the SourcerBot logo** — resets the search and all filters instantly

---

## We'd Love Your Feedback

SourcerBot is in early access and we're actively improving it. We'd love to hear:

- Your overall experience using the tool
- Any bugs or unexpected behaviour you encounter
- Search scenarios where results felt off or incomplete
- Features you wish it had
- Anything that felt confusing or clunky in the UI

Please share your feedback by [opening an issue](https://github.com/johnrambo-r/sourcerbot/issues) on this repo or joining the conversation at [Sourcer.club](https://sourcer.club).

---

## Roadmap

- [ ] OAuth login — sign in with GitHub instead of manual token entry
- [ ] Sourcer.club community forum
- [ ] More recruiter tools at sourcer.club

---

*Built with ❤️ by [Sourcer.club](https://sourcer.club) — tools and community for talent sourcers.*
