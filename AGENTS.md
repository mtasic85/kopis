# AGENTS.md – internal guide for AI agents

## Build / Lint / Test
- Build: `uv build` (uv_build backend from pyproject.toml)
- Lint: `ruff check .` and `ruff format . --check`
- Type check: `ty check .` (pinned in dev group)
- Test a single test: `pytest -xvs tests/<test_file>.py -k <test_name>`
## Code Style
- Imports: stdlib -> third‑party -> local; explicit only
- Format: `ruff format`; line limit 88; trailing commas
- Naming: snake_case functions/vars, PascalCase classes
- Types: annotate public APIs; prefer `list[int]`
- Errors: raise custom exceptions
- Log with `logging`
- Docs: Google‑style; document Args, Returns, Raises
- Dependencies: version pins in `pyproject.toml`; keep dev deps separate
- Testing: under `tests/`; use pytest fixtures; mark flaky with `pytest.mark.flaky`
## Agent Usage
- Read `README.md` first; reference `pyproject.toml` for commands
- Use `write` only after reading; never commit directly
- Follow the style rules above
