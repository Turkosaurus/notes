# bash

## git

### Pull
Retrieves all changes and change history from repo
- `git fetch` (fetches changes but does not apply; less common)
- `git pull` (fetches and applies changes; more common)

### Push
Sends all changes and change history to repo
- Stage all files in the current directory: `git add .`
- Commit with message: `git commit -m "message detailing changes"`
- Push commit(s) to branch: `git push [optional_origin]`

## ls
- `-a` all (include hidden)
- `-l` long (details)
- `-t` time (last modified)
- `-S` extension
- `-v` version sort
- `-S` size sort
- `-R` recursively
- `-1` ?

## psql
- `\dt` display public tables
- `\d [table]` display table schema

## venv
Virtual Environments ([docs](https://docs.python.org/3/library/venv.html))

### Create a new `venv` in the target directory
- `python3 -m venv /path/to/new/virtual/env`
- `python3 -m venv .venv` (common)
- `python3 -m venv venv` (example)

### Activate virtual environment
- `source venv/bin/activate`
- the `(venv)` preceeding shell prompt indicates that the virtural envioronment is active

### Deactivate the virtual environment
- `deactivate`


## vscode
#### Shortcuts
| Function | Key Combination |
| --- | --- |
| Fold All | `ctl + k` `ctl + 0` |


## wsl
Windows Subsystem for Linux
#### flags
- `-l` list distros
- `-d` run distros
