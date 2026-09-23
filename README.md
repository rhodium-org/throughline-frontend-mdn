# throughline-frontend-mdn

**MDN Web Docs front-end best practices** (accessible, semantic, maintainable
HTML/CSS/JS) expressed as a [throughline](https://pypi.org/project/throughline/)
**source** — a standalone, grounded requirements graph that a consuming project
composes with
`tl` from [throughline](https://pypi.org/project/throughline/) 3.11.0 or later.

This repository holds no code. It is a directory of small YAML items with permanent
UIDs, validated by `tl check`. Consumers import it under a namespace and reference
its rules as `mdn:SR-0001`.

## One of three alternative front-end sources

This is a **concern** source, and one of **three alternative front-end sources** a
project chooses among according to its priority:

- **`throughline-frontend-mdn`** (this repo) — the open-web platform's semantics and
  accessibility, reverse-engineered from MDN Web Docs. Pick this when your priority is
  accessible, semantic, standards-first HTML/CSS/JS.
- **`throughline-frontend-web-vitals`** — Google's Core Web Vitals, when your priority
  is measured loading, interactivity and visual-stability performance.
- **`throughline-frontend`** — the general house front-end concern.

A project normally picks the **one** that matches its priority; they *can* be composed
together, but they are offered as choices rather than a stack. Compose whichever you
choose alongside a language source (e.g. `throughline-typescript`) so a project's
front-end code is grounded in both at once.

## Status

<!-- tl:count type == 'user_requirement' -->
8
<!-- tl:end --> sections and
<!-- tl:count type == 'system_requirement' -->
55
<!-- tl:end --> best-practice rules, published to [`docs/spec.md`](docs/spec.md):

- `INT-0001` — the root intent (why the practices exist), `normative: false`.
- Each best-practice area as a `user_requirement` that `derives_from` the intent.
- Every individual recommendation as a `system_requirement` that `implements` its area,
  carrying the guide reference in `attrs.source_ref`.

The counts above are rendered from the live graph by the `tl:count` directive, so
they cannot drift.

## Editions — dated tags

MDN Web Docs is a living resource. A material revision is cut as a dated tag on this
repo (e.g. `v2026-08`); a consumer pins the ref it wants.

## Composing it

```toml
[[sources]]
namespace = "mdn"
url = "https://github.com/rhodium-org/throughline-frontend-mdn"
ref = "v2026-08"
```

Then reference a rule from your own items:

```yaml
links:
- target: mdn:SR-0001          # MDN Web Docs: use semantic elements for their meaning
  type: satisfies
```

`tl check` in the consuming project composes this source and resolves the reference.
A `tl` older than 3.11.0 reports it as `namespace-unresolved`.

## Local checks

```sh
pip install throughline
tl check --strict     # the graph must stay sound
tl docs --check       # docs/spec.md must match the graph
```

## Provenance

MDN Web Docs is © Mozilla and its contributors, prose licensed CC BY-SA 2.5. See
[NOTICE](NOTICE) and https://developer.mozilla.org/. This repository is Apache-2.0 for
its structure and tooling; the reproduced rule text remains the work of the MDN
community.
