---
description: Change your gamemode.
---

# /gm

## Usage

```
/gm <gamemode> [player]
```

{% hint style="info" %}
You can use the following arguments for each gamemode:\
\
**Survival:** `survival`, `s`, `0`\
**Creative:** `creative`, `c`, `1`\
**Adventure:** `adventure`, `a`, `2`\
**Spectator:** `spectator`, `sp`, `3`
{% endhint %}

## Permission

### Until v2.26.0

#### /gm \<gamemode>

```
buildsystem.gamemode
```

#### /gm \<gamemode> \<player>

```
buildsystem.gamemode.others
```

### From v2.27.0 onwards

#### /gm \<gamemode>

```
buildsystem.gamemode
```

{% hint style="info" %}
Each gamemode also has it's own permission which is granted by default when the player has the `buildsystem.gamemode` permission:

* **Survival**: `buildsystem.gamemode.survival`
* **Creative**: `buildsystem.gamemode.creative`
* **Adventure**: `buildsystem.gamemode.adventure`
* **Spectator**: `buildsystem.gamemode.spectator`
{% endhint %}

#### /gm \<gamemode> \<player>

```
buildsystem.gamemode.other
```

{% hint style="info" %}
Each gamemode also has it's own permission which is granted by default when the player&#x20;

has the `buildsystem.gamemode.other` permission:

* **Survival**: `buildsystem.gamemode.survival.other`
* **Creative**: `buildsystem.gamemode.creative.other`
* **Adventure**: `buildsystem.gamemode.adventure.other`
* **Spectator**: `buildsystem.gamemode.spectator.other`
{% endhint %}
