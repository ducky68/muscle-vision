# Muscle Vision — AGENTS.md

## Mission

Build **Muscle Vision**, an Astra-powered interactive 3D anatomy trainer for the GPT-6 Astra hackathon.

Muscle Vision helps users understand how exercise technique affects muscle emphasis.

The user selects an exercise, grip, posture, playback speed, and viewing angle. A 3D anatomical human performs the exercise continuously while relevant muscles are highlighted dynamically throughout the movement.

The application must be visually compelling, easy to understand, and realistically buildable as a hackathon prototype.

---

## Source of Truth

Before implementation, read:

- `docs/PRD.md`
- `docs/ROADMAP.md`
- `docs/PROGRESS.md`
- `docs/DEMO.md`
- `docs/REFERENCES.md`

Responsibilities:

- `PRD.md` = what the product is and how it should work
- `ROADMAP.md` = implementation phases and acceptance criteria
- `PROGRESS.md` = current implementation state
- `DEMO.md` = scripted <=90-second demonstration
- `REFERENCES.md` = anatomy, exercise, UX, and technical references

Do not duplicate large amounts of product specification inside this file.

---

# Hard Constraints

## Build Constraints

- This is a solo hackathon build.
- Target implementation time is approximately **3–4 hours**.
- Prioritize a working and polished prototype over feature count.
- Do not expand scope without explicit approval.
- Build incrementally according to `ROADMAP.md`.
- A working smaller prototype is preferable to a partially working larger prototype.

---

## Required Technology

The intended stack is:

- **Three.js / React Three Fiber** for the interactive 3D browser experience
- **Blender** for preparing, rigging, animating, and exporting 3D assets
- **GLB / glTF** for browser-ready 3D assets
- **GPT-6 Astra** for reasoning, explanation, comparison, and orchestration
- **ChatGPT Sites** for final deployment
- **Git + GitHub** for source control

Do not introduce additional infrastructure unless it materially improves the required prototype.

---

# Python Tooling

If Python is used anywhere in this project:

- Use **uv** as the Python package and environment manager.
- Do not use `pip` directly unless `uv` cannot support the required operation.
- Do not create environments with `python -m venv`.
- Keep Python dependencies in `pyproject.toml`.
- Keep `uv.lock` under version control.
- Prefer running Python commands through `uv run`.

Preferred commands:

```bash
uv init
uv add <package>
uv remove <package>
uv sync

uv run python script.py
uv run pytest