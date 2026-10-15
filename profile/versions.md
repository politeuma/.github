# Version compatibility / 版の対応表

Which combinations of politeuma pieces work together. Read-only draft
from inspection of the sibling repos on 2026-10-15 — update the SHAs
when any side moves.

| Piece | Version / pin | Commit (2026-10-15) |
|---|---|---|
| law-map schema | **v2** (`schemas/obligation.schema.yml`; `version` must equal `2`) | `91c00b0` |
| daimonion rulebook snapshot | `LAWMAP_SHA` `c4aaf02` (vendored `guidance/sections` + `checks/`, MANIFEST declares `schema: 2`) | daimonion `2a43156` |
| daimonion package | `0.1.0` (no tags yet; PyPI unpublished) | `2a43156` |
| architekton-py → daimonion | template pins `daimonion_spec` to `daimonion@5ec9539` (commit pin, moves to hash-pinned PyPI once published) | architekton-py `2908a892` |
| open-law | setuptools-scm versioned, no tags (PyPI unpublished) | `9b491dd` |
| kanon | archived; README points to law-map `guidance/` | `0d17f96` |

Notes:

- law-map → daimonion is currently **several commits behind**: vendored
  `LAWMAP_SHA` (`c4aaf02`) predates law-map HEAD (`91c00b0`). The lagging
  commits add per-grounding `confidence` (`high/medium/low`, schema still
  v2 — optional field) to most `obligations/` files plus docs and
  tooling, so the vendored snapshot parses but no longer reflects the
  newest grounding metadata. Re-vendor via
  `python tools/vendor_rulebook.py ../law-map` (daimonion action).
- No PyPI releases or git tags exist yet for law-map, daimonion,
  open-law, or kanon (owner action). architekton-py is the exception
  with tags `6.0.0`, `6.1.0`, `7.0.0`. Until date-versions land
  (ARCH-5, e.g. `2026.11`), the commit SHAs above are the pairing
  contract.
- Consumers take daimonion's output, not law-map directly; the only
  hard compatibility edge is rulebook **schema v2** ↔ daimonion's
  vendored-spec loader.
