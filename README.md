# dotfiles

My dev environment config. Neovim (kickstart-based) + tmux.

## Prerequisites

```bash
brew install neovim tmux node
```

### Nerd Fonts

Install all Nerd Fonts (for icons in nvim and terminal):

```bash
brew install --cask font-3270-nerd-font font-fira-mono-nerd-font \
  font-inconsolata-go-nerd-font font-inconsolata-lgc-nerd-font \
  font-inconsolata-nerd-font font-monofur-nerd-font \
  font-overpass-nerd-font font-ubuntu-mono-nerd-font \
  font-agave-nerd-font font-arimo-nerd-font \
  font-anonymice-nerd-font font-aurulent-sans-mono-nerd-font \
  font-bigblue-terminal-nerd-font font-bitstream-vera-sans-mono-nerd-font \
  font-blex-mono-nerd-font font-caskaydia-cove-nerd-font \
  font-code-new-roman-nerd-font font-cousine-nerd-font \
  font-daddy-time-mono-nerd-font font-dejavu-sans-mono-nerd-font \
  font-droid-sans-mono-nerd-font font-fantasque-sans-mono-nerd-font \
  font-fira-code-nerd-font font-go-mono-nerd-font \
  font-gohufont-nerd-font font-hack-nerd-font \
  font-hasklug-nerd-font font-heavy-data-nerd-font \
  font-hurmit-nerd-font font-im-writing-nerd-font \
  font-iosevka-nerd-font font-jetbrains-mono-nerd-font \
  font-lekton-nerd-font font-liberation-nerd-font \
  font-meslo-lg-nerd-font font-monoid-nerd-font \
  font-mononoki-nerd-font font-mplus-nerd-font \
  font-noto-nerd-font font-open-dyslexic-nerd-font \
  font-profont-nerd-font font-proggy-clean-tt-nerd-font \
  font-roboto-mono-nerd-font font-sauce-code-pro-nerd-font \
  font-shure-tech-mono-nerd-font font-space-mono-nerd-font \
  font-terminess-ttf-nerd-font font-tinos-nerd-font \
  font-ubuntu-nerd-font font-victor-mono-nerd-font
```

Set a Nerd Font in your terminal app's settings (e.g. **MesloLGS Nerd Font** or **JetBrains Mono Nerd Font**).

## Install

```bash
# Clone the repo
git clone git@github.com:apekshik/dotfiles.git ~/Developer/dotfiles

# Symlink nvim config
ln -sf ~/Developer/dotfiles/nvim ~/.config/nvim

# Symlink tmux config
ln -sf ~/Developer/dotfiles/tmux/.tmux.conf ~/.tmux.conf

# Reload tmux config (if tmux is running)
tmux source-file ~/.tmux.conf
```

Open `nvim` — plugins will auto-install on first launch via lazy.nvim. Run `:MasonUpdate` to pull the latest LSP registry.

## What's included

### Neovim
- **Base**: kickstart.nvim
- **Theme**: tokyonight-night
- **LSP**: lua-language-server, typescript-language-server (via Mason)
- **Plugins**: telescope (fuzzy finder), neo-tree (file tree), treesitter, gitsigns, blink.cmp (autocomplete)
- **Custom keymaps**:
  - `jk` — escape insert mode
  - `]b` / `[b` — next/prev buffer
  - `\` — toggle file tree
  - `Space sf` — find files
  - `Space sg` — grep across files
  - `Space Space` — switch buffers

### tmux
- **Prefix**: `Ctrl-b` (default)
- **Pane navigation**: `prefix + h/j/k/l`
- **Mouse**: enabled
