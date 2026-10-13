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

## Git

### Push the current branch

```bash
git push
```

- Works once the branch is linked to a branch on GitHub.
- The first push of a new branch makes that link: `git push -u origin <branch>`.

### Take a file out of the stage, keeping its changes

```bash
git restore --staged <file>
```

- `--staged` touches only the stage: the file leaves the next commit, and its changes stay.
- Use `.` instead of `<file>` to take everything out of the stage.
- Without `--staged`, `git restore <file>` throws away the changes in the file, with no way back.

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

### Return a new object instead of changing this one

```python
def <method>(self, <param>):
    return <ClassName>(self.<attribute> * <param>)
```

- Calling the class name creates the object; Python has no `new`.
- The calculation runs first, and its result goes to the constructor.
- `self.<attribute>` is only read, so the object the method was called on does not change.
