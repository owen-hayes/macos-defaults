---
title: Focus du Terminal au survol | Divers
---

::: warning Attention
La langue française n'est plus supportée sur macos-defaults.com. Cette page redirigera automatiquement vers la version anglaise correspondante en 2024.
:::

# Focus du Terminal au survol

Focus des fenêtres du Terminal au survol du curseur de la souris.
Le changement de focus ne fonctionne qu'entre les fenêtres du Terminal.

<!-- break lists -->

- **Testé sur macOS**:
  - Ventura
  - Monterey
- **Type de paramètre**: bool

## Avec la valeur `false` (par défaut)

Par défaut le changement de focus entre fenêtres du Terminal se fait en cliquant sur celles-ci ou en pressant
<code>cmd + `</code> .

```bash
defaults write com.apple.Terminal "FocusFollowsMouse" -bool "false" && killall Terminal
```

<video autoplay loop muted playsinline width="739" height="416" style="max-width: 100%; height: auto">
  <source src="../../misc/images/FocusFollowsMouse/false.mp4" type="video/mp4">
  Exemple avec la valeur false
</video>

## Avec la valeur `true`

Le focus suit le curseur de la souris entre les fenêtres du Terminal.

```bash
defaults write com.apple.Terminal "FocusFollowsMouse" -bool "true" && killall Terminal
```

<video autoplay loop muted playsinline width="739" height="416" style="max-width: 100%; height: auto">
  <source src="../../misc/images/FocusFollowsMouse/true.mp4" type="video/mp4">
  Exemple avec la valeur true
</video>

## Lire la valeur courante

```bash
defaults read com.apple.Terminal "FocusFollowsMouse"
```

## Remettre la valeur à l'état initial

```bash
defaults delete com.apple.Terminal "FocusFollowsMouse" && killall Terminal
```
