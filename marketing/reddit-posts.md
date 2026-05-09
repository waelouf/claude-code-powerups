# Claude Code Powerups — Reddit Distribution

Created: May 7, 2026
Status: Ready to post. Requires CEO authorization (MBS-147).

---

## Subreddit Priority

| Subreddit | Members | Post type | Timing |
|-----------|---------|-----------|--------|
| r/ClaudeAI | 50K+ | Product announcement | Day 1 |
| r/programming | 6M+ | Technical tool post | Day 2 |
| r/dotnet | 80K+ | Clean Architecture showcase | Week 2 |
| r/azure | 120K+ | Azure plugin announcement | Week 2 |
| r/LangChain | 30K+ | OWASP LLM security tool | Week 2 |

---

## Post 1: r/ClaudeAI

**Title:**
```
I built 3 Claude Code plugins for Clean Architecture, Azure, and OWASP LLM security
```

**Body:**
```
Been using Claude Code heavily across .NET, Azure, and AI application projects. Kept re-explaining the same context — what Clean Architecture means, how I want Azure structured, which OWASP checks to run.

Built these into 3 installable plugins:

**Claude Code Powerups**

1. **Clean Architecture Powerup** — .NET projects with Clean Architecture. Scaffolds projects/features across layers, audits for architectural violations, assists with migrations. Works with FastEndpoints.

2. **Azure Architect Powerup** — Infrastructure-as-code (Bicep/Terraform), CI/CD pipeline setup for GitHub Actions + Azure DevOps, multi-environment configs, security and monitoring defaults.

3. **OWASP LLM Top 10 Security Auditor** — Scans AI application code for OWASP LLM Top 10 issues. Generates risk reports, flags vulnerabilities before deployment. Useful for Claude/GPT integrations.

Install all three:
```
claude-code plugin install waelouf/claude-code-powerups
```

All open source: github.com/waelouf/claude-code-powerups

Would love feedback — especially on the Clean Architecture and OWASP auditing workflows.
```

---

## Post 2: r/programming

**Title:**
```
Open-source Claude Code plugins for Clean Architecture scaffolding, Azure IaC, and OWASP LLM security audits
```

**Body:**
```
I've been building on top of Claude Code's plugin system and wanted to share three plugins I've found useful:

**[Claude Code Powerups](https://github.com/waelouf/claude-code-powerups)**

Three separate plugins, installable independently or together:

**1. Clean Architecture Powerup** (`cc-powerup-clean-architecture`)
- Interactive scaffolding for new .NET Clean Architecture projects
- Feature generation across Domain/Application/Infrastructure/Presentation layers
- Architectural audits — detects layer violations
- Migration assistance for legacy codebases
- Works with FastEndpoints

**2. Azure Architect Powerup** (`cc-powerup-azure-architect`)
- Infrastructure-as-code generation (Bicep and Terraform)
- CI/CD pipeline templates for GitHub Actions and Azure DevOps
- Multi-environment configuration (dev/staging/prod)
- Security and monitoring setup
- Cost optimization guidance

**3. OWASP LLM Top 10 Security Auditor** (`cc-powerup-owasp-llm`)
- Scans AI application code against OWASP LLM Top 10 vulnerabilities
- Generates structured risk assessments
- Remediation guidance per finding
- Pre-deployment audit workflow

Install:
```bash
claude-code plugin install waelouf/claude-code-powerups
```

Or individually:
```bash
claude-code plugin install waelouf/cc-powerup-clean-architecture
claude-code plugin install waelouf/cc-powerup-azure-architect  
claude-code plugin install waelouf/cc-powerup-owasp-llm
```

Everything's open source on GitHub. Happy to answer questions about implementation.

[github.com/waelouf/claude-code-powerups](https://github.com/waelouf/claude-code-powerups)
```

---

## Post 3: r/dotnet

**Title:**
```
Claude Code plugin for .NET Clean Architecture — scaffolding, audits, and migration assistance
```

