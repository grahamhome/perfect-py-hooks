# Git Hooks for Python
This repo contains useful Git hooks for Python development. Hooks may be found in [hooks/pre-commits](hooks/pre-commits).
## Contents
- [hooks/pre-commits/black](hooks/pre-commits/black): Runs [Black](https://pypi.org/project/black/) on all .py files included in each commit.
- [hooks/pre-commits/isort](hooks/pre-commits/isort): Runs [isort](https://pypi.org/project/isort/) on all .py files included in each commit.
- [hooks/pre-commit](hooks/pre-commit): Executes all pre-commit hooks whenever `git commit` is run.
## Installation
### Global
If you would like to use these hooks in all your Git repos:
1. Clone this repo (for example purposes, we will clone it to `~/projects/py-hooks`)
1. Execute the following commands one time only:
	1. `git config --global init.templatedir '~/.git-templates'`
	1. `cp -a ~/projects/py-hooks/. ~/.git-templates`
	1. `rm ~/.git-templates/README.md`
1. All Git repos created will now include the Python pre-commit hooks by default.
	1. To add the hooks to an existing Git repo, run `git init` inside the repo.
### Per-Project
If you would like to use these hooks in a specific repo only:

For example purposes, we will add them to the repo `~/projects/py-project/`
1. Clone this repo (for example purposes, we will clone it to `~/projects/py-hooks`)
1. Execute the following commands one time only:
	1. `cp -a ~/projects/py-hooks/. ~/projects/.git/`
## Usage
Once hooks are installed globally or for a specific project, simply add and commit project files as you normally would. Committed Python (`.py`) files will automatically be formatted with Black and isort to ensure all your code is clean and PEP8 compliant!

## Note
You will need to ensure that the Black and isort Python packages are installed in your Python environment in order for these hooks to work. Simply install them with your package manager of choice e.g. `pip install black` and `pip install isort`.

## Bonus: Git Shortcuts
If you use Git from the command line, these aliases will make your life easier. Simply add them to your `~/.bashrc` file and memorize them for daily use.
```commandline
# Handy Git shortcuts
alias gpl="git pull"
alias gst="git status"
alias gco="git checkout"
alias gcb="git checkout -b"
alias gaa="git add ."
alias gad="git add"
alias gct="git commit"
alias gcm="git commit -m"
alias gca="git commit -am"
alias gps="git push"
alias gdf="git diff"
```
