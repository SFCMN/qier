# qgit &middot; [![qgit version](https://img.shields.io/badge/version-2.1.1-blue)](https://github.com/SFCMN/qier/tree/main/scripts/qgit)

Easily execute the same operation on multiple git remotes. (**Currently only support Mac OS**)

# Getting Started

```
usage: qgit [--qhelp] [-qh] [help]
            <git-command> [<args>]

You can run the 'qgit' to get the help information, or you can also use other commands or options.

These are common qgit commands used in various situations:
notes: the 'q' stands for the abbreviation of qgit, just to distinguish it from the commands of git itself

      -qh            ↓
      --qhelp        ↓
      qhelp          Get usage and help information of qgit
      qinit          Generate a configuration file in which you need to add all the remote names you want to use
                     notes: if the configuration file already exists, this command will not do anything;
                            otherwise, it will generate a new configuration file and put into some comment information

Using git subcommands, when multiple remotes are involved, the qgit will execute the same git operation on each remote in turn
notes: when the executed git subcommand involves the remote name, you can use '-' instead. When it's actually executed, '-' will be replaced with the real remote name

Example:
 【qgit push - master】 equals 【git push <remote1> master && git push <remote2> master】
```

# Install

You can run the following command, which contains all the necessary steps.<br/>
notes: currently `qgit` only supports **Mac OS**<br/>
notes: **`qgit qinit` will be executed automatically after installation**

```bash
curl -LJO https://raw.githubusercontent.com/SFCMN/qier/main/scripts/qgit/qgit && chmod +x ./qgit && mv ./qgit /usr/local/bin/qgit && qgit qinit
```

**Chinese users can use the following command to install:**

```bash
curl -LJO https://gitee.com/sfcmn/qier/raw/main/scripts/qgit/qgit && chmod +x ./qgit && mv ./qgit /usr/local/bin/qgit && qgit qinit
```
