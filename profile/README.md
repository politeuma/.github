# ConstitutiveTemplates

Legal-aware project scaffolding for the AI-agent era: templates that know
which rules apply to the code they generate, and a knowledge pipeline that
keeps those rules current.

```text
open-law                law-map                  kanon                   architekton-py / daimonion
world legislation  ->   obligation graph   ->    reviewed prose     ->    vendored into
scraped politely        (deontic rules +         sections for             generated
                        jurisdiction             humans and AI           repos
                        groundings)              agents
```

## Repositories

| Repo | Role |
|------|------|
|[architekton-py](https://github.com/ConstitutiveTemplates/architekton-py) | Opinionated Copier template for Python projects: 8 project types + opt-in layers, Z3-verified questionnaire, security & compliance built in |
| [open-law](https://github.com/ConstitutiveTemplates/open-law) | Scrapes and consolidates legislation from official sources worldwide into one unified shape (Akoma Ntoso where offered) |
| [law-map](https://github.com/ConstitutiveTemplates/law-map) | Machine-readable obligation graph — maps statutes, precedent, and guidance across jurisdictions to the technical duties software must satisfy |
| [kanon](https://github.com/ConstitutiveTemplates/kanon) | Canonical legal & ethical prose sections, reviewed and versioned, vendored into generated `AGENTS.md` files |
| [daimonion](https://github.com/ConstitutiveTemplates/daimonion) | Socrates' inner voice as a linter: fast, language-agnostic legal/ethical trigger scanning for diffs and source files, plus AGENTS.md ethics blocks for any repository |

## The pipeline

1. **open-law** fetches legislation through polite, robots-aware adapters —
   one per jurisdiction — and normalizes it.
2. **law-map** organizes that law by *function, not form* (functional
   equivalence): a Japanese statute, an EU regulation, and a US enforcement
   precedent that demand the same technical behavior ground one obligation
   node. Every grounding carries a `review_by` date; weekly drift-watch opens
   an issue when law or sources go stale.
3. **kanon** renders obligations into reviewed prose for humans
   and coding agents.
4. **daimonion** (formerly law-lint) ships a pinned snapshot inside its
   wheel and inserts matching ethics sections into any project's
   `AGENTS.md` — whatever template it came from — and scans diffs against
   the same triggers.
5. **architekton-py** (formerly daimonion) vendors pinned snapshots into
   generated repositories — `AGENTS.md` invariants, ethics appendices,
   and CI gates — so a new Python project starts compliant by default.
   Renders are pure functions of the template tree; nothing fetches law
   at render time.

## Not legal advice

Everything here is a technical guardrail, not legal counsel. Groundings cite
primary sources; expert review is required for real compliance decisions.
