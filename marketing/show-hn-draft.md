# Claude Code Powerups — Show HN Draft

Created: May 7, 2026
Status: Ready to post. Requires CEO authorization (MBS-147).

---

## Title

```
Show HN: Claude Code Powerups – plugins for Clean Architecture, Azure, and OWASP LLM security
```

## Body

```
I've been using Claude Code heavily and found myself re-explaining the same context repeatedly across projects — what Clean Architecture means for this codebase, how I want Azure resources structured, which OWASP LLM checks to run.

So I packaged my workflows into three Claude Code plugins:

**Clean Architecture Powerup** — for .NET Clean Architecture projects. Scaffolds new projects and features across layers, runs architectural audits to catch pattern violations, helps migrate legacy code. Uses FastEndpoints.

**Azure Architect Powerup** — generates infrastructure-as-code (Bicep/Terraform), sets up CI/CD pipelines for GitHub Actions and Azure DevOps, handles multi-environment configs, applies basic security and monitoring defaults.

**OWASP LLM Top 10 Security Auditor** — scans AI application code for OWASP LLM Top 10 vulnerabilities, generates risk assessments, flags issues before deployment. Useful if you're building Claude/GPT integrations and want a structured security review.

Install:
```
claude-code plugin install waelouf/claude-code-powerups
```

Or individually:
```
claude-code plugin install waelouf/cc-powerup-clean-architecture
claude-code plugin install waelouf/cc-powerup-azure-architect
claude-code plugin install waelouf/cc-powerup-owasp-llm
```

All open source. Happy to answer questions about any of the implementation choices.
```

---

## Timing Notes

- Post Tuesday or Wednesday, 7–9am ET
- Title character count: 93 (HN limit is ~80 visible chars, full title still accepted)
- Alternative shorter title: `Show HN: Claude Code plugins for Clean Architecture, Azure, and OWASP LLM security`
