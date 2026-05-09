# Claude Code Powerups — Distribution Checklist

Created: May 7, 2026
Context: Blog post written 2026-02-07, unpublished 12+ weeks. Assets ready for immediate distribution once CEO authorizes.

---

## Assets Ready (no additional work needed)

| Asset | File | Status |
|-------|------|--------|
| Dev.to post (preferred — better title) | `marketing/devto-launch-post.md` | Ready (copy-paste format) |
| Dev.to post (original, has frontmatter) | `docs/blog-post.md` | Ready (published: true) |
| Show HN draft | `marketing/show-hn-draft.md` | Ready |
| Reddit posts (r/ClaudeAI, r/programming, r/dotnet, r/azure, r/LangChain) | `marketing/reddit-posts.md` | Ready — 5 posts total |
| Indie Hackers post | `marketing/indie-hackers-post.md` | Ready |
| Newsletter pitches (.NET Weekly, InfoQ, Console.dev, TLDR) | `marketing/newsletter-pitches.md` | Ready |
| Product Hunt listing + maker comment | `marketing/product-hunt-listing.md` | Ready (post 1-2 wks after HN) |

---

## Distribution Sequence (CEO/Wael executes)

### Step 1 — Dev.to (5 min)
1. Open `marketing/devto-launch-post.md` — this has the preferred title: "I built 3 Claude Code plugins so I'd stop re-explaining the same context across .NET and Azure projects"
2. Go to dev.to → New Post → paste the content from the Body section
3. Set tags: claudecode, dotnet, azure, security
4. Add cover image if available (skip if not — launch without it)
5. Publish immediately
6. Copy the Dev.to URL for use in Reddit posts and IH comment

### Step 2 — Show HN (5 min)
1. Go to news.ycombinator.com/submit
2. Title: `Show HN: Claude Code plugins for Clean Architecture, Azure, and OWASP LLM security`
3. URL: GitHub marketplace repo (github.com/waelouf/claude-code-powerups)
4. Post Tuesday or Wednesday, 7–9am ET
5. Engage with every comment in the first 6 hours

### Step 3 — r/ClaudeAI (5 min)
1. Use draft from `marketing/reddit-posts.md` — Post 1
2. Post same day as HN, stagger 1–2 hours after HN goes up
3. Engage with comments

### Step 4 — r/programming (5 min)
1. Use draft from `marketing/reddit-posts.md` — Post 2
2. Post Day 2
3. Check r/programming rules — self-promotion usually allowed with technical framing

### Step 5 — Domain-specific subreddits (10 min total)
- r/dotnet: Post 3 from reddit-posts.md (Week 2) — Clean Architecture Powerup angle
- r/azure: Post 4 from reddit-posts.md (Week 2) — Azure Architect Powerup, IaC + CI/CD focus
- r/LangChain: Post 5 from reddit-posts.md (Week 2) — OWASP LLM security auditor focus

### Step 6 — Indie Hackers post (10 min)
1. Open `marketing/indie-hackers-post.md`
2. Post on indiehackers.com — same day as Dev.to or within 48 hours
3. Link the Dev.to post in the IH post if it has gotten upvotes

### Step 7 — Newsletter pitches (15 min)
1. Open `marketing/newsletter-pitches.md`
2. Send .NET Weekly pitch first (longest lead time: 1-2 weeks)
3. Send InfoQ pitch same day
4. Submit Console.dev tool listing
5. Submit TLDR link (Dev.to URL) via tldr.tech/submit

### Step 8 — Product Hunt (separate from HN day)
- Launch on Product Hunt 1-2 Tuesdays after the HN post
- Use `marketing/product-hunt-listing.md` — maker's comment is pre-written
- Do NOT launch PH same day as HN — split traffic hurts both

### Optional: Hashnode
- Same content as Dev.to, cross-post with canonical URL pointing to Dev.to
- Hashnode auto-syncs from Dev.to if accounts are linked

---

## Success Metrics (30 days)

| Metric | Target |
|--------|--------|
| Dev.to reactions | 50+ |
| HN Show HN points | 20+ |
| GitHub stars delta | +25 |
| Plugin installs (if trackable) | +50 |

---

## Note on Timing

12 weeks of delay has already reduced the first-mover advantage. However:
- Claude Code is still growing rapidly (new users discover it daily)
- The plugins are still relevant (no major API breaking changes)
- r/ClaudeAI community has grown since Feb — more potential audience now than at launch

Post this week. Every additional week of delay loses organic discovery.
