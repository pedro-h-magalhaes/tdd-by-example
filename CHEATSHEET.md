# Cheat sheet

Commands and code I looked up while working through the book.

## Terminal

### Write text into a file, replacing what it had

```bash
echo "text" > file
```

Creates `file` if it does not exist.

### Add a line at the end of a file, keeping what it had

```bash
echo "text" >> file
```

### Show what is inside a file

```bash
cat file
```

## Python

### Create a virtual environment

```bash
python3 -m venv <folder>
```

- `python3 -m venv` creates the environment, using the `venv` module that comes with Python.
- `<folder>` is where the environment goes.
  - The usual choice is `.venv`, run from the project folder: `python3 -m venv .venv`.
  - In this repository it is `python/.venv`.

### Save the installed packages to `requirements.txt`

```bash
pip freeze > <file>
```

- `pip freeze` lists every package installed in the active virtual environment, as `name==version`.
- `> <file>` sends that list to a file instead of the screen.
  - The usual file is `requirements.txt`, in the project folder.
