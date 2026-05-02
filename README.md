# mac.dot

Combined macOS dotfiles and configuration.

## Content

- **Git config** — `.gitconfig` (from dotfiles repo)
- **Window manager** — `.config/aerospace/aerospace.toml`
- **Terminal** — `.config/kitty/kitty.conf` (macOS-specific overrides)
- **SSH** — `.ssh/config`

## Setup

```bash
git clone --bare git@github.com:stivce/mac.dot.git $HOME/.macdot
git --git-dir=$HOME/.macdot --work-tree=$HOME checkout
```

Add to your shell profile:

```bash
alias macdot='git --git-dir=$HOME/.macdot --work-tree=$HOME'
macdot config status.showUntrackedFiles no
```

## Usage

```bash
macdot add ~/.gitconfig
macdot add ~/.config/aerospace/aerospace.toml
macdot commit -m "update config"
macdot push
```
