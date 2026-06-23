# Changelog

## 2026.06.23 — split per colour from the LinuxMint upstream

**Install docs:** the README install section now lists the meta packages (top-level `*-icons-meta`, plus the group meta where applicable) alongside the per-variant `*-icons-git` package — replacing the outdated single `pacman -S` line.

### What Changed

Initial standalone repo. The **Surfn-Mint-X-Yellow** colour variant was generated fresh from
`linuxmint/mint-x-icons` and surfn-ified so it ships as its own package, `surfn-mint-x-yellow-icons-git`,
depending on the base `surfn-icons-git`.

### Technical Details

- `usr/share/icons/Mint-X-Yellow/` copied from upstream, dir renamed to `Surfn-Mint-X-Yellow`.
- `index.theme` patched: `Name=Surfn Mint-X-Yellow`, `Inherits=Surfn,Adwaita,gnome,hicolor`.
- `icon-theme.cache` not shipped — the pacman gtk-update-icon-cache hook rebuilds it on install.

### Files Modified

- Initial scaffold + usr/share/icons/Surfn-Mint-X-Yellow/
