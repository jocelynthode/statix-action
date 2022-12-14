# statix-action

Automatically creates pull requests to lint Nix
files

## Usage

Create a `.github/workflows/statix.yml` file:

```yaml
on: [push]

name: Lint Nix code

jobs:
  statix:
    name: Lint code
      runs-on: ubuntu-latest
        steps:
          - uses: actions/checkout@v3.1.0
          - uses: cachix/install-nix-action@v18
          - uses: cachix/cachix-action@v12
            with:
              name: statix
          - uses: jocelynthode/statix-action@master
```


## Inspiration

Thanks to [deadnix-action](https://github.com/astro/deadnix-action)
