# Shell environments
- Use programs without permanently installing
	- `nix-shell --packages cowsay lolcat`
	- `nix-shell -p vscode`
	- `nix-shell -p cowsay --run "cowsay Test"`
	- `nix-shell -p hello --run hello`
- Nestable
## Declarative shell environments
- `shell.nix`
- [ ] Learn the language
# Packages
> [Search here!](https://search.nixos.org/packages)
# Reproduciblility
- Able to specify exact versions of packages
	- `nix-shell -p git --run "git --version" --pure -I nixpkgs=[url]`
		- `--pure` discards most environment variables
		- `-I` indicates the source
## Scripts
```
#! /usr/bin/env nix-shell
#! nix-shell -i real-interpreter -p packages
```
- Note that `-i` is not `-I`
- See [[nixpkgs-releases.sh]] for an example!
