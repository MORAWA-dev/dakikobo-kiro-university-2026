# Structure

- `app.py`: Flask routes and response assembly.
- `core/`: retrieval, routing, safety, domain logic, and provider adapters.
- `templates/` and `static/`: farmer-facing web interface.
- `tests/`: offline regression, browser, and integration checks.
- `Data/`: local agricultural source corpus and review records.
- `evaluation/`: release evidence and human validation material.
- `.kiro/specs/`: Kiro requirements, design, and executable task plans.

Prefer small changes at the narrowest module boundary. Preserve the JSON
contracts exercised by route and browser tests.
