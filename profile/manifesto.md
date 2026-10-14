# politeuma manifesto

Coding agents now write much of our code. They are fast, tireless, and
entirely unaware of the law. Most developers are not much better informed:
statutes are long, scattered across countries, and keep changing — while
legal review cannot look at every pull request.

So unlawful code ships by default: personal identifiers in plaintext logs,
unconsented data transfers, inaccessible interfaces. Not from malice. From
nobody putting the rule where the code was written.

politeuma exists to put the rule where the code is written.

We turn legal requirements into short, sourced rules that sit next to your
code — in `AGENTS.md`, where people and agents read them, and as checks in
CI. Laws that differ in form but demand the same behaviour are grouped as
one obligation, so a team implements each rule once. Every rule shows its
sources and the date it was last checked, because law changes and sources
go stale.

These are reminders with receipts, not verdicts. No tool can decide whether
your product complies with any law, and using these rules does not make
anything compliant. What they can do is make sure that whoever — or
whatever — is about to add a log line sees, in that moment, the three
sources behind "don't put raw personal identifiers in logs."

This project grows out of the Good-future idea: that software should be
built so that doing the right thing is the easy thing, and that the
discipline for doing so should live in code and checks, not in documents
nobody reads. politeuma is that idea applied to law.

We start Japan-first and global-ready: built in Japan, grounded first in
Japanese, EU, and US law, open to every jurisdiction. The canonical
language is English, with a maintained Japanese translation alongside.

Not legal advice. Engineering guardrails with citations; ask a qualified
professional for compliance decisions.
