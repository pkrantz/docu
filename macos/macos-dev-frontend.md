# Development Frontend

## Node (v14)

```bash
brew install node@14
```

`node@14` is `keg-only`, which means it was not symlinked into `/usr/local`. If you need to have `node@14` first in your `PATH`, run:

```bash
echo 'export PATH="/usr/local/opt/node@14/bin:$PATH"' >> /Users/{username}/.bash_profile
node --version
npm --version
```

## Global dependencies

```bash
npm install -g @angular/cli
```
