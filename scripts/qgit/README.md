# qgit &middot; [![qgit version](https://img.shields.io/badge/version-2.0-blue)](https://github.com/SFCMN/qier/tree/main/scripts/qgit)

Easily execute the same operation on multiple git remotes.

# Getting Started

```
usage: qgit [--qhelp] [-qh] [help]
            <git-command> [<args>]

Using git subcommands, when multiple remotes are involved, the qgit will execute the same git operation on each remote in turn
notes: when the executed git subcommand involves the remote name, you can use '-' instead. When it's actually executed, '-' will be replaced with the real remote name

Example:
【qgit push - master】 equals 【git push <remote1> master && git push <remote2> master】

There are some options or subcommands to help get the help information of qgit
notes: the 'q' stands for the abbreviation of qgit, just to distinguish it from the help of git itself
       -qh            ↓
       --qhelp        ↓
       qhelp          Get usage and help information of qgit
       qinit          Generate a configuration file in which you need to add all the remote names you want to use
                      notes: if the configuration file already exists, this command will not do anything;
                      otherwise, it will generate a new configuration file and put into some comment information
```

# Install

You can run the following command, which contains all the necessary steps.<br/>
notes: currently `qgit` only supports **Mac OS**

```bash
curl -LJO https://raw.githubusercontent.com/SFCMN/qier/main/scripts/qgit/qgit && chmod +x ./qgit && mv ./qgit /usr/local/bin/qgit
```
