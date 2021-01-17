[< back to contents](./readme.md)

# About SSH

Using the SSH protocol, you can connect and authenticate to remote servers and services. With SSH keys, you can connect to GitHub without supplying your username and personal access token at each visit.

## Checking existing ssh keys

Before you generate an SSH key, you can check to see if you have any existing SSH keys with following command:
```bash-
ls -al ~/.ssh
```
It shows list ssh keys if exist.

## Generating new ssh key

Generate key by enter command:
```bash-
ssh-keygen -t ed25519 -C "your_email@example.com"
```
then enter name for your ssh key and passphrase for protection of unautorized usage. If keep passphrase empty key will be without protection.

## Adding your SSH key to the ssh-agent

Now it is necessary to start ssh-agent with command:
```
eval `ssh-agent -s`
```
You can use auto-launching the ssh-agent by copying following lines and paste them into your ~/.bashrc or ~/.profile file. Agent will be started every time when you open Git bash.

```bash
env=~/.ssh/agent.env

agent_load_env () { test -f "$env" && . "$env" >| /dev/null ; }

agent_start () {
    (umask 077; ssh-agent >| "$env")
    . "$env" >| /dev/null ; }

agent_load_env

# agent_run_state: 0=agent running w/ key; 1=agent w/o key; 2= agent not running
agent_run_state=$(ssh-add -l >| /dev/null 2>&1; echo $?)

if [ ! "$SSH_AUTH_SOCK" ] || [ $agent_run_state = 2 ]; then
    agent_start
    ssh-add
elif [ "$SSH_AUTH_SOCK" ] && [ $agent_run_state = 1 ]; then
    ssh-add
fi

unset env
```
Checking key using ssh-agent:

```bash
ssh-add -l
```

Next you should do is set up public ssh-key to github.com

[<Previous](./push.md) ... [Next>](./public_ssh_key.md)