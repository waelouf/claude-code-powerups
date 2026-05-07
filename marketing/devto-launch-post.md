# Claude Code Powerups — Dev.to Launch Post

Platform: dev.to
Status: Ready to post. Requires CEO authorization (MBS-147). Post same day as Show HN.
Tags: claudecode, dotnet, azure, security

---

## Title

```
I built 3 Claude Code plugins so I'd stop re-explaining the same context across .NET and Azure projects
```

---

## Body

```
Every time I started a new .NET project in Claude Code, I spent 10 minutes re-establishing the same context: what Clean Architecture means in this codebase, which layers exist, how they depend on each other, and what patterns I want followed. On the third project, I decided to package that context once.

I ended up with three plugins. This post walks through what each one does and the implementation choices behind them.

---

## The Problem

Claude Code is genuinely useful for architectural tasks — scaffolding new features, auditing layer boundaries, generating infrastructure. But it doesn't automatically know:

- That this project uses FastEndpoints, not MVC controllers
- That the Azure setup should use Bicep with a specific module structure
- That this is an AI application and should be evaluated against the OWASP LLM Top 10

Without explicit context, you get generic answers. The plugins are that context, packaged.

---

## Plugin 1: Clean Architecture Powerup

Designed for .NET projects using Clean Architecture + FastEndpoints.

**Scaffolding:** Given a feature name, the plugin creates the full layer stack — domain entity, application command/query handlers, infrastructure implementation, FastEndpoint — with the correct dependencies and no layer violations.

Before this, I'd create the files manually, route them correctly, wire up dependencies, and realize 20 minutes later I'd put something in the wrong layer. Now it's one command.

**Audit mode:** The plugin can scan an existing codebase for architectural violations: domain logic in infrastructure, application layer bypassing domain, missing abstractions. The output is a violation list with file references — not a lecture, just findings.

**Migration assistance:** For legacy projects that are being moved toward Clean Architecture incrementally, the plugin understands the current state and suggests next steps that move in the right direction without requiring a big-bang rewrite.

The main implementation challenge was representing "what Clean Architecture means" in a way that produces consistent results across different project structures. The plugin encodes the dependency rules explicitly rather than relying on Claude's general knowledge of the pattern.

---

## Plugin 2: Azure Architect Powerup

Generates Bicep/Terraform for Azure infrastructure and CI/CD pipelines for GitHub Actions / Azure DevOps.

The key behavior: the output reflects your actual project context, not a template. If you ask for "a production-ready Azure setup for this API," the plugin generates resources appropriate to a .NET minimal API backend — App Service or Container Apps, Key Vault for secrets, Application Insights for observability — with naming conventions that match Azure's recommendations and environment separation (dev/staging/prod) built in.

Pipeline generation handles the common patterns: build, test, publish, deploy with environment promotion gates. The plugin knows the difference between what you'd do in GitHub Actions versus Azure DevOps and generates accordingly.

Security defaults are applied without prompting: managed identities instead of connection strings where possible, HTTPS enforcement, diagnostic logging enabled.

---

## Plugin 3: OWASP LLM Top 10 Security Auditor

This one started as a personal checklist and became a plugin because I kept forgetting to run it before shipping AI features.

The OWASP LLM Top 10 covers vulnerabilities specific to AI-integrated applications that general security scanners don't check:

- **LLM01: Prompt Injection** — User input that can alter model behavior
- **LLM02: Insecure Output Handling** — Trusting model output without sanitization
- **LLM06: Sensitive Information Disclosure** — Inadvertently leaking training data or system prompts
- **LLM09: Overreliance** — Critical decisions delegated to the model without validation

The plugin scans the codebase and generates a risk assessment per vulnerability category: what was found, what the potential impact is, and what the fix looks like. The output is a structured report, not a general warning.

It's most useful just before you hand an AI feature to anyone else. Running it at that point consistently surfaces something — usually in prompt construction or output trust.

---

## Install

```
claude-code plugin install waelouf/claude-code-powerups
```

Or individually:

```
claude-code plugin install waelouf/cc-powerup-clean-architecture
claude-code plugin install waelouf/cc-powerup-azure-architect
claude-code plugin install waelouf/cc-powerup-owasp-llm
```

All three are open source: github.com/waelouf/claude-code-powerups

---

## What I'd Build Differently

I shipped all three together because they were all done. If I were starting over: release Clean Architecture first, validate the workflow, then add Azure and OWASP as follow-ons. The Clean Architecture plugin is the one I use daily. The OWASP auditor is the one I use once before shipping an AI feature. Bundling them made the install simpler but obscured the use case differentiation.

Happy to answer questions about the plugin implementation, the Clean Architecture pattern choices, or the OWASP LLM Top 10 audit logic.
```

---

## Cover Image

Use the MBSoft Systems logo or a simple dark banner with "Claude Code Powerups" and the three plugin names. Dev.to renders a 1000x420px cover image.

## Tags

`claudecode` `dotnet` `azure` `security`

## Notes

- Canonical URL: leave blank (Dev.to as primary)
- Post same day as Show HN (Show HN in morning, Dev.to 2-3 hours after)
- Link the Dev.to post in the Show HN thread as "technical writeup"
- Cross-post to r/dotnet and r/ClaudeAI with a link to the Dev.to post on day 2
