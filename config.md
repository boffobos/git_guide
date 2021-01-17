[< back to contents](./readme.md)

# git config

**git config *[options]*** - Get and set repository or global options

There is a lot of options so if you would like to get detailed informations follow the [link](https://git-scm.com/docs/git-config#_options)

**git config *--list*** - check all your configuration settings

For initial configure git enter the following command:

```bash
git config --global user.name "John Doe"
git config --global user.email johndoe@example.com
```
Also you can set up enternal editor for git by command:

```bash
git config --global core.editor "'C:/Program Files/Notepad++/notepad++.exe' -multiInst -notabbar -nosession -noPlugin"
```
At the begining you shoul install some editor (example [Notepad++](https://notepad-plus-plus.org/))

To get know where is stored particular configuration enter next command:
```
git config --show-origin user.email
```

[<Previous](./public_ssh_key.md) ... [Next>](.)