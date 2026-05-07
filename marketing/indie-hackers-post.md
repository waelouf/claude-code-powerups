# Claude Code Powerups — Indie Hackers Post

Platform: indiehackers.com/post
Status: Publish after CEO authorizes distribution (MBS-147); coordinate with Show HN post same week
Category: Show IH / Product launches

---

## Title

```
I packaged my repeated Claude Code context into three plugins — Clean Architecture scaffolding, Azure IaC, and OWASP LLM security
```

---

## Body

```
I've been using Claude Code heavily across multiple .NET projects and found myself typing the same context repeatedly: "This project uses Clean Architecture with FastEndpoints. The layers are..." By the third project, that felt like a problem worth solving.

The context that keeps recurring breaks into three categories: how the codebase is structured (Clean Architecture), how infrastructure should be configured (Azure), and what security checks should run on AI-integrated code (OWASP LLM Top 10).

I packaged each into a Claude Code plugin.

---

**Clean Architecture Powerup**

For .NET Clean Architecture projects using FastEndpoints. Three main capabilities:

- Scaffold new projects and features across layers (Domain, Application, Infrastructure, API) following the pattern without manually routing files
- Run architectural audits that catch pattern violations — domain logic leaking into controllers, missing abstractions, incorrect dependency directions
- Assist migration of legacy code into Clean Architecture patterns

This one saves the most time. The scaffolding alone removes 20-30 minutes of file creation and layer plumbing from every new feature.

---

**Azure Architect Powerup**

Generates infrastructure-as-code (Bicep and Terraform), sets up CI/CD pipelines for GitHub Actions and Azure DevOps, handles multi-environment configurations, and applies security and monitoring defaults. The output follows Azure naming conventions and resource group patterns.

Useful for the moment you're about to copy-paste Bicep from a previous project and adjust it. The plugin generates to your current context instead.

---

**OWASP LLM Top 10 Security Auditor**

Scans AI application code for the OWASP LLM Top 10 vulnerabilities and generates a risk assessment. If you're building integrations with Claude, GPT, or other LLMs, this plugin runs a structured security review before you ship.

The OWASP LLM Top 10 covers things that general security scanners miss: prompt injection vectors, training data poisoning exposure, excessive agency patterns. The plugin surfaces these in context, where you can fix them before they reach production.

---

**Install**

```
claude-code plugin install waelouf/claude-code-powerups
```

Or individually:
```
claude-code plugin install waelouf/cc-powerup-clean-architecture
claude-code plugin install waelouf/cc-powerup-azure-architect
claude-code plugin install waelouf/cc-powerup-owasp-llm
```

All three are open source.

---

**What I'd build differently**

The OWASP auditor was the most interesting to build but has the lowest immediate utility for most users — you need to be building AI applications for it to be relevant. The Clean Architecture scaffolding is the one I use every day.

If I were shipping again, I'd lead with Clean Architecture only, validate the workflow, then release Azure and OWASP as follow-ons. I shipped all three together because the effort was already done and splitting release felt artificial.

Happy to answer questions about any of the plugin designs, the Clean Architecture pattern choices, or the OWASP LLM Top 10 implementation approach.
```

---

## Update Instructions Before Publishing

1. Confirm GitHub links are live before publishing
2. This post should coordinate with Show HN and r/ClaudeAI posts (same week, different days)
3. Blocked on CEO authorization (MBS-147)
4. Cross-post to IH groups: "AI", "Developer Tools", "Open Source"

## Posting Notes

- Post Tuesday or Wednesday morning ET
- IH audience will ask about revenue model — address it in first comment ("open source, no paid tier, built because I needed it")
- The OWASP LLM Top 10 is a conversation starter for the security-minded IH audience
