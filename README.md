# NixOS configuration
## Flake update:
- `nix flake update`
- `sudo nixos-rebuild switch --flake ~/.dotfiles`
- `home-manager switch --flake ~/.dotfiles`

## Home-manager rollack:
- `home-manager generations` - list all generations. Output:
```
[vectorofint@pc:~/.dotfiles]$ home-manager generations
2024-06-06 10:24 : id 5 -> /nix/store/byn6cwhrdjjhv1j5njy5ic97n6z9qarv-home-manager-generation
2024-06-06 10:16 : id 4 -> /nix/store/bmm3jxlqkngxbx44x0nj36v2hhxwhp1z-home-manager-generation
2024-06-06 10:13 : id 3 -> /nix/store/0lrx5m9lirm4zlahn3p9s3np4yijy06s-home-manager-generation
2024-06-06 10:01 : id 2 -> /nix/store/wc54xzi31vz0r72q4x401jjdpim1sfp0-home-manager-generation
2024-06-06 09:48 : id 1 -> /nix/store/cq2dsf92xrv3m4qi3k5i6daz2vd6a2pa-home-manager-generation

```
- Select the generation that you want to rollback to. I would like to rollback to session **id 2**.
- Copy **id 2** generation path. In this case it's `/nix/store/wc54xzi31vz0r72q4x401jjdpim1sfp0-home-manager-generation`
- To rollback to this generation add `/activate` at the end of the generation path.
```
/nix/store/wc54xzi31vz0r72q4x401jjdpim1sfp0-home-manager-generation/activate
```
