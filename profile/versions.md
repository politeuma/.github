# Version compatibility / 版の対応表

Which combinations of politeuma pieces work together. Read-only draft
from inspection of the sibling repos on 2026-10-15 — update the SHAs
when any side moves.

| Piece | Version / pin | Commit (2026-10-15) |
|---|---|---|
| law-map schema | **v2** (`schemas/obligation.schema.yml`; `version` must equal `2`) | `c4aaf02` |
| daimonion rulebook snapshot | `LAWMAP_SHA` `8ba7170` (vendored `guidance/sections` + `checks/`, MANIFEST declares `schema: 2`) | daimonion `2f315ec` |
| daimonion package | `0.1.0` (no tags yet; PyPI unpublished) | `2f315ec` |
| architekton-py → daimonion | template pins `daimonion_spec` to `daimonion@5ec9539` (commit pin, moves to hash-pinned PyPI once published) | architekton-py `fb24b4cb` |
| open-law | setuptools-scm versioned, no tags (PyPI unpublished) | `9b491dd` |
| kanon | archived; README points to law-map `guidance/` | `0d17f96` |

Notes:

- law-map → daimonion is currently **one commit behind**: vendored
  `LAWMAP_SHA` (`8ba7170`) predates law-map HEAD (`c4aaf02`), but the
  lagging commit only adds `law-map export` (guidance-format `.md`
  drafts) — no obligation, grounding, or check-spec content changed, so
  the vendored snapshot is still current in substance.
- No PyPI releases or git tags exist yet for law-map, daimonion, or
  open-law (owner action). Until date-versions land (ARCH-5, e.g.
  `2026.11`), the commit SHAs above are the pairing contract: daimonion
  maintainers refresh via `python tools/vendor_rulebook.py ../law-map`.
- Consumers take daimonion's output, not law-map directly; the only
  hard compatibility edge is rulebook **schema v2** ↔ daimonion's
  vendored-spec loader.
