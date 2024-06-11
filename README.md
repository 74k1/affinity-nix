# affinity-nix

Affinity Photo, Designer, and Publisher applications with packaged with nix.

Based on https://github.com/lf-/affinity-crimes and https://codeberg.org/wanesty/affinity-wine-docs, and uses [ElementalWarrior's wine](https://gitlab.winehq.org/ElementalWarrior/wine).

## Usage Instructions

**Cached with garnix. Add it as a nix subsitutor! Read https://garnix.io/docs/caching for instructions.**

Perform the first time setup which will manipluate `~/.local/share/affinity/`.

```bash
nix run github:mrshmllow/affinity-nix#photo

nix run github:mrshmllow/affinity-nix#designer

nix run github:mrshmllow/affinity-nix#publisher
```

The operation will fail half way. Copy `C:\Windows\System32\WinMetadata` from a windows computer to `~/.local/share/affinity/drive_c/windows/system32/`.

```bash
cp -r ~/Documents/WinMetadata ~/.local/share/affinity/drive_c/windows/system32/
```

Launch the package again and follow the installation prompts.
