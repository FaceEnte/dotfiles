# Dotfiles with GNU Stow

This repo contains my personal dotfiles, managed using [GNU Stow](https://www.gnu.org/software/stow/).

## Getting started

### 1. Clone the repo

```bash
git clone https://github.com/yourusername/dotfiles.git ~/dotfiles
cd ~/dotfiles
```

### 2. Install GNU Stow

#### On Linux (Arch)

```bash
sudo pacman -Syu
sudo pacman -S stow
```

#### On macOS (with Homebrew)

```bash
brew install stow
```

## Using Stow

Stow works by creating symlinks from your dotfiles repo into your home directory.

### To link a config directory

```bash
stow .config/nvim
stow .config/wezterm
stow .config/fastfetch
```

### To remove symlinks (unstow)

```bash
stow -D .config/nvim
```

> ⚠️**Warning**: 'stow -D' removes symlinks, not actual files.
> It only unlinks the dotfiles Stow created. You real config files will remain untouched.
> But make sure you're not relying on the symlinks before removing them.

### Dry run (preview changes)

```bash
stow -nv .config/nvim
```

### Restow (refresh links after making changes)

```bash
stow -R .config/nvim
```

### Unstow everything

```bash
stow -D */*
```

> ⚠️**Warning**: Unstowing everything will remove all symlinks created by Stow.
> Make sure you're not deleting anything important. This won't delete your actual config folders, just the symlinks.

## Directory structure

```
~/.dotfiles
├── .zshrc
│
└── .config/
    ├── fastfetch
    ├── nvim
    └── wezterm
```
