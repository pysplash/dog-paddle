# Rye notes

---

## Remove pyenv and use rye

---

## Set up a learning system

### Set a global python
rye config --set-bool behavior.global-python=true

### Set up some global tools (science prototyping)

```
rye tools install ipython
rye tools install jupyter
rye tools install notebook
```

### Check which global tools are installed
```
rye tools list --include-scripts --include-version
# or
rye tools list -v -s
```
### Run a script like ipython
```
rye run ipython
# or 
ipython
```
---

## Start a new project (which I want to share)
```
rye init
```

---

## Start a virtual project (just using stuff not pypi package)

```
rye init --virtual
rye add mkdocs
rye sync
rye run mkdocs
```
---

## Nice to have

### Install completion for rye

# Make sure ~/.zfunc is added to fpath, before compinit.
rye self completion -s zsh > ~/.zfunc/_rye

Then add to `.zshrc` before init modules (if using zimfw):  `fpath=(~/.zsh $fpath)`

---

## Things to check

- conda
- mamba
- pixi

---

## Questions

- If you update `rye self update`, do you need to do a `rye sync` when you enter a project again?
On mac, can I ditch homebrew to install Python?
