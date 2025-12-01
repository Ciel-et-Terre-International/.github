# Ciel & Terre International – GitHub

This GitHub organization hosts the software, mechatronics, and R&D projects of Ciel & Terre International.

Repositories are organized by product line / activity using **prefixes**:

* **WattRack**: systems and projects related to water operations (trolley, mooring, lab, etc.)
* **Fusio**: land-based mechatronic projects
* **Optim**: software tools, data, telemetry, internal applications
* **R&D / Other**: research projects, prototypes, experimental work

This document describes the common conventions for the organization.

---

## Repository organization

Repositories are flat at the organization level, but logically grouped by **prefix**:

* `wattrack-…` – WattRack line
* `fusio-…` – Fusio line
* `optim-…` – Optim line
* `rd-…` or `misc-…` – R&D projects, tools, cross-cutting topics

Each repository must have its own `README.md` including:

* functional context
* technical architecture (high level)
* installation / build instructions
* how to run tests

---

## Naming and metadata

### Repository names

* all **lowercase**
* use **hyphens** (`-`) as separators
* use prefixes: `wattrack-`, `fusio-`, `optim-`, `rd-`
* short but explicit names (avoid opaque acronyms)


### Topics / tags

Use a few GitHub topics to make filtering easier:

* `wattrack`, `fusio`, `optim`, `rd`
* technology / domain tags such as `embedded`, `mechatronics`, `software`, `data`, `lab`, etc.

---

## Branching model and Git workflow

* Default branch: **`main`** (protected).
* Day-to-day work happens on feature branches:
  `feature/<short-description>`

Examples:

* `feature/add-can-support`
* `feature/new-dashboard`

### General rules

* Any change to `main` must go through a **Pull Request (PR)**.
* At least **1 approved review** is required before merge.
* CI (tests, lint, etc.) must be **green** before merge.
* No direct commits to `main`, except exceptional and documented cases.

---

## Minimum repository structure

The exact structure depends on the technology, but aim for at least:

```text
<repo>/
├── README.md         # description, installation, usage
├── src/              # main source code
├── tests/            # unit / integration tests
└── docs/             # additional documentation (optional)
```

---

## Issues and pull requests

### Issues

* Use issue templates (bug / feature / improvement) when available.
* Clear title, concise description, reproduction steps for bugs.
* Apply relevant labels (`bug`, `enhancement`, etc.).

### Pull requests

* One PR per coherent change / feature.
* Describe what changes and why.
* Reference related issues (for example: `Closes #123`).
* Add screenshots or logs when the change has a visible impact.

---

## Teams and ownership

Access is managed with **GitHub Teams** aligned with product lines:

* Team `WattRack`: maintains `wattrack-*` repositories
* Team `Fusio`: maintains `fusio-*` repositories
* Team `Optim`: maintains `optim-*` repositories
* Team `R&D`: maintains `rd-*` repositories

General principles:

* The owning team of a repository has write / maintain permissions.
* Other teams have at least read access, unless the project is sensitive.

---

## General best practices

* Prefer **small, frequent** changes over large, hard-to-review ones.
* Add and maintain **automated tests** whenever possible.
* Keep READMEs up to date (installation, usage, limitations).
* Document important decisions inside the repo (in `docs/` or PR descriptions).

---

## Contact

For questions about the GitHub organization or creating a new repository, contact:

* Internal GitHub owner: `<name / team>`
* Internal support channel: `<Teams / email link>`

Update this README whenever conventions change in a significant way.
