# Config

## messages

### `spawn-teleport-message`

* **default:** false
* **description:** Sets whether a message will be sent when teleporting to the spawn.

### `join-quit-message`

* **default:** true
* **description:** Sets whether a message will be sent when a player joins or quite the server.

### `date-format`

* **default:** dd/MM/yyyy
* **description:** Sets the date format that will be used throughout the plugin.

## settings

### `update-checker`

* **default:** true
* **description:** Sets whether the plugin should check for possible updates and notfiy players if any are found.

### `scoreboard`

* **default:** true
* **description:** Sets whether the scoreboard component should be initiated. If set to `false`, players will not be able to activate the scoreboard. Is not equivalent to the per-player setting!

### archive

#### `vanish`

* **default:** true
* **description:** Sets whether players should be hidden from other players and receive an invisibility effect in archived worlds.

#### `change-gamemode`

* **default:** true
* **description:** Sets whether a player's gamemode will be automaticcaly set (to the one provided by [#world-gamemode](config.md#world-gamemode "mention")) when entering archive worlds.

#### `world-gamemode`

* **default:** ADVENTURE
* **description:** The gamemode which a player will be set to when entering archive worlds. Requires [#change-gamemode](config.md#change-gamemode "mention") to be enabled.

### save-from-death

#### `enabled`

* **default:** true
* **description:** Sets whether a player will be saved from death if they fall into the void

#### `teleport-to-map-spawn`

* **default:** true
* **description:** Sets whether the player will be teleported to the map spawn if they receive void damage. If disabled, the player will be teleported 200 blocks upwards. Requires [#enabled](config.md#enabled "mention") to be set to true.

### build-mode

#### `drop-items`

* **default:** true
* **description:** Sets whether a player can drop items while in "build mode" (`/build`)

#### `move-items`

* **default:** true
* **description:** Sets whether a player can move items (e.g. into a chest) while in "build mode" (`/build`)

### builder

#### `block-worldedit-non-builder`

* **default:** true
* **description:** When enabled, players who are not a builder in a world, will not be able to use WorldEdit commands in said world.

### navigator

#### `item`

* **default:** CLOCK
* **description:** The item to be used as the navigator.

#### `give-item-on-join`

* **default:** true
* **description:** Sets whether the navigator should be given to a player on joining the server.

## world

### default

{% hint style="info" %}
When a new world is generated, the following settings are set for that specific world.
{% endhint %}

#### permission

* `public`
  * **default:** -
  * **description:** The default permission _public_ worlds have when created
* `private`
  * **default:** worlds.%world%
  * **description:** The default permission _private_ worlds have when created

#### time

* `sunrise`
  * **default:** 0
  * **description:** The time which is used when setting the time in a world to "sunrise".
* `noon`
  * **default:** 6000
  * **description:** The time which is used when setting the time in a world to "noon".
* `night`
  * **default:** 18000
  * **description:** The time which is used when setting the time in a world to "night".

#### worldboarder

* `size`
  * **default:** 6000000
  * **description:** The size which the world board is set to on world generation.

#### `difficulty`

* **default:** PEACEFUL
* **description:** The difficulty of a world which is used on generation.

#### `gamerules`

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
* **description:** A map of gamerules and their values which are to be automatically set.

#### settings

* `physics`
  * **default:** true
  * **description:** Sets whether blocks have physics in the world. For example, if phyiscs are disabled, sand will not have gravity.
* `explosions`
  * **default:** true
  * **description:** Sets whether explosions are allowed in the world.
* `mob-ai`
  * **default:** true
  * **description:** Sets whether mobs have an AI in the world.
* `block-breaking`
  * **default:** true
  * **description:** Sets whether blocks are allowed to be broken in the world.
* `block-placement`
  * **default:** true
  * **description:** Sets whether blocks are allowed to be placed in the world.
* `block-interactions`
  * **default:** true
  * **description:** Sets whether blocks are allowed to be interacted with in the world.
* builders-enabled
  * **default:**&#x20;
    * `public`: false
    * `private`: true
  * **description:** Sets whether only builders should be allowed to build in the world.

### `lock-weather`

* **default:** true
* **description:** Sets whether the weather will be locked and will therefore not change.

### `invalid-characters`

* **default:** ^\b$
* **description:** Specify further characters to be removed from a world's name on creation.

### import-all

#### `delay`

* **default:** 30
* **description:** Sets the amount of seconds between the import each world.

### max-amount

#### `public`

* **default:** -1
* **description:** Sets the maximum amount of public worlds that are allowed to exist simultaneously. Set to -1 to disable.

#### `private`

* **default:** -1
* **description:** Sets the maximum amount of private worlds that are allowed to exist simultaneously. Set to -1 to disable.

### unload

#### `enabled`

* **default:** false
* **description:** Sets whether worlds will automatically be unloaded after a given time when no players are present in the world.

#### `time-untill-unload`

* **default:** 01:00:00
* **description:** Sets the time until a worlds will automatically be unloaded.

#### `blacklisted-worlds`

* **default:**

```
- world
- world_nether
- worth_the_end
```

* **description:** A list of all worlds that will not be unloaded, even if there are no players present in the world.

### `deletion-blacklist`

* **default:**

```
- world
- world_nether
- worth_the_end
```

* **description:** A list of all worlds that cannot be deleted by any player.

### backup

#### `max-backups-per-world`

* **default:** 5
* **description:** The maximum amount of backups a world can have (limited to 18).

#### auto-backup

* `enabled`
  * **default:** true
  * **description:** Sets whether worlds will be automatically backed up in a predefined interval.
* `interval`
  * **default:** 900
  * **description:** The interval (in seconds) in which worlds are backed up automatically.
* `only-active-worlds`
  * **default:** true
  * **description:** Sets whether only active worlds (i.e. worlds with builders in them) will be backed up.

#### storage

* `type`
  * **default:** local
  * **description:** Defines where backups are to be saved to. \
    Can be either `local` (saved on the server), `s3` (saved on an S3 storage) or `sftp` (uploaded to a server)
* s3 (only required when using S3)
  * `url`: If not using AWS S3, specify the S3 storage's URL.
  * `access-key`: The access key required to access the S3 storage instance.
  * `secret-key`: The secret key required to access the S3 storage instance.
  * `region`: The region of the S3 storage instance.
  * `bucket`: The bucket in which backups are to be stored.
  * `path`: The path at which backups are to be stored within the bucket.
* sftp (only required when using SFTP)
  * `host`: The server host.
  * `port`: The server port.
  * `username`: The username required to access the server.
  * `password`: The password required to access the server.
  * `path`: The path at which backups are to be stored on the server.

## folder

### `override-permissions`

* **default:** true
* **description:** Sets whether worlds will inherit a parent folder's permission.

### `override-projects`

* **default:** false
* **description:** Sets whether worlds will inherit a parent folder's project.
