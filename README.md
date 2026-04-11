# wstg-skill

A Claude Code skill that turns any project into an auditable, OWASP WSTG-compliant codebase — with the full WSTG v4.2 checklist built in, structured evidence templates, and a security-PR protocol designed for compliance audits (SOC 2, ISO 27001, ENS, PCI-DSS).

> **Why this exists:** OWASP WSTG is the reference standard for web security testing, but applying it to a real project means reading hundreds of pages, building checklists from scratch, and manually tracking findings. This skill gives Claude Code the methodology, the checklist, and the evidence templates so you can run a full audit and generate compliance-grade documentation from your terminal.

## What it does

- **Runs a guided WSTG v4.2 audit** against your project, auto-detecting the stack and filtering the ~100 test cases to the ones that actually apply
- **Generates a cumulative test register** — the evidence artifact auditors actually ask for
- **Documents findings** in a structured format with WSTG ID traceability
- **Drafts security PRs** with the full WSTG → issue-tracker → validation chain
- **Never closes a finding without evidence** (code, tests, or runtime validation)

## Installation

Clone into your Claude Code skills directory:

```bash
git clone https://github.com/aritzjl/wstg-skill.git ~/.claude/skills/wstg-skill
```

Or install into a single project:

```bash
cd your-project
git clone https://github.com/aritzjl/wstg-skill.git .claude/skills/wstg-skill
```

Claude Code will auto-discover the skill on next launch.

## Usage

Once installed, just talk to Claude naturally:

```
> Run a WSTG audit on this project
> Document a finding: our login endpoint leaks account existence via timing
> Fix DEV-64 following the WSTG protocol
> Generate a findings report for the last audit
```

The skill detects the intent, loads the relevant WSTG reference material, and drives the workflow from there.

## What's included

```
skills/wstg/
├── SKILL.md                      # Skill definition + workflow instructions
├── references/
│   └── wstg-v42/                 # Full WSTG v4.2 checklist, one file per category
│       ├── INFO.md               # Information Gathering (10 tests)
│       ├── CONF.md               # Configuration & Deployment (11 tests)
│       ├── IDNT.md               # Identity Management (5 tests)
│       ├── ATHN.md               # Authentication (10 tests)
│       ├── AUTHZ.md              # Authorization (4 tests)
│       ├── SESS.md               # Session Management (9 tests)
│       ├── INPV.md               # Input Validation (20 tests)
│       ├── ERRH.md               # Error Handling (2 tests)
│       ├── CRYP.md               # Cryptography (4 tests)
│       ├── BUSL.md               # Business Logic (9 tests)
│       ├── CLNT.md               # Client-Side (14 tests)
│       └── APIT.md               # API Testing (1 test)
└── assets/
    └── templates/
        ├── test-register.md      # Cumulative audit registry
        ├── checklist.md          # Per-execution checklist
        ├── findings-report.md    # Findings report format
        └── security-pr.md        # Security PR template
```

## The workflow

1. **Init** — Creates `docs/wstg/` in your project with the templates and an initial `test-register.md`
2. **Audit** — Runs a guided walkthrough of the applicable WSTG categories and records results in the register
3. **Finding** — Documents a concrete vulnerability with WSTG ID, severity, repro, and linked issue
4. **Fix** — Implements the fix and drafts a security PR with the full evidence chain
5. **Report** — Aggregates findings into a compliance-ready report

Every step leaves an audit trail. Nothing is closed without evidence.

## Philosophy

This skill is opinionated about three things:

1. **Traceability beats automation.** A finding without a WSTG ID and a linked issue is invisible to your compliance team.
2. **Evidence beats documentation.** Auditors want repro steps, commit hashes, and test output — not a paragraph saying "we fixed it".
3. **Registers are cumulative.** Rows in `test-register.md` are never deleted. History is the proof.

## Compatibility

Works with any web project. Auto-detects stack from common manifests:

- **Backend:** Python (FastAPI, Django, Flask), Node.js (Express, NestJS), Go, Ruby on Rails, PHP (Laravel, Symfony), Java (Spring)
- **Frontend:** React, Next.js, Vue, Nuxt, Angular, Svelte
- **Issue trackers:** Linear, GitHub Issues, Jira, GitLab Issues

If your stack isn't auto-detected, the skill falls back to asking you once and remembering for the project.

## Standard

Based on [OWASP Web Security Testing Guide v4.2](https://owasp.org/www-project-web-security-testing-guide/v42/).

## License

MIT. See [LICENSE](./LICENSE).

## Contributing

Contributions welcome — especially:

- Additional stack detectors
- Issue tracker integrations
- Corrections to the WSTG reference data
- New templates for specific compliance frameworks (SOC 2, ISO 27001, ENS, PCI-DSS)

Open an issue or PR at [github.com/aritzjl/wstg-skill](https://github.com/aritzjl/wstg-skill).
