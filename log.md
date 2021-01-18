[< back to contents](./readme.md)

# git log

**git log** - Show the commit logs

There are a lot of output options. Here is one of them:

```bash-
git log --pretty=oneline --max-count=6
```

Some convenient view of output:

```bash
git log --pretty=format:"%h %ad | %s%d [%an]" --graph --date=short
```
where is:   
* `--pretty=format:"..."` - defines output format
* `%h` - abbreviated commit hash
* `%d` - ref names
* `%ad` - author date
* `%an` - author name
* `%s` - subject
* `--graph` - Draw a text-based graphical representation of the commit history on the left hand side of the output
* `--date=short` - shows only the date, but not the time, in `YYYY-MM-DD` format

For more information follow [link](https://git-scm.com/docs/git-log)

[<Previous](./status.md) ... [Next>]()