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

## Directory structure (template)

```
~/.dotfiles
├── .zshrc
│
└── .config/
    ├── fastfetch
    ├── nvim
    └── wezterm
```
