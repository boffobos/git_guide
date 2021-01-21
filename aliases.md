[< back to contents](./readme.md)

# Aliases

Aliases allow set up chortcuts for git commands and simplify its input. There are some examples of setting up aliases:

```bash
git config --global alias.hist "log --pretty=format:'%h %ad | %s%d [%an]' --graph --date=short"
```
```bash
git config --global alias.st status
```
```bash
git config --global alias.co checkout
```
```bash
git config --global alias.ci commit
```
```bash
git config --global alias.br branch
```
```bash
git config --global alias.type 'cat-file -t'
```
```bash
git config --global alias.dump 'cat-file -p'
```
[<Previous](./fetch.md) ... [Next>](.)