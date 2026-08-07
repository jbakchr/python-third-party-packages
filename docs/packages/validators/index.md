# Validators

A lightweight Python library for validating common values such as URLs, email addresses, IP addresses, domains, slugs, UUIDs, and more.

---

## What Is It?

Validators provides a simple set of functions for checking whether a value is valid.

Instead of writing custom validation logic yourself, you can often use a built-in validator.

Examples of things it can validate:

- URLs
- Email addresses
- IP addresses
- Domain names
- UUIDs
- Slugs
- SHA hashes

---

## Why I Like It

- Extremely simple API
- Lightweight dependency
- Easy to remember
- No configuration required
- Great for quick validation tasks
- Perfect for scripts and CLI tools

---

## When I Use It

- CLI applications
- Input validation
- Configuration validation
- Utility scripts
- Sanity-checking user input before processing

---

## Installation

```bash
pip install validators
```

---

## Common Examples

### Validate URL

```python
import validators

validators.url("https://www.google.com")
```

Returns:

```python
True
```

Invalid URL:

```python
validators.url("not-a-url")
```

Returns:

```python
ValidationError(...)
```

---

### Validate Email

```python
import validators

validators.email("john@example.com")
```

Returns:

```python
True
```

Invalid email:

```python
validators.email("john")
```

Returns:

```python
ValidationError(...)
```

---

### Validate IPv4 Address

```python
import validators

validators.ipv4("127.0.0.1")
```

Returns:

```python
True
```

---

### Validate IPv6 Address

```python
import validators

validators.ipv6("2001:db8::1")
```

Returns:

```python
True
```

---

### Validate Domain Name

```python
import validators

validators.domain("example.com")
```

Returns:

```python
True
```

---

### Validate Slug

```python
import validators

validators.slug("my-awesome-post")
```

Returns:

```python
True
```

---

### Validate UUID

```python
import validators

validators.uuid(
    "550e8400-e29b-41d4-a716-446655440000"
)
```

Returns:

```python
True
```

---

## Useful Pattern

I often use a helper function like this:

```python
import validators

def validate_url(url: str) -> bool:
    return bool(validators.url(url))
```

Usage:

```python
if not validate_url(url):
    raise ValueError("Invalid URL")
```

---

## Alternatives

### Pydantic

Good when using data models and type validation.

Pros:

- Rich validation features
- Excellent FastAPI integration

Cons:

- More setup required
- Heavier dependency

---

### Cerberus

Validation framework for dictionaries and structured data.

Pros:

- Flexible schemas

Cons:

- More complex than Validators

---

## Documentation

- Official project:
  https://github.com/python-validators/validators

- Documentation:
  https://python-validators.github.io/validators/

---

## Personal Notes

### Notes

- Great for quickly validating URLs in CLI tools.
- Useful when reading configuration files.
- Often simpler than writing regular expressions.
- Good companion to Typer applications.

### Lessons Learned

#### 2026-08-07

Created the first package page for the Python Third Party Packages project.

This package is a good example of a "small package":

- One page is enough.
- No need for additional sub-pages.
- Most useful features can be shown with a few examples.

This page serves as a template for future package pages.