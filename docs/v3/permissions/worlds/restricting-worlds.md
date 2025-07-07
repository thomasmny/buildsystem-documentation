# Restricting Worlds

_BuildSystem_ allows server owners to restrict which worlds a player can modify when using commands.

{% hint style="info" %}
All commands default to `.self` when no suffix (`.self`, `.other`) is provided.&#x20;

**For example:** `buildsystem.day` = `buildsystem.day.self`
{% endhint %}

## Only modify worlds owned by player

If you want a player to only modify worlds which belong to the player (i.e. player **is** creator), then use the command suffix `.self`.

**For example:** If you only want player's to change the world time to day (`/day`) in their own worlds, then give the player the permission `buildsystem.day.self`.

## Modify worlds not owned by player

With the permission suffix `.other`, a player can also modify worlds that **don't** belong to the player (player is **not** creator)

**For example:** If you only want player's to change the world time to day (`/day`) in other worlds, then give the player the permission `buildsystem.day.other`.
