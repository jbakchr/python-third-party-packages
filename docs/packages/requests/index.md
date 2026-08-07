# Requests

Python library for making HTTP requests.

---

## What Is It?

Requests is one of the most popular Python libraries for interacting with HTTP APIs and websites.

It provides a simple and Pythonic way to:

- Send HTTP requests
- Consume REST APIs
- Download files
- Upload files
- Send JSON data
- Work with authentication
- Handle HTTP responses

---

## Why I Like It

- Extremely easy to use
- Excellent documentation
- Simple API
- Great for scripts and automation
- Perfect default choice for HTTP requests
- Much cleaner than using Python's built-in HTTP libraries

---

## When I Use It

- Calling REST APIs
- Downloading files
- Web scraping
- Automation scripts
- Integrations between systems
- Quick experiments and prototypes

---

## Installation

```bash
pip install requests
```

---

## Quick Reference

| Task | Function |
|--------|--------|
| GET request | `requests.get()` |
| POST request | `requests.post()` |
| PUT request | `requests.put()` |
| DELETE request | `requests.delete()` |
| Send JSON | `json=` |
| Custom headers | `headers=` |
| Query parameters | `params=` |
| File download | `response.content` |
| Raise exception on error | `response.raise_for_status()` |
| Set timeout | `timeout=` |

---

## Common Examples

### Simple GET Request

```python
import requests

response = requests.get(
    "https://api.github.com"
)

print(response.status_code)
print(response.text)
```

Explanation:

- Sends a GET request
- Returns a Response object

---

### GET Request with Query Parameters

```python
import requests

response = requests.get(
    "https://api.example.com/users",
    params={
        "page": 1,
        "limit": 10
    }
)
```

Resulting URL:

```text
https://api.example.com/users?page=1&limit=10
```

---

### POST JSON Data

```python
import requests

response = requests.post(
    "https://api.example.com/users",
    json={
        "name": "Jonas",
        "email": "jonas@example.com"
    }
)
```

Using `json=` automatically:

- Serializes JSON
- Sets the correct Content-Type header

---

### Custom Headers

```python
import requests

response = requests.get(
    "https://api.example.com",
    headers={
        "Authorization": "Bearer TOKEN"
    }
)
```

Useful for authenticated APIs.

---

### Read JSON Response

```python
import requests

response = requests.get(url)

data = response.json()

print(data)
```

One of the most common patterns when consuming REST APIs.

---

### Error Handling

```python
import requests

response = requests.get(url)

response.raise_for_status()
```

Recommended practice.

Raises an exception if:

- 400 Bad Request
- 401 Unauthorized
- 403 Forbidden
- 404 Not Found
- 500 Internal Server Error

etc.

---

### Set a Timeout

```python
import requests

response = requests.get(
    url,
    timeout=10
)
```

Never assume external services respond immediately.

---

### Download a File

```python
import requests

response = requests.get(url)

with open(
    "file.pdf",
    "wb"
) as file:
    file.write(response.content)
```

Useful for:

- PDFs
- Images
- ZIP files
- Documents

---

## Useful Patterns

### Pattern: Safe API Request

```python
import requests

response = requests.get(
    url,
    timeout=10
)

response.raise_for_status()

data = response.json()
```

This is my default pattern when consuming APIs.

---

### Pattern: Authenticated API Request

```python
import requests

headers = {
    "Authorization": f"Bearer {token}"
}

response = requests.get(
    url,
    headers=headers
)
```

Useful for:

- GitHub API
- Azure APIs
- OpenAI APIs
- Internal APIs

---

### Pattern: Reusable Session

```python
import requests

session = requests.Session()

session.headers.update({
    "Authorization": f"Bearer {token}"
})

response = session.get(url)
```

Useful when making many requests.

---

## Alternatives

### HTTPX

Pros:

- Modern API
- Async support
- Similar interface to Requests

Cons:

- Slightly more complexity

When I would choose it:

- Async applications
- FastAPI applications

---

### aiohttp

Pros:

- Fully asynchronous
- High performance

Cons:

- Different API
- More complexity

When I would choose it:

- Massive numbers of requests
- Async web applications

---

## Documentation

### Official Documentation

- [Requests Documentationuests.org/en/latest/

### Source Code

- [Requests GitHub Repository](https://github.com/psfotes

### Notes

- Usually my first choice for HTTP requests.
- Excellent for scripts, automation, and integrations.
- Easy to read and understand.
- Great companion to BeautifulSoup and Trafilatura.

### Things I Want to Remember

- Always use `timeout=`.
- Prefer `response.raise_for_status()`.
- Use `json=` instead of manually serializing JSON.
- Use `Session()` when making many requests.

---

## Lessons Learned

### YYYY-MM-DD

Always set a timeout.

Eventually every application makes a request to a service that is slow or unavailable.

---

### YYYY-MM-DD

Use `raise_for_status()` early.

Failed requests should fail fast rather than producing confusing errors later in the code.

---

## Related How-Tos

- Call REST API
- Download File from URL
- Scrape Web Page
- Consume JSON API

---

## Related Packages

- BeautifulSoup
- Trafilatura
- HTTPX
- aiohttp
- FastAPI

---

## Changelog

### YYYY-MM-DD

- Created package page.