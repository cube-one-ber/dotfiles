# Dotfiles Managed with Chezmoi

This repository contains my personal configuration files (dotfiles) managed with [Chezmoi](https://www.chezmoi.io/). Feel free to use them!

## Repository

**Clone URL:**  
```
ssh://git@codeberg.org/Cube1ber/dotfiles.git
```

## Requirements

- Git

## Installation

1. **Clone and initialize the dotfiles using Chezmoi**:

```zsh
sh -c "$(curl -fsLS get.chezmoi.io)" -- init --ssh git@codeberg.org:Cube1ber/dotfiles.git
```

2. **Apply changes to your home directory**:

```zsh
chezmoi apply
```

3. **Edit configurations** (optional):

```zsh
chezmoi edit <file>
```

## Updating Dotfiles

After making changes to your local dotfiles, update the repository with:

```zsh
chezmoi add <file>
git commit -m "Update dotfiles"
git push origin master
```

To pull and apply updates on another machine:

```zsh
chezmoi update
chezmoi apply
```

## Encryption (Optional)

Sensitive files can be encrypted using GPG. Chezmoi automatically decrypts them when applying:

```zsh
chezmoi add --encrypt <sensitive_file>
```

## Structure

A typical structure for the repository:

```
dotfiles/
├── .zshrc
├── .vimrc
├── .gitconfig
├── .config/
│   ├── nvim/
│   └── alacritty/
└── README.md
```

## Contributing

These dotfiles are primarily for personal use. Feel free to fork, adapt, and use them for your own purposes.

---

[License](LICENSE)
