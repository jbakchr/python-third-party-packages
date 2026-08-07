# Trafilatura

Python library for downloading web pages and extracting clean article content from HTML.

---

## What Is It?

Trafilatura is a web scraping and content extraction library.

Its primary purpose is to extract the meaningful text from a web page while removing things such as:

- Navigation menus
- Sidebars
- Advertisements
- Cookie banners
- Other page clutter

It is especially useful when:

- Building RAG pipelines
- Scraping articles
- Processing blog posts
- Extracting content for LLMs
- Creating datasets from websites

---

## Why I Like It

- Extremely easy to use
- Produces surprisingly clean results
- Handles a lot of HTML complexity for me
- Great for AI and RAG projects
- Supports metadata extraction
- Supports multiple output formats

---

## When I Use It

- RAG experiments
- Building AI tools
- Reading article content from the web
- Processing documentation sites
- Creating datasets
- Quick web scraping projects

---

## Installation

```bash
pip install trafilatura
```

---

## Quick Reference

| Task | Function |
|--------|--------|
| Download webpage | `trafilatura.fetch_url()` |
| Extract article text | `trafilatura.extract()` |
| Extract metadata | `trafilatura.extract(..., with_metadata=True)` |
| Output JSON | `trafilatura.extract(..., output_format="json")` |
| Process existing HTML | `trafilatura.extract(html)` |

---

## Common Examples

### Download a Web Page

```python
import trafilatura

html = trafilatura.fetch_url(
    "https://example.com"
)
```

The downloaded HTML can then be processed using `extract()`.

---

### Extract Article Text

```python
import trafilatura

html = trafilatura.fetch_url(url)

text = trafilatura.extract(html)

print(text)
```

This is the most common workflow I use.

---

### Extract From Existing HTML

```python
import trafilatura

html = """
<html>
    ...
</html>
"""

text = trafilatura.extract(html)
```

Useful when HTML has already been downloaded by another library.

---

### Extract Metadata

```python
import trafilatura

result = trafilatura.extract(
    html,
    with_metadata=True
)

print(result)
```

Can include information such as:

- Title
- Author
- Publication date

when available on the page.

---

### Output JSON

```python
import trafilatura

result = trafilatura.extract(
    html,
    output_format="json"
)

print(result)
```

Useful when extracting structured content.

---

## Useful Patterns

### Pattern: Web Page → Clean Text

```python
import trafilatura

html = trafilatura.fetch_url(url)

if html:
    text = trafilatura.extract(html)
```

This is the workflow I use most often.

---

### Pattern: Extract Content for RAG

```python
import trafilatura

html = trafilatura.fetch_url(url)

content = trafilatura.extract(
    html,
    include_links=False,
    include_comments=False
)
```

The extracted text can then be chunked and embedded for a RAG system.

---

## Alternatives

### BeautifulSoup

Pros:

- Extremely flexible
- Industry standard
- Works on almost any HTML

Cons:

- Requires more manual parsing
- More code required

---

### Newspaper3k

Pros:

- Designed for article extraction
- Includes metadata support

Cons:

- Less actively discussed in modern scraping workflows
- Less flexible

---

## Documentation

### Official Documentation

- https://trafilatura.readthedocs.io/

### Source Code

- https://github.com/adbar/trafilatura

---

## Personal Notes

### Notes

- Often my first choice when I need article content from a website.
- Usually produces cleaner content than manually parsing HTML.
- Particularly useful for AI projects where I only need the actual text.
- Works very well together with embeddings and vector databases.

### Things I Want to Remember

- Use `fetch_url()` when Trafilatura should handle downloading.
- Use `extract()` when HTML is already available.
- Start simple before exploring additional extraction options.

---

## Lessons Learned

### YYYY-MM-DD

Trafilatura is often a better first solution than writing custom BeautifulSoup extraction logic.

Try Trafilatura first and only fall back to custom parsing when the extracted content is not sufficient.

---

## Related How-Tos

- Scrape Web Page
- Extract Article Content
- Build RAG Knowledge Base

---

## Related Packages

- BeautifulSoup
- Requests
- ChromaDB
- Pydantic
- LangChain

---

## Changelog

### YYYY-MM-DD

- Created package page.