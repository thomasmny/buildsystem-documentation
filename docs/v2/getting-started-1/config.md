# Config

## Messages

### spawn-teleport-message

* **default:** false
* **description:** Sets whether a message will be sent when teleporting to the spawn.

### join-quit-message

* **default:** true
* **description:** Sets whether a message will be sent when a player joins or quite the server.

### join-quit-message

* **default:** dd/MM/yyyy
* **description:** Sets the date format that will be used throughout the plugin.

## Settings

### update-checker

* **default:** true
* **description:** Sets whether the plugin should check for possible updates and notfiy players if any are found.

### scoreboard

* **default:** true
* **description:** Sets whether the scoreboard component should be initiated. If set to `false`, players will not be able to activate the scoreboard. Is not equivalent to the per-player setting!

### archive-vanish

* **default:** true
* **description:** Sets whether players should be hidden from other players and receive an invisibility effect in archived worlds.

### teleport-after-creation

* **default:** true
* **description:** Sets whether the creator of a world should be automatically teleported to a said world when it is created.

### builder

#### block-worldedit-non-builder

* **default:** true
* **description:** When enabled, players who are not a builder in a world, will not be able to use WorldEdit commands in said world.

### navigator

#### item

* **default:** CLOCK
* **description:** The item to be used as the navigator.

#### give-item-on-join

* **default:** true
* **description:** Sets whether the navigator should be given to a player on joining the server.

## world

### default

{% hint style="info" %}
When a new world is generated, the following settings are set for that specific world.
{% endhint %}

#### permission

* public
  * **default:** -
  * **description:** The default permission _public_ worlds have when created
* private
  * **default:** worlds.%world%
  * **description:** The default permission _private_ worlds have when created

#### time

* sunrise
  * **default:** 0
  * **description:** The time which is used when setting the time in a world to "sunrise".
* noon
  * **default:** 6000
  * **description:** The time which is used when setting the time in a world to "noon".
* night
  * **default:** 18000
  * **description:** The time which is used when setting the time in a world to "night".

#### worldboarder

* size
  * **default:** 6000000
  * **description:** The size which the world board is set to on world generation.

#### difficulty

* **default:** PEACEFUL
* **description:** The difficulty of a world which is used on generation.

#### gamerules

{% hint style="info" %}
To add a gamerule which should be set on world generation, just add it to the list of existing ones (or remove the present ones if needed).

For example if you want to add the gamerule `randomTickSpeed`:&#x20;

```
doDaylightCycle: false
doMobSpawning: false
doFireTick: false
randomTickSpeed: 0
```
{% endhint %}

*   **default:**

    ```
    doDaylightCycle: false
    doMobSpawning: false
    doFireTick: false
    ```

#### settings

* physics
  * **default:** true
  * **description:** Sets whether blocks have physics in the world. For example, if phyiscs are disabled, sand will not have gravity.
* explosions
  * **default:** true
  * **description:** Sets whether explosions are allowed in the world.
* mob-ai
  * **default:** true
  * **description:** Sets whether mobs have an AI in the world.
* block-breaking
  * **default:** true
  * **description:** Sets whether blocks are allowed to be broken in the world.
* block-placement
  * **default:** true
  * **description:** Sets whether blocks are allowed to be placed in the world.
* block-interactions
  * **default:** true
  * **description:** Sets whether blocks are allowed to be interacted with in the world.
* builders-enabled
  * **default:**&#x20;
    * public: false
    * private: true
  * **description:** Sets whether only builders should be allowed to build in the world.

### lock-weather

* **default:** true
* **description:** Sets whether the weather will be locked and will therefore not change.

### invalid-characters

* **default:** ^\b$
* **description:** Specify further characters to be removed from a world's name on creation.

### import-all

#### delay

* **default:** 30
* **description:** Sets the amount of seconds between the import each world.

### max-amount

#### public

* **default:** -1
* **description:** Sets the maximum amount of public worlds that are allowed to exist simultaneously. Set to -1 to disable.

#### private

* **default:** -1
* **description:** Sets the maximum amount of private worlds that are allowed to exist simultaneously. Set to -1 to disable.

### unload

#### enabled

* **default:** false
* **description:** Sets whether worlds will automatically be unloaded after a given time when no players are present in the world.

#### time-untill-unload

* **default:** 01:00:00
* **description:** Sets the time until a worlds will automatically be unloaded.

#### blacklisted-worlds

* **default:**

```
- world
- world_nether
- worth_the_end
```

* **description:** A list of all worlds that will not be unloaded, even if there are no players present in the world.

### void-block

* **default:** true
* **description:** Sets whether a gold block should be generated at `0 64 0` in a void world.\
