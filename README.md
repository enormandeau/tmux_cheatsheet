# tmux_cheatsheet

Useful tmux infos, commands and config

## Why tmux?

tmux plays the same role as screen, only better. screen is dead, long live tmux!

## Installing

Download tmux from its [homepage](https://tmux.github.io/), deflate the archive and follow the installation instructions. Basically, it is a simple:

```bash
./configure
make
sudo make install
```

If you want to use tmux on a server where you do not have administration rights, it is probably easier to ask the system admin to install the latest version for you.

## Configuration

tmux is pretty configurable and a few additions make it much more usable. Please find the file `tmux.conf` in this repository. It is a minimal configuration that improves functionality. Copy it to your home folder as `.tmux.conf` (do not forget the dot (`.`) before the name.

**NOTE:** The following examples will suppose that you have installed the config file.

## Starting a session

- Basic session: `tmux`
- Nammed session (better): `tmux new -s <session-name>`

## Quitting the session

Because of our configuration, you won't be able to exit tmux using `Ctrl-D`, which is a good thing because you can otherwise quit multiple windows and sessions by mistake if you hold `Ctrl-D` too long. To quit, type:

```bash
logout
```

## Why reinvent the wheel?

The two following cheatsheets are absolutely great, so I let them deal with the details of how to use tmux. I also add a link to the official manual.

- [tmux shortcuts & cheatsheet](https://gist.github.com/MohamedAlaa/2961058)
- [Tmux Cheat Sheet & Quick Reference](https://tmuxcheatsheet.com/)
- [Official tmux manual](http://man.openbsd.org/OpenBSD-current/man1/tmux.1)

## Suggested aliases

Some aliases to add to your `~/.bashrc/` or equivalent file:

- `alias ta='tmux attach'`
- `alias tn='tmux new -s'`
- `alias lo='logout'`

You can then use `ta` to attach to tmux and `tn <session-name>` to create a new session.
