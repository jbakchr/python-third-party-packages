# Roadmap

This project is intended to grow organically over time.

The goal is not to document every Python package that exists.

Instead, the goal is to document Python third-party packages that I have personally used, enjoyed using, or found useful for solving real-world problems.

When deciding what to document next, preference should be given to packages that:

- I use frequently
- I often forget how to use
- Have useful patterns worth remembering
- Have solved real problems for me
- Would benefit Future Me

---

# Current Status

## Existing Package Pages

### Validation

- Validators

### HTTP

- Requests

### CLI

- Typer

### Web Scraping

- Trafilatura

---

# Phase 1: Frequently Used Packages

Packages I have either used many times or expect to use regularly.

## CLI

- Rich
- Textual

## HTTP

- HTTPX

## Web Scraping

- BeautifulSoup

## Data Validation

- Pydantic

## ORM / Database

- SQLModel

## Automation

- Selenium
- webdriver-manager

## Utilities

- Pydash
- Humanize
- Faker

---

# Phase 2: AI Development

Packages related to AI, LLMs, embeddings, RAG, and vector databases.

## LLMs

- OpenAI
- Ollama
- LiteLLM

## Vector Databases

- ChromaDB

## AI Frameworks

- LangChain
- LlamaIndex

## Embeddings

- Sentence Transformers

## RAG Utilities

- Unstructured

---

# Phase 3: API Development

Packages commonly used when building services and APIs.

## Frameworks

- FastAPI

## Data Validation

- Pydantic

## Database

- SQLModel
- SQLAlchemy

## Authentication

- Passlib
- python-jose

## Testing

- Pytest

---

# Phase 4: Data Analysis

Packages useful when processing and analyzing data.

## Core Data Analysis

- Pandas

## Numerical Computing

- NumPy

## Visualization

- Matplotlib
- Seaborn
- Plotly

---

# Phase 5: Developer Experience

Packages that improve the developer experience.

## Terminal UI

- Rich
- Textual

## Configuration

- python-dotenv

## Logging

- Loguru

## Progress Bars

- tqdm

---

# Phase 6: File Processing

Packages for working with files and documents.

## Excel

- OpenPyXL

## PDF

- PyPDF2
- pypdf

## Word Documents

- python-docx

## Images

- Pillow

---

# Medium Package Candidates

These packages should initially be documented using a single page.

If the page grows large enough, additional pages can be created later.

Examples:

- Requests
- Trafilatura
- Rich
- BeautifulSoup
- SQLModel
- Pydantic

Potential structure:

```text
package/
└── index.md
```

Later:

```text
package/
├── index.md
├── topic-a.md
└── topic-b.md
```

---

# Large Package Candidates

These packages will likely require multiple pages.

Examples:

- FastAPI
- Pandas
- SQLAlchemy
- Textual
- LangChain

Potential structure:

```text
package/
├── index.md
├── section/
│   └── index.md
└── ...
```

---

# Future How-To Pages

Task-oriented documentation.

Unlike package pages, these pages focus on solving problems.

## HTTP

- Call REST API
- Download File From URL
- Authenticate Against API

## CLI

- Build CLI Tool
- Add Progress Bar
- Add Interactive Prompt

## Web Scraping

- Scrape Web Page
- Extract Article Content
- Download Images From Website

## AI

- Build Simple RAG System
- Generate Embeddings
- Query ChromaDB
- Run Local LLM With Ollama

## Database

- Create SQLite Database
- Perform CRUD Operations
- Model Database Relationships

---

# Future Category Pages

Potential category pages.

## APIs

- FastAPI
- Requests
- HTTPX

## CLI

- Typer
- Rich
- Textual

## Validation

- Validators
- Pydantic

## ORM

- SQLModel
- SQLAlchemy

## AI

- Ollama
- ChromaDB
- LangChain
- LlamaIndex

## Web Scraping

- Trafilatura
- BeautifulSoup
- Selenium

---

# GitHub Pages

Future goal:

Transform this repository into a GitHub Pages site.

Potential navigation:

```text
Home

Categories
Packages
How-Tos
```

Possible future improvements:

- Navigation sidebar
- Search functionality
- Package cross-linking
- Category pages
- Related package suggestions
- Recently added pages

---

# Guiding Principle

This repository is not intended to become a copy of official documentation.

Every page should focus on:

- What the package does
- Why I like it
- When I use it
- Common examples
- Useful patterns
- Personal notes
- Lessons learned

If Future Me can quickly solve a problem using the information on a page, then the page has achieved its purpose.