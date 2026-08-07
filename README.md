# Python Third Party Packages

A personal knowledge base of Python third-party packages I've used and enjoyed using.

The goal of this project is not to replace official documentation, but to provide practical examples, notes, lessons learned, and quick references that help me remember which package solves a problem and how to use it.

Over time this repository should become a searchable collection of package documentation, cheat sheets, examples, and how-to guides.

---

## Why This Project Exists

After years of writing Python code, I've used many excellent third-party packages.

The problem isn't remembering that a package exists.

The problem is remembering:

- Which package solved a specific problem?
- How did I use it?
- What were the most useful functions?
- Why did I choose it over alternatives?
- What lessons did I learn while using it?

This repository is my attempt to capture that knowledge.

---

## Goals

- Document useful Python third-party packages.
- Capture practical examples.
- Record personal notes and lessons learned.
- Create quick reference pages.
- Build a searchable knowledge base.
- Reduce time spent re-reading documentation.

---

## Repository Structure

```text
docs/
├── categories/
├── howtos/
├── packages/
└── _templates/
```

### Categories

Categories help discover packages by problem domain.

Examples:

```text
categories/
├── api.md
├── cli.md
├── validation.md
└── orm.md
```

Example questions:

- "I need a CLI package."
- "I need validation functionality."
- "I need a package for HTTP requests."

---

### Packages

Package pages document individual packages.

Examples:

```text
packages/
├── validators/
│   └── index.md
├── requests/
│   └── index.md
├── typer/
│   └── index.md
└── trafilatura/
    └── index.md
```

Package pages contain:

- What the package is
- Why I like it
- When I use it
- Common examples
- Useful patterns
- Alternatives
- Personal notes
- Lessons learned

---

### How-Tos

How-to pages are task-oriented.

Examples:

```text
howtos/
├── call-rest-api.md
├── validate-email.md
├── scrape-web-page.md
└── create-cli-tool.md
```

A how-to may reference multiple packages.

Example:

```text
How To: Scrape Web Page

Uses:

- requests
- trafilatura
- beautifulsoup
```

---

### Templates

Templates help keep documentation consistent.

Examples:

```text
_templates/
├── package-index.md
├── medium-package-index.md
└── large-package-index.md
```

---

## Package Types

### Small Packages

Examples:

- validators
- humanize
- pydash
- python-slugify

Structure:

```text
package/
└── index.md
```

Typically documented on a single page.

---

### Medium Packages

Examples:

- requests
- trafilatura
- rich
- beautifulsoup

Structure:

```text
package/
└── index.md
```

May later expand into additional pages if needed.

---

### Large Packages

Examples:

- fastapi
- pandas
- sqlalchemy
- textual

Structure:

```text
package/
├── index.md
├── section/
│   └── index.md
└── ...
```

Large packages are organized into multiple sections and pages.

---

## Current Packages

### Validation

- Validators

### HTTP

- Requests

### Web Scraping

- Trafilatura

### CLI

- Typer

---

## Documentation Philosophy

This repository is intentionally opinionated.

The focus is not on documenting every feature.

Instead, each package page should answer the questions:

- What does this package do?
- Why would I use it?
- What are the most common things I do with it?
- What are the important examples I want to remember?
- What lessons have I learned?

If a page helps Future Me solve a problem quickly, it has achieved its purpose.

---

## Future Ideas

- GitHub Pages site
- Searchable package catalog
- Category pages
- Project examples
- More how-to guides
- Cross-linking between packages and how-tos
- Personal package recommendations

---

## License

This project is primarily a personal knowledge base, but if it helps other Python developers remember useful packages, that's a bonus.