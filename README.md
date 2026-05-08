<<<<<<< HEAD
# ransomware_project (educational / defensive repo)

This workspace appears to contain **two distinct components**:

- `dnstwist/`: a legitimate, defensive **domain-fuzzing / typosquatting** and **phishing-detection** tool (upstream project).
- `ransomware.py`: **ransomware-like code** (file encryption + ransom note + wallpaper change + Windows API thread execution).

Because parts of this repo are **malware-capable**, this documentation is written for **analysis, auditing, and defensive learning**. It intentionally **does not provide instructions to deploy, build, or execute** ransomware functionality.

## Repository layout

- `ransomware.py`: Ransomware proof-of-concept (dangerous).
- `ransomware.spec`: PyInstaller spec referencing `ransomware.py` (packaging metadata).
- `wallpaper.jpg`: Image referenced by `ransomware.py`.
- `dnstwist/`: Defensive tooling with its own docs and Python packaging.
- Other folders (e.g. `safe/`, `build/`, `dist/`, `c/`): appear to be artifacts/experiments and may include generated outputs.

## Safety and handling

If you are reviewing this repository:

- **Do not run unknown binaries** from `dist/` or other build output directories.
- Prefer a **disposable VM** (no personal data, snapshots enabled, no shared clipboard/drive).
- Keep the machine **offline** unless you specifically need network access for analysis.
- Treat `ransomware.py` as **live malware**: it is designed to encrypt files and modify the desktop environment.

See `docs/SAFETY.md` for a concrete safe-analysis checklist and high-level behavior notes.

## Defensive component: dnstwist

The `dnstwist/` directory is an upstream defensive project with its own documentation:

- Main docs: `dnstwist/docs/README.md`
- Python dependencies: `dnstwist/requirements.txt`
- Entrypoints/scripts: `dnstwist/dnstwist.py`, `dnstwist/webapp/webapp.py`

If your goal is to use only the defensive tooling, focus on `dnstwist/` and ignore the ransomware PoC portions of the repo.

## Documentation index

- `docs/PROJECT_OVERVIEW.md`: What’s in this repo and how it relates.
- `docs/SAFETY.md`: Safe handling + high-level behaviors/IOCs for defenders.

=======
# Ransomware_project
>>>>>>> 972a210f4e9a9c4f38b77750762a6f47d05125ae