**Body:**
```
Built a Claude Code plugin specifically for .NET Clean Architecture projects.

**Clean Architecture Powerup** — what it does:

- **Project scaffolding** — sets up a new CA project without missing boilerplate (Domain, Application, Infrastructure, Presentation layers, FastEndpoints integration)
- **Feature generation** — generates CRUD features across all layers from a single prompt, including commands, queries, validators, and endpoints
- **Architectural audits** — scans your codebase for layer violations (e.g., domain referencing infrastructure) and reports them
- **Migration assistance** — helps refactor existing code toward Clean Architecture
- **Pattern library** — common patterns ready to reference in context

Install:
```bash
claude-code plugin install waelouf/cc-powerup-clean-architecture
```

GitHub: github.com/waelouf/cc-powerup-clean-architecture

Would love feedback from others doing CA in .NET — especially on the audit detection patterns.
```

---

## Post 4: r/azure (Week 2)

**Title:**
```
Claude Code plugin for Azure IaC and CI/CD — generates Bicep/Terraform, GitHub Actions pipelines, and multi-env configs
```

**Body:**
```
I built a Claude Code plugin specifically for Azure infrastructure work: Azure Architect Powerup.

**What it does:**

- **Infrastructure-as-code generation** — prompts Azure resource requirements, outputs Bicep or Terraform. Covers VNets, App Services, AKS, SQL, storage, Key Vault, with production-grade defaults (private endpoints, diagnostics, tagging).
- **CI/CD pipeline scaffolding** — generates GitHub Actions and Azure DevOps pipelines for .NET apps, including build, test, and deployment stages across environments.
- **Multi-environment configs** — dev/staging/prod environment templates with parameter files, environment-specific overrides, and consistent naming conventions.
- **Security and monitoring defaults** — NSGs, Key Vault references for secrets (not inline), Log Analytics workspace wiring, alerts. Not optional add-ons — built into generated templates.
- **Cost optimization guidance** — flags expensive defaults (reserved capacity, right-sizing, dev environment scale-downs).

Install:
```bash
claude-code plugin install waelouf/cc-powerup-azure-architect
```

Or with the full suite:
```bash
claude-code plugin install waelouf/claude-code-powerups
```

GitHub: github.com/waelouf/claude-code-powerups

Would love feedback from Azure practitioners — especially on the Bicep output quality and whether the multi-env pattern matches what you'd actually use in production.
```

---

## Post 5: r/LangChain (Week 2)

**Title:**
```
Open-source Claude Code plugin for OWASP LLM Top 10 security audits — scans your AI app code before you deploy
```

**Body:**
```
Built an OWASP LLM Top 10 security auditor as a Claude Code plugin. Useful if you're building LLM applications (LangChain, LlamaIndex, Claude/GPT integrations, RAG pipelines) and want to scan for known vulnerability patterns before deploying.

**What it covers (OWASP LLM Top 10):**

- LLM01 Prompt Injection — unsanitized user input passed to prompts, jailbreak surface area
- LLM02 Insecure Output Handling — unescaped model output rendered in browsers or shells
- LLM03 Training Data Poisoning — data pipeline hygiene, source validation
- LLM04 Model Denial of Service — unbounded input sizes, rate limiting gaps
- LLM05 Supply Chain Vulnerabilities — third-party model and plugin dependencies
- LLM06 Sensitive Information Disclosure — PII in prompts, logs, stored completions
- LLM07 Insecure Plugin Design — plugin/tool call trust boundaries
- LLM08 Excessive Agency — tool permissions, action reversibility, approval gates
- LLM09 Overreliance — missing fallbacks, no human review gates for high-stakes decisions
- LLM10 Model Theft — API key exposure, model endpoint access controls

**Output:** structured risk report per finding, severity rating, remediation guidance. Designed to run as a pre-deployment check.

Install:
```bash
claude-code plugin install waelouf/cc-powerup-owasp-llm
```

Or with the full suite:
```bash
claude-code plugin install waelouf/claude-code-powerups
```

GitHub: github.com/waelouf/claude-code-powerups

Curious what security checks others are running on their LLM pipelines before shipping — anything you'd add to the OWASP list?
```

---

## Timing

- **Day 1 (immediately after CEO authorization):** Post r/ClaudeAI
- **Day 1 (same day, stagger 2h):** Post to HN (see show-hn-draft.md)
- **Day 2:** Post r/programming
- **Week 2:** Post r/dotnet, then r/azure, then r/LangChain (1-2 days apart)
