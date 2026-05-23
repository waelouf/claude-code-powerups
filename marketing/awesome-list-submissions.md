# Claude Code Powerups — Awesome List Submissions

Created: 2026-05-21
Status: Ready to submit after CEO authorizes distribution (MBS-147). GitHub repos must be public before submitting.
Gate: Verify repos are public first — see distribution-checklist.md Pre-Launch Verification section.
Context: PR submissions to curated awesome lists. Wael submits from personal GitHub account (waelouf).

---

## Target Lists (Priority Order)

| List | Stars | Powerup fit | When to submit |
|------|-------|------------|----------------|
| awesome-dotnet | ~20K | Clean Architecture Powerup | After CEO auth + repos public |
| awesome-azure | ~15K | Azure Architect Powerup | After CEO auth + repos public |
| awesome-claude / awesome-claude-code | Various | All 3 powerups (marketplace) | After CEO auth + repos public |
| awesome-llm-tools | ~10K | OWASP LLM Auditor | After CEO auth + repos public |

---

## 1. awesome-dotnet

**Repo:** github.com/quozd/awesome-dotnet  
**PR title:** Add Claude Code Powerup for Clean Architecture  
**Target section:** `Tools` → `IDE` or `Code Analysis/Metrics` (add to whichever fits alphabetically)

**Entry to add:**
```markdown
* [Claude Code Powerup — Clean Architecture](https://github.com/waelouf/cc-powerup-clean-architecture) - Claude Code skill that scaffolds full feature layer stacks for Clean Architecture + FastEndpoints .NET projects, audits layer boundary violations, and guides incremental migrations from legacy codebases.
```

**PR body:**
```
## Description

Claude Code Powerup for Clean Architecture is a SKILL file for Claude Code (Anthropic's
coding assistant) that packages Clean Architecture knowledge for .NET projects.

What it does:
- Scaffolds complete feature layer stacks (Domain entity → Application handler → 
  Infrastructure → FastEndpoint) with correct dependency direction
- Audits existing codebases for layer boundary violations (domain logic in 
  infrastructure, missing abstractions)
- Guides incremental migration of legacy projects toward Clean Architecture 
  without big-bang rewrites

Target stack: .NET 10, FastEndpoints, Clean Architecture, EF Core.
Install: claude mcp add https://github.com/waelouf/cc-powerup-clean-architecture

- GitHub: https://github.com/waelouf/cc-powerup-clean-architecture
- License: MIT
- Platform: Claude Code (claude.ai/code)

## Checklist
- [x] I am the author/maintainer
- [x] The project is actively maintained
- [x] Entry is added in alphabetical order
```

---

## 2. awesome-azure

**Repo:** github.com/kristofferandreasen/awesome-azure  
**PR title:** Add Claude Code Powerup for Azure Architecture  
**Target section:** `Tools` or `Developer Tools`

**Entry to add:**
```markdown
* [Claude Code Powerup — Azure Architect](https://github.com/waelouf/cc-powerup-azure-architect) - Claude Code skill for Azure IaC and CI/CD scaffolding. Generates Bicep modules, Azure DevOps pipelines, GitHub Actions workflows, and App Service / Container Apps / AKS configurations following Azure Well-Architected Framework principles.
```

**PR body:**
```
## Description

Claude Code Powerup for Azure Architecture is a SKILL file for Claude Code that packages
Azure infrastructure and DevOps knowledge.

What it does:
- Generates Bicep modules for Azure resources (App Service, Container Apps, AKS, 
  SQL, Storage, Key Vault) following WAF naming conventions
- Scaffolds GitHub Actions and Azure DevOps pipelines with proper secret management
- Audits existing IaC for WAF violations (cost, reliability, security, performance)
- Provides environment-specific deployment guidance (dev/staging/prod)

Install: claude mcp add https://github.com/waelouf/cc-powerup-azure-architect

- GitHub: https://github.com/waelouf/cc-powerup-azure-architect
- License: MIT
- Platform: Claude Code (claude.ai/code)
```

---

## 3. awesome-llm-tools / AI tool directories

**Target repos (submit to whichever are active):**
- github.com/filipecalegario/awesome-generative-ai
- github.com/steven-tey/awesome-claude (if exists / active)
- Any "awesome-claude-code" repo

**Entry for marketplace (submit to all):**
```markdown
* [Claude Code Powerups](https://github.com/waelouf/claude-code-powerups) - Marketplace of Claude Code SKILL files for .NET Clean Architecture, Azure IaC/CI-CD, and OWASP LLM security auditing. Install individual powerups or browse all.
```

**Entry for OWASP LLM Auditor specifically:**
```markdown
* [Claude Code Powerup — OWASP LLM Auditor](https://github.com/waelouf/cc-powerup-owasp-llm) - Claude Code skill that audits LLM application code against the OWASP LLM Top 10 (prompt injection, insecure output handling, training data poisoning, etc.) and generates a prioritized finding report with remediation guidance.
```

---

## Submission Notes

- Submit PRs from github.com/waelouf (personal account, project author)
- One PR per list — do not batch multiple lists into one PR
- Check each list's CONTRIBUTING.md before submitting (some have specific requirements)
- awesome-dotnet and awesome-azure are the highest-value targets (largest audiences, best fit)
- Submit awesome-dotnet and awesome-azure on the same day as the Dev.to post for maximum momentum
- Do NOT submit before GitHub repos are confirmed public (would result in 404 links in the PR)
