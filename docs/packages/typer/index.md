# Typer

Python library for building command-line applications with minimal code and excellent developer experience.

---

## What Is It?

Typer is a framework for creating command-line interfaces (CLIs).

It is built on top of Click and uses Python type hints to automatically generate:

- Command-line arguments
- Options
- Help text
- Input validation
- Documentation

---

## Why I Like It

- Extremely easy to learn
- Type hints drive much of the functionality
- Excellent help output
- Very little boilerplate
- Great developer experience
- Works well for both small and large CLI tools

---

## When I Use It

- CLI tools
- Automation scripts
- Developer utilities
- Internal tools
- AI tooling
- Personal projects

---

## Installation

```bash
pip install typer
```

---

## Quick Reference

| Task | Example |
|--------|--------|
| Create app | `app = typer.Typer()` |
| Add command | `@app.command()` |
| Add argument | Function parameter |
| Add option | `typer.Option()` |
| Print text | `typer.echo()` |
| Exit application | `raise typer.Exit()` |
| Ask for input | `typer.prompt()` |
| Confirm action | `typer.confirm()` |

---

## Common Examples

### Create a Simple CLI

```python
import typer

app = typer.Typer()


@app.command()
def hello():
    print("Hello World")


if __name__ == "__main__":
    app()
```

Run:

```bash
python app.py hello
```

---

### Command With Arguments

```python
import typer

app = typer.Typer()


@app.command()
def greet(name: str):
    print(f"Hello {name}")


if __name__ == "__main__":
    app()
```

Run:

```bash
python app.py greet Jonas
```

---

### Command With Options

```python
import typer

app = typer.Typer()


@app.command()
def greet(
    name: str,
    uppercase: bool = typer.Option(
        False,
        "--uppercase"
    )
):
    message = f"Hello {name}"

    if uppercase:
        message = message.upper()

    print(message)


if __name__ == "__main__":
    app()
```

Run:

```bash
python app.py greet Jonas --uppercase
```

---

### Prompt User For Input

```python
import typer

name = typer.prompt(
    "What is your name?"
)

print(name)
```

---

### Confirm Action

```python
import typer

if typer.confirm("Continue?"):
    print("Continuing...")
else:
    raise typer.Exit()
```

---

## Useful Patterns

### Pattern: Multi-Command Application

```python
import typer

app = typer.Typer()


@app.command()
def create():
    print("Creating...")


@app.command()
def delete():
    print("Deleting...")


@app.command()
def list():
    print("Listing...")


if __name__ == "__main__":
    app()
```

Useful for larger CLI applications.

---

### Pattern: Main CLI + Domain Commands

Project structure:

```text
commands/
├── jobs.py
├── resume.py
└── applications.py
```

Example:

```python
app = typer.Typer()

app.add_typer(
    jobs.app,
    name="jobs"
)

app.add_typer(
    resume.app,
    name="resume"
)
```

Useful when a project grows beyond a few commands.

---

## Alternatives

### argparse

Pros:

- Included with Python
- No external dependency

Cons:

- More verbose
- Less developer-friendly

---

### Click

Pros:

- Extremely mature
- Powerful

Cons:

- Slightly more boilerplate
- Less type-hint focused

---

## Documentation

### Official Documentation

- https://typer.tiangolo.com/

### Source Code

- [Typer GitHub Repository](httpsr

---

## Personal Notes

### Notes

- My preferred CLI framework.
- Usually my first choice for new Python command-line tools.
- Simple enough for small scripts.
- Powerful enough for larger applications.

### Things I Want to Remember

- Start with a single file and one command.
- Use subcommands when the application grows.
- Use type hints everywhere.
- Use Rich together with Typer for better output.

---

## Lessons Learned

### YYYY-MM-DD

Typer makes it easy to start small and then grow a CLI into a larger application without major refactoring.

### YYYY-MM-DD

Using `app.add_typer()` helps keep larger CLI codebases organized.

---

## Related How-Tos

- Create CLI Tool
- Build Multi-Command CLI
- Create Interactive Terminal Application

---

## Related Packages

- Rich
- Textual
- Click
- Pydantic

---

## Changelog

### YYYY-MM-DD

- Created package page.