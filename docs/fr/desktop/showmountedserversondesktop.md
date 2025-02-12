---
title: Serveurs connectés | Bureau
---

::: warning Attention
La langue française n'est plus supportée sur macos-defaults.com. Cette page redirigera automatiquement vers la version anglaise correspondante en 2024.
:::

# Serveurs connectés

Afficher sur le bureau les serveurs connectés.

<!-- break lists -->

- **Testé sur macOS**:
  - Monterey
  - Big Sur
- **Type de paramètre**: bool

## Avec la valeur `true`

Affiche les serveurs connectés

```bash
defaults write com.apple.finder "ShowMountedServersOnDesktop" -bool "true" && killall Finder
```

## Avec la valeur `false` (par défaut)

Masque les serveurs connectés

```bash
defaults write com.apple.finder "ShowMountedServersOnDesktop" -bool "false" && killall Finder
```

## Lire la valeur courante

```bash
defaults read com.apple.finder "ShowMountedServersOnDesktop"
```

## Remettre la valeur à l'état initial

```bash
defaults delete com.apple.finder "ShowMountedServersOnDesktop" && killall Finder
```
