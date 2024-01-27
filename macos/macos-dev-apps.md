# Terminal

## Homebrew

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)“
```

## Bash

- .bash_aliases
- .bash_profile
- .bashrc

## ITerm

```bash
brew install iterm2
```

## Oh my Posh`

```bash
brew tap jandedobbeleer/oh-my-posh
brew install oh-my-posh
```

Use a standard theme. Add the following to `~/.bashrc `

```bash
eval "$(oh-my-posh --init --shell bash --config $(brew --prefix oh-my-posh)/themes/jandedobbeleer.omp.json)"
```

Preview the themes

```bash
for file in $(brew --prefix oh-my-posh)/themes/*.omp.json; do echo "$file\n"; oh-my-posh --config $file --shell universal; echo "\n"; done;
```

# Applications

## Insomnia

```bash
brew install --cask insomnia
```

## Atom

```bash
brew install --cask atom
```
