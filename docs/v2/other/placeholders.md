---
description: Some placeholders are part of the plugin, others require PlaceholderAPI
---

# Placeholders

## Table of Contents

1. [Integrated Placeholders](placeholders.md#integrated-placeholders)
2. [PlaceholderAPI Placeholders](placeholders.md#placeholderapi-placeholders)
   1. [Settings Placeholders](placeholders.md#settings-placeholders)
   2. [World Placeholders](placeholders.md#world-placeholders)

## Integrated Placeholders

Integrated placeholders are placeholders that come included with the plugin and do not require any external dependancies. They can be used in `messages.yml`.

{% hint style="info" %}
The default layout for all placeholder part of the plugin itself is **%\<value>%**. However, these placeholders cannot be used in all messages found in `messages.yml`. \
The message must already **contain the placeholder by default** or be the `scoreboard` or `world_item_lore`&#x20;
{% endhint %}

#### World builders

> Returns the list of builders in the world.

{% hint style="warning" %}
Not available for the `scoreboard`
{% endhint %}

```
%builders%
```

#### World creator

> Returns the world's creator.

```
%creator%
```

#### World creation date

> Returns the world's creation date.

```
%creation%
```

#### World permission

> Returns the permission needed for the world.

```
%permission%
```

#### World project

> Returns the world's project.

```
%project%
```

#### World status

> Returns the world's status (e.g. In Progress, Archive, etc.).

```
%status%
```

#### World name

> Returns the name of the world.

```
%world%
```



## PlaceholderAPI Placeholders

There are two main types of placeholders that are provided to the PlaceholderAPI:

1. Settings Placeholders
2. World Placeholders

The difference between both can be found out in the following.



### Settings Placeholders

{% hint style="info" %}
The default layout for a settings placeholder is **%buildsystem\_settings\_\<settings>%**

For more information on each setting, look [here](../commands/settings.md#settings).
{% endhint %}

#### Navigator Type

```
%buildsystem_settings_navigatortype%
```

#### Glass Color

```
%buildsystem_settings_glasscolor%
```

#### World Sort

```
%buildsystem_settings_worldsort%
```

#### Clear Inventory

```
%buildsystem_settings_clearinventory%
```

#### Disable Interact

```
%buildsystem_settings_disableinteract%
```

#### Hide Players

```
%buildsystem_settings_hideplayers%
```

#### Instant Place Signs

```
%buildsystem_settings_instantplacesigns%
```

#### Keep Navigator

```
%buildsystem_settings_keepnavigator%
```

#### Night Vision

```
%buildsystem_settings_nightvision%
```

#### NoClip

```
%buildsystem_settings_noclip%
```

#### Place Plants

```
%buildsystem_settings_placeplants%
```

#### Scoreboard

```
%buildsystem_settings_scoreboard%
```

#### Slab Breaking

```
%buildsystem_settings_slabbreaking%
```

#### Spawn Teleport

```
%buildsystem_settings_spawnteleport%
```

#### Open (Trap-)Doors

```
%buildsystem_settings_opentrapdoors%
```



### World Placeholders

{% hint style="info" %}
The default layout for a world placeholder is **%buildsystem\_\<value>%**.&#x20;

If a world is not specified by using the format  **%buildsystem\_\<value>\_\<world>%** then the world the player is currently in will be used.
{% endhint %}

#### Block breaking

> Returns whether or not blocks can be broken in the world.

```
%buildsystem_blockbreaking%
```

#### Block placement

> Returns whether or not blocks can be placed in the world.

```
%buildsystem_blockplacement%
```

#### World builders

> Returns the list of builders in the world.

```
%buildsystem_builders%
```

#### Builders enabled in world

> Returns whether or not the builders feature is enabled in the world.

```
%buildsystem_buildersenabled%
```

#### World creation date

> Returns the world's creation date.

```
%buildsystem_creation%
```

#### World creator

> Returns the world's creator.

```
%buildsystem_creator%
```

#### World creator ID

> Returns the UUID of the world's creator.

```
%buildsystem_creatorid%
```

#### Explosions

> Returns whether or not explosions are enabeld in the world.

```
%buildsystem_explosions%
```

#### World loaded

> Returns whether or not the world is loaded.

```
%buildsystem_loaded%
```

#### World material

> Returns the world's material which is shown in the navigator.

```
%buildsystem_material%
```

#### MobAI

> Returns whether or not mobs have an AI in the world.

```
%buildsystem_mobai%
```

#### World permission

> Returns the permission needed for the world.

```
%buildsystem_permission%
```

#### World visibility

> Returns the world's visibility (private or public).

```
%buildsystem_private%
```

#### World project

> Returns the world's project.

```
%buildsystem_project%
```

#### World physics

> Returns whether or not physics are enabled in the world.

```
%buildsystem_physics%
```

#### World spawn

> Returns the world's spawn.

```
%buildsystem_spawn%
```

#### World status

> Returns the world's status (e.g. In Progress, Archive, etc.).

```
%buildsystem_status%
```

#### World type

> Returns the world's type (e.g. Normal, Flat, Nether, etc.).

```
%buildsystem_type%
```

#### World name

> Returns the name of the world.

```
%buildsystem_world%
```
