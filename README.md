# Nix Flake Setup

## Preparation

# NixOS

- Install NixOS
- Enable Git in `configuration.nix` under `systemPackages`
- Enable Flakes in `configuration.nix`
  `nix.settings.experimental-features = [ "nix-command" "flakes" ];`
- sudo nixos-rebuild switch
- [generate an ssh key](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent#generating-a-new-ssh-key)

## Usage

Clone the repo to `~/.nixos`

Modify options in `config.nix` as required, including adding any new packages.

To apply: 

```bash
> nix run nix-darwin -- switch --flake .#mbp-dev
```
