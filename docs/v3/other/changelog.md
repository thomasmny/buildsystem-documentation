# Changelog

## v3.0.0 - 17.10.2025

{% tabs %}
{% tab title="Added" %}
* Added [Developer API](https://github.com/thomasmny/BuildSystem/pull/200)
* Added [World Folders](https://github.com/thomasmny/BuildSystem/pull/352)
* Added [World Backups](https://github.com/thomasmny/BuildSystem/pull/357)
* Added [config option to prohibit world deletion](https://github.com/thomasmny/BuildSystem/commit/0838b76f22fe33ac9a6d2e453455a70cc2e5cde5)
* Added [config option for disabled world physics](https://github.com/thomasmny/BuildSystem/pull/372)
* Added [commands for directly opening navigator categories](https://github.com/thomasmny/BuildSystem/commit/6057dee955741ee15e8002d5a6fd32d5497d05f4)
{% endtab %}

{% tab title="Fixed" %}
* Fixed [template worlds not keeping world generator settings](https://github.com/thomasmny/BuildSystem/pull/360)
{% endtab %}

{% tab title="Other" %}
* [Updated to Java 21](https://github.com/thomasmny/BuildSystem/pull/355)
* [Dropped support for older versions](https://github.com/thomasmny/BuildSystem/pull/356)
{% endtab %}
{% endtabs %}

## v2.27.1 - 26.05.2025

{% tabs %}
{% tab title="Fixed" %}
Fixed `java.lang.ClassCastException` when sending title to player that a world is loading
{% endtab %}
{% endtabs %}

## v2.27.0 - 26.05.2025

{% tabs %}
{% tab title="Added" %}
* Add support for Minecraft 1.21.5
* Add individual permissions for each gamemode
{% endtab %}
{% endtabs %}

## v2.26.0 - 16.01.2025

{% tabs %}
{% tab title="Added" %}
* Add support for Minecraft 1.21.3 & 1.21.4
* Simple Axiom Support
* Add permissions to `/buildsystem`, `/worlds help` and `/worlds item`
* Add bypass permissions for viewing/joining worlds
{% endtab %}

{% tab title="Changed" %}
* Reload `messages.yml` file when using `/config reload`
{% endtab %}

{% tab title="Fixed" %}
* Fix UUID fetch bug in offline server
* Add permission check when navigating from `/worlds builders` to the world editor
{% endtab %}
{% endtabs %}

## v2.25.2 - 30.09.2024

{% tabs %}
{% tab title="Added" %}
Added the option to disable the adventure game mode on archived worlds
{% endtab %}

{% tab title="Fixed" %}
Removed fall damage cancellation
{% endtab %}
{% endtabs %}

## v2.25.1 - 08.07.2024

{% tabs %}
{% tab title="Fixed" %}
Fixed `IncompatibleClassChangeError`
{% endtab %}
{% endtabs %}

## v2.25.0 - 06.07.2024

{% tabs %}
{% tab title="Added" %}
* Add support for Minecraft 1.21
* Improve skull performance in menus
* Added world type to the import command
* Allow builders to be added and removed via command
{% endtab %}

{% tab title="Fixed" %}
* Fixed incorrectly implemented bypass logic
* Don't allow world to be renamed if other world with new name already exists
* World was not saved before chunks are unloaded
* Fixed NPE when using filters
{% endtab %}
{% endtabs %}

## v2.24.4 - 13.12.2023

{% tabs %}
{% tab title="Added" %}
* Added support for Minecraft 1.20.4
{% endtab %}

{% tab title="Fixed" %}
* Fixed message error in world editor
{% endtab %}
{% endtabs %}

## v2.24.3 - 01.12.2023

{% tabs %}
{% tab title="Changed" %}
* Worlds are now unloaded by default; **If you do not have this setting activated, I suggest you do so**
* Add permission to setting individual status states (`/worlds setStatus`): [https://buildsystem.eintosti.de/worlds/setstatus#individual-permission](https://buildsystem.eintosti.de/worlds/setstatus#individual-permission)
* Improve player teleportation: Player is now teleported up when `VOID` damage is received
* You can now use PlaceholderAPI placeholders in messages
* The scoreboard is now updated scoreboard asynchronously
{% endtab %}

{% tab title="Fixed" %}
* Worlds which are blacklisted from being unloaded will now load when the server starts
* The "import successful" message will only be sent if the import actually finished
* Added missing plants to the "Place Plants" setting
{% endtab %}
{% endtabs %}

## v2.24.2 - 04.10.2023

{% tabs %}
{% tab title="Added" %}
* **Added 1.20.2 support**
{% endtab %}

{% tab title="Fixed" %}
* Few bug fixes
{% endtab %}
{% endtabs %}

## v2.24.1 - 26.06.2023

{% tabs %}
{% tab title="Added" %}
* **Added 1.20.1 support**
{% endtab %}
{% endtabs %}

## v2.24.0 - 10.06.2023

{% tabs %}
{% tab title="Added" %}
* **Added 1.20 support**\

* **Added ability to filter words in navigator**
  * New slot in the navigator
  * Toggle through multiple settings: "_none_", "_starts with_", "_contains_" and "_matches_"\

* **Allow admins to specify further illegal characters in a world's name**
  * New config option: `invalid-characters`
  * If a character in the world's name matches the specified regex, it is removed\

* **New placeholders**
  * `%buildsystem_lastedited%`
  * `%buildsystem_lastloaded%`
  * `%buildsystem_lastunloaded%`
{% endtab %}
{% endtabs %}

## v2.23.1 - 07.05.2023

{% tabs %}
{% tab title="Fixed" %}
* Fixed worlds being not imported correctly
* Scoreboard lines longer than 30 chars are now trimmed in versions <1.13
* Fixed bypass of world version check when importing worlds (`-DPaper.ignoreWorldDataVersion`)
{% endtab %}

{% tab title="Improved" %}
* Added `-c <creator>` argument to `/worlds import` command, to specify which player should be the creator of the imported world
* Removed `creator-is-builder` config option, as creator should always be builder
* Removed `world-edit-wand` config option, as WorldEdit wand is now read from the (FastAsync)WorldEdit config
{% endtab %}
{% endtabs %}

## v2.23.0 - 23.03.2023

{% tabs %}
{% tab title="Added" %}
* **Added 1.19.4 support**
* **Added ability to not send messages**
  * Blank messages are no longer sent to the player
  * Example: A command is to be hidden from `/buildsystem` \
    -> Set `buildsystem_XXX: ""` in the `messages.yml` file
{% endtab %}

{% tab title="Changed" %}
* **Multi-page `/buildsystem` command**
  * The `/buildsystem [page]` command now takes a page argument, as it no longer displays all commands at once
{% endtab %}

{% tab title="Fixed" %}
* Players _not_ in build-mode could not interact with other inventories when `move-items` was disabled
{% endtab %}
{% endtabs %}

## v2.22.3 - 04.03.2023

{% tabs %}
{% tab title="Fixed" %}
* **Fix duplicate message key**
  * The key "`worlds_import_newer_version`" was supposed to be "`worlds_importall_newer_version`"
* **Allow messages to contain commas**
  * Previously, when using commas (,) in multi-line messages would result in the message being split
{% endtab %}
{% endtabs %}

## v2.22.2 - 20.12.2022

{% tabs %}
{% tab title="Changed" %}
Compress world `level.dat` with GZIP when writing server version
{% endtab %}
{% endtabs %}

## v2.22.1 - 16.12.2022

{% tabs %}
{% tab title="Fixed" %}
Fixes a bug that would stop worlds from being loaded on servers using Spigot 1.8
{% endtab %}
{% endtabs %}

## v2.22.0 - 16.12.2022

{% tabs %}
{% tab title="Added" %}
* **1.19.3 support**
* **Check world `DataVersion` before loading**
  * Stops newer worlds from being loaded in older versions
  * Is ignored when `Paper.ignoreWorldDataVersion` flag is enabled
* **Add `move-items` config option**
  * Stops a player from moving/taking items to/from other inventories when in build-mode
  * Also changed the default of `drop-items` to true
{% endtab %}

{% tab title="Fixed" %}
* Player would receive navigator even if setting was disabled
* Instant Place Signs didn't support `mangrove_sign`
{% endtab %}
{% endtabs %}

## v2.21.2 - 05.11.2022

{% tabs %}
{% tab title="Added" %}
* **Improvements to /build**
  * Add permission for when setting other players into build-mode: `buildsystem.build.others`
  * Reset player inventory when leaving build-mode
  * New config option for disabling item drops when in build-mode (default: false)
  * Add LuckPerms context for when players are in build-mode (`build-mode`)
{% endtab %}

{% tab title="Fixed" %}
* Custom blocks were not being placed when disable interactions is enabled
{% endtab %}
{% endtabs %}

## v2.21.1 - 05.11.2022

{% tabs %}
{% tab title="Fixed" %}
Fix world icon not displaying correctly
{% endtab %}
{% endtabs %}

## v2.21.0 - 05.11.2022

{% tabs %}
{% tab title="Added" %}
* **Utilize PaperLib**
  * If the server is running Paper, players will be teleported asynchronously&#x20;
* **Improved** **`/worlds` command**
  * Up till now, whenever a command such as `/worlds edit <world>` was run, the world always had to be specified
  * Now, whenever a world is not specified (`/worlds edit`) the player's current world is used
* **Improvements to `/blocks`**
  * Added invisible item frame to servers running 1.17
  * Improved rotation of orientable blocks
{% endtab %}

{% tab title="Fixed" %}
* **Allow players to rejoin server in unloaded worlds**
  * If a player has spawn teleportation deactivated and world unloading has been enabled, the world the player was previously in is now loaded automatically
{% endtab %}
{% endtabs %}

## v2.20.6 - 10.10.2022

{% tabs %}
{% tab title="Added" %}
* **Add permissions to each world type creation**&#x20;
  * Allows server owners to restrict which world types can be created
* **Allow admins to bypass a world's permission**
  * Use the admin permission: `buildsystem.admin`
{% endtab %}
{% endtabs %}

## v2.20.5 - 15.08.2022

{% tabs %}
{% tab title="Fixed" %}
* Fix `NoSuchMethodError` thrown in legacy versions
{% endtab %}
{% endtabs %}

## v2.20.4 - 02.08.2022

{% tabs %}
{% tab title="Fixed" %}
* Don't use `StringUtils` from `apache commons lang3`
{% endtab %}

{% tab title="Changed" %}
* Switch from Spigot 1.19 to 1.19.1 as API version
{% endtab %}
{% endtabs %}

## v2.20.3 - 04.07.2022

{% tabs %}
{% tab title="Fixed" %}
* Fix "Double Stone Slab" block being placed incorrectly (Minecraft 1.14+)
* Show archived private worlds in world archive
{% endtab %}
{% endtabs %}

## v2.20.2 - 03.07.2022

{% tabs %}
{% tab title="Added" %}
* Added piston head block to `/blocks`
{% endtab %}

{% tab title="Fixed" %}
* When editing gamerules in a world (`/worlds edit`), the next page button should now work as intended in versions <1.13
{% endtab %}
{% endtabs %}

## v2.20.1 - 15-06.2022

{% tabs %}
{% tab title="Fixed" %}
* Update notifier displayed incorrect version
{% endtab %}
{% endtabs %}

## v2.20 - 15.06.2022

{% tabs %}
{% tab title="Added" %}
* Support for Minecraft 1.19
{% endtab %}

{% tab title="Fixed" %}
* Don't import a world twice if already existent (`/worlds importAll`)
{% endtab %}
{% endtabs %}

## v2.19 - 27.05.2022

## v2.18.9 - 21.04.2022

{% tabs %}
{% tab title="Fixed" %}
* Correctly allow multiple private worlds to be created
{% endtab %}
{% endtabs %}

## v2.18.8 - 21.04.2022

{% tabs %}
{% tab title="Changed" %}
* From now on, only the creator of a world can delete it (or players with the admin permission: `buildsystem.admin`)
* Players are no longer limited to one private world. Use the permission `buildsystem.create.private.<amount>` to set the maximum amount a player can create
{% endtab %}

{% tab title="Fixed" %}
* Fixes a bug where creators could not add builders to their world with `/worlds addBuilder`
{% endtab %}
{% endtabs %}

## v2.18.7 - 12.04.2022

{% tabs %}
{% tab title="Changed" %}
* **Navigator permission changes**
  * Changes the permission needed to open the navigator to `buildsystem.navigator`
  * Adds a permission which is needed to receive the navigator item: `buildsystem.navigator.item`
{% endtab %}

{% tab title="Fixed" %}
* **Fixed bugs with the modern navigator**
  * Item used to close navigator could be dropped
  * Players were able to modify other player's navigator leaving them unusable
* **Minor optimisation**
  * Reset unload task after world switch (or quitting) to ensure correct unload time
{% endtab %}
{% endtabs %}

## v2.18.6 - 30.03.2022

{% tabs %}
{% tab title="Changed" %}
* **Changes to world difficulty**
  * Allow a world's difficulty to be changed in the `/worlds edit <world>` menu
  * Correctly retrieve the default world difficultly from the config
{% endtab %}

{% tab title="Fixed" %}
* **Allow unloaded worlds to be renamed**
  * Previously, a world had to be imported in order for it to be renamed
{% endtab %}
{% endtabs %}

## v2.18.5 - 29.03.2022

{% tabs %}
{% tab title="Fixed" %}
* **Fix incorrect chunk generator when loading worlds**
  * Worlds that were unloaded and then loaded again were using the standard `WorldCreator`, not the custom generators they should be
{% endtab %}
{% endtabs %}

## v2.18.4 - 21.03.2022

{% tabs %}
{% tab title="Fixed" %}
* Fixed an error in legacy versions (< 1.13) where normal blocks could not be broken when slab breaking was enabled
{% endtab %}
{% endtabs %}

## v2.18.3 - 20.03.2022

{% tabs %}
{% tab title="Fixed" %}
* Some listeners were registered twice
* `Instant Place Signs` would not work with `Material#DARK_OAK_SIGN`
* Unloaded worlds were not being deleted correctly
* `/settings` would throw a NPE when using Minecraft versions < 1.13
{% endtab %}
{% endtabs %}

## v2.18.2 - 11.03.2022

{% tabs %}
{% tab title="Added" %}
* **Added new config option: `teleport-after-creation` (default: `true`)**
  * When enabled, the player is teleported a world after it is created instead of having to enter through the navigator
{% endtab %}

{% tab title="Fixed" %}
* Chunks in void worlds were not generated correctly after the server restarts
{% endtab %}
{% endtabs %}

## v2.18.1 - 06.03.2022

{% tabs %}
{% tab title="Added" %}
* **Support for Minecraft 1.18.2**
{% endtab %}

{% tab title="Fixed" %}
* Sending commands that use `CommandSender#spigot` throws `NoSuchMethodError`
* `NullPointerException` while opening GameRule inventory
* Navigator does not stay in inventory when „Keep Navigator“ is enabled
{% endtab %}
{% endtabs %}

## v2.18 - 15.02.2022

**Full changelog:** [https://github.com/einTosti/BuildSystem/releases/tag/2.18](https://github.com/einTosti/BuildSystem/releases/tag/2.18)

{% tabs %}
{% tab title="Added" %}
* Support for RGB messages
* Implement `buildsystem:role` Context for LuckPerms
* Add limits to the amount of worlds allowed to be created
{% endtab %}
{% endtabs %}

## v2.17.2 - 16.01.2022

{% tabs %}
{% tab title="Added" %}
* **Expand PlaceholderAPI expansion**
  * Add placeholders for player-settings
  * Full list of (newly introduced) placeholders can be found here: [https://buildsystem.eintosti.com/placeholders#settings-placeholders](https://buildsystem.eintosti.com/placeholders#settings-placeholders)
{% endtab %}

{% tab title="Fixed" %}
* Worlds can no longer have a blank name when only consisting of special characters
* Stop items from trying to be placed with "Disable Interactions" enabled
* Stop WorldEdit items from being able to break blocks when they shouldn't
{% endtab %}
{% endtabs %}

## v2.17.1 - 26.12.2021

{% tabs %}
{% tab title="Fixed" %}
* Fix WorldEdit wand breaking blocks
{% endtab %}
{% endtabs %}

## v2.17 - 09.12.2021

{% tabs %}
{% tab title="Added" %}
* Support for Minecraft 1.18
{% endtab %}

{% tab title="Fixed" %}
* Bugs with lower versions. If any still occur, please report them on [GitHub](https://github.com/einTosti/BuildSystem/issues)
{% endtab %}
{% endtabs %}

## v2.16.6 - 26.11.2021

{% tabs %}
{% tab title="Fixed" %}
* NoClassDefFoundError with `/worlds help`
{% endtab %}
{% endtabs %}

## v2.16.5 - 25.11.2021

{% tabs %}
{% tab title="Added" %}
* Previously, only WorldEdit commands were blocked. Now the usage of brushes etc should also be blocked
{% endtab %}

{% tab title="Changed" %}
* Bug fixes
* Refactored code
{% endtab %}
{% endtabs %}

## v2.16.4 - 21.09.2021

{% tabs %}
{% tab title="Added" %}
* Added ability to unimport worlds with `/worlds unimport` (Perm: `buildsystem.unimport`)
* Added `/w` as an alias for `/worlds`
{% endtab %}

{% tab title="Fixed" %}
* Fixed bug where settings were not toggling correctly
{% endtab %}
{% endtabs %}

## v2.16.3 - 01.09.2021

{% tabs %}
{% tab title="Added" %}
* Added option to add worlds to a blacklist which ensures that they won't be unloaded (**config.yml**: `world.unload.blacklisted-worlds`)
* Added option to keep the "Navigator" on inventory clear (`/settings`)
{% endtab %}
{% endtabs %}

## v2.16.2 - 23.08.2021

{% tabs %}
{% tab title="Added" %}
* Added command to remove a world's custom spawn (**/worlds removeSpawn**)
* Added option to set a world's default difficulty to the config (**world.default.difficulty**)
{% endtab %}

{% tab title="Changed" %}
* Improved the blockage of WorldEdit commands for non-builders
* Improved **/worlds** tab-complete
* Improved **/worlds help** command
* **/config** can now be used from the console
{% endtab %}
{% endtabs %}

## v2.16.1 - 02.08.2021

{% tabs %}
{% tab title="Added" %}
* Adds option to not give navigator on join ("settings.navigator.give-item-on-join")
{% endtab %}
{% endtabs %}

## v2.16 - 26.07.2021

{% tabs %}
{% tab title="Added" %}
* **Custom world generators**
  * When creating a new world, a new icon can be found in the "World Create GUI": **Generators**
  * In order to create a world with a custom world generator, the generator plugin must be present in the "plugins" folder (and the plugins must be loaded!)
  * Then after having selected "Generators" as a world type, enter the world name and afterwards the name of the World Generator and voilà!
{% endtab %}

{% tab title="Fixed" %}
* Duplicate key in `messages.yml` bug
{% endtab %}
{% endtabs %}

## v2.15 - 22.07.2021

{% tabs %}
{% tab title="Added" %}
* Support for 1.17(.1)
{% endtab %}

{% tab title="Changed" %}
* Replaced AnvilGUI with chat input
{% endtab %}
{% endtabs %}

## v2.14.6 - 23.04.2021

{% tabs %}
{% tab title="Added" %}
* Standard settings for newly created worlds
  * e.g. physics, explosions, etc.
{% endtab %}

{% tab title="Fixed" %}
* Commands should no longer clash with other plugins
* World names in the "navigator" (!) can now include symbols
* Skulls in the "private world navigator" should consume fewer resources & load faster
* You can now place plants in flower pots while "Place Plants" is activated
{% endtab %}
{% endtabs %}

## v2.14.5 - 13.01.2021

{% tabs %}
{% tab title="Fixed" %}
* World names in /worlds can now have other characters that the world name itself​
{% endtab %}
{% endtabs %}

## v2.14.4 - 03.11.2020

{% tabs %}
{% tab title="Added" %}
* Support for Minecraft 1.16.4
{% endtab %}
{% endtabs %}

## v2.14.3 - 20.09.2020

{% tabs %}
{% tab title="Added" %}
* Added the ability to write with colors in the chat & on signs » Chat: buildsystem.color.chat » Signs: buildsystem.color.sign
{% endtab %}

{% tab title="Changed" %}
* **Restructured config**
  * Will have to be deleted after updating!
* **Improved world import**
  * The world which is supposed to be imported will now be checked for invalid characters
  * /worlds import can now be tab completed&#x20;
  * /worlds importAll now has a delay between each world (can be configured in the config, default 30s)
* **Improved NoClip**
  * The players previous gamemode is now saved
{% endtab %}
{% endtabs %}

## v2.14.2 - 18.08.2020

## v2.14.1 - 15.08.2020

{% tabs %}
{% tab title="Fixed" %}
* The navigator should now work as expected in 1.16+
* Fixed `back_usage` message error (only for newly generated messages.yml files)​
{% endtab %}
{% endtabs %}

## v2.14 - 14.08.2020

## v2.13.3 - 09.06.2020

{% tabs %}
{% tab title="Added" %}
* /spawn \[set/remove] & /config \<reload> can now be tab-completed
{% endtab %}

{% tab title="Fixed" %}
* The spawn (/spawn) can no longer be set in a world which is not imported
{% endtab %}
{% endtabs %}

## v2.13.2 - 02.06.2020

## v2.13.1 - 23.05.2020

{% tabs %}
{% tab title="Added" %}
* Added sounds to the "World Editor" and the "Builders" GUI
{% endtab %}

{% tab title="Changed" %}
* **Improvement to the "World Editor"**
  * After changing a world's permission or project via the "World Editor" you are now brought back to the GUI instead of the GUI just closing
  * Improved messages (information about world status, permission & project)
    * In order to see these changed messages.yml must be deleted (or at least all messages with " "worldeditor\_" in them)
{% endtab %}
{% endtabs %}

## v2.13 - 22.05.2020

{% tabs %}
{% tab title="Added" %}
* **New setting: Place plants**
  * When enabled, plants can be placed n all kinds of blocks
* **World editor**
  * Easily customise worlds with a GUI » Can be opened with /worlds edit  or by right-clicking a word in the world navigator
  * World must be loaded to use the editor!
  * Features:
    * Toggle block breaking/placement/physics
    * Alter the time of day
    * Toggle explosions
    * Butcher all mobs in a world
    * Manage builders (more to that later)
    * Manage gamerules
    * Toggle world visibility (if a world is shown in "Private Worlds")
    * Toggle MobAIs
    * Change a world's status/project/permission
* **Introducing builders**
  * When a world has builders enabled (private worlds by default, public worlds after being enabled), only these players can place and destroy blocks
  * A list of a world's builder can be seen in the world editor or with /worlds builders  (Permission: worlds.builders)&#x20;
  * Add a builder in the world editor or with /worlds addBuilder  (Permission: worlds.addbuilder)
  * Remove a builder in the world editor or with /worlds removeBuilder  (Permission: worlds.removebuilder)
  * Only the world creator can add or remove builders! (Set the creator with /worlds setCreator )&#x20;
  * Can be disabled in the config (block-world-edit-non-builder)
* **Admin bypass permission**
  * Permission: buildsystem.admin
  * Bypasses all restrictions such as not being the creator of a world, archived worlds, disabled block breaking/placement
* **New /worlds info placeholders**
  * Added %builders\_enabled%, %block\_breaking% & %block\_placement%
  * Shows whether or not a certain world has the builder feature enabled and whether or not blocks can be placed/broken
{% endtab %}
{% endtabs %}

## v2.12.2 - 17.05.2020

{% tabs %}
{% tab title="Fixed" %}
* Powered Redstone Lamps are now lit, even when physics are disabled
* "Disabled Interact" should again work as expected
{% endtab %}
{% endtabs %}

## v2.12.1 - 10.05.2020

{% tabs %}
{% tab title="Added" %}
* **Update checker**
  * Automatically checks for updates when the server starts/reloads
  * Players who have the permision "buildsystem.update" (default: op) are also notified of join
  * Can be disabled in the config (update-checker)
* **Additions to /speed**
  * /s as an alias for /speed
  * /speed (/s) can now be tab-completed
{% endtab %}

{% tab title="Fixed" %}
* When placing the "Powered Redstone Lamp", the block above would lose its colour&#x20;
* Private world would disappear when set to archive (now shown in the "World Archive")
* Now all block interactions should be cancelled when "Disable Interactions" is enabled
{% endtab %}
{% endtabs %}

## v2.12 - 07.05.2020

{% tabs %}
{% tab title="Added" %}
* **More settings**
  * Instant Place Signs: Allows for signs to be placed without the menu opening
  * Player hider: Hide/show all players&#x20;
* **Custom import generators**
  * When importing worlds you can now choose from 3 generators: NORMAL, FLAT, VOID (default)
  * /world import  \[-g ]
* **Implemented bStats**
  * Gives me information on how the plugin is used, so I can improve it more
* **Toggle join/quit messages**
  * Option found in the config: join-quit-messages (default: true)
* **Toggle block in void worlds**
  * You can now toggle whether or not a gold block is placed in a void world when it is created
  * Option found in the config: void-block (default: true)
{% endtab %}

{% tab title="Changed" %}
* **Improved navigator**
  * Now contains settings (/settings command will still continue to exist)
* **"Slab Breaking"**&#x20;
  * Smooth Stone, Smooth Sandstone & Smooth Red Sandstone blocks (found in /blocks) are now fully broken when "Slab Breaking" is enabled
{% endtab %}
{% endtabs %}

## v2.11.1 - 05.05.2020

{% tabs %}
{% tab title="Fixed" %}
* Fixed a bug where the second page of the "World Archive" couldn't be opened
{% endtab %}
{% endtabs %}

## v2.11 - 04.05.2020

{% tabs %}
{% tab title="Added" %}
* **/worlds setStatus GUI can now be customized**
  * Use /setup and proceed the same as with changing the other default item
{% endtab %}

{% tab title="Changed" %}
* **Improved /worlds delete**
  * World deletion must now be confirmed (No more accidental deletes)
  * Therefore you can now tab-complete /worlds delete
* **Redesigned "World Create GUI"**
  * Check it out for yourself
{% endtab %}
{% endtabs %}

## v2.10 - 23.04.2020

{% tabs %}
{% tab title="Added" %}
* **Added the option the clear a player's inventory on join**
  * Can be toggled with /settings (default: disabled)
* **Worlds can now be unloaded**
  * After X amount of time, a world is unloaded if a player hasn't entered the world since then (default is 1h)
  * First enable the option in the config (unload-worlds)
  * If you want to you can change the time until the world is unloaded (time-until-unload)
  * Then reload the server
* **Worlds can now be sorted in more ways**
  * Added "Z-A" and "oldest first"
* **The scoreboard can now be disabled in the config**
{% endtab %}

{% tab title="Changed" %}
* Improved deletion of worlds
{% endtab %}

{% tab title="Fixed" %}
* Blocks will now be coloured when "Disabled Interactions" is enabled
* Fixed some other small bugs
{% endtab %}
{% endtabs %}

## v2.9 - 04.04.2020

{% tabs %}
{% tab title="Added" %}
* **/setup** &#x20;
  *   Changes the items which   &#x20;

      a) are shown in the GUI when you create a world   &#x20;

      b) are given to specific worlds by default (e.g.             Normal world is a log) &#x20;
  * Permission: buildsystem.setup
{% endtab %}
{% endtabs %}

## v2.8.1 - 25.03.2020

{% tabs %}
{% tab title="Fixed" %}
* Fixed a bug where worlds wouldn't load if they had a dot in their name
{% endtab %}
{% endtabs %}

## v2.8 - 21.03.2020

{% tabs %}
{% tab title="Added" %}
* **Spawn system**
  * Use /spawn set to set a spawn where all players will be teleported to (if they wish) when they join the server or use /spawn » Remove the spawn with /spawn remove
  * Permission needed: buildsystem.spawn
* **New settings**
  *   There are now 2 new options in /settings&#x20;

      1\) Toggle block interactions:&#x20;

      * When block interactions are deactivated you can place blocks against certain blocks (e.g. furnace, crafting table, chest, etc.) without opening them
      * This function works best in Spigot 1.13+ because blocks won't rotate when place in versions below

      2\) Toggle spawn teleportation

      * If players don't want to be teleported to the spawn, they can disable this
* **World information**
  * /worlds info \[world] gives you information about a world
  * Permission: worlds.info
* **Fast enable physics**
  * /physics all quickly enables world physics in all worlds, as long as there isn't a world names "all"
{% endtab %}

{% tab title="Fixed" %}
* Fixed a huge ton of bugs
{% endtab %}
{% endtabs %}

## v2.7 - 01.03.2020

{% tabs %}
{% tab title="Added" %}
* **More world information**&#x20;
  * Newly created world from now on store the world creator and creation date/time
    * World Creator: %creator%
    * Creation date/time: %date%
  * These new placeholders can be used in the scoreboard and in the world navigator lore
  * The world creator can be changed with /worlds setCreator
  * The date format can be changed in the config
* **Option to change how worlds are sorted in the navigator**
  * Choose between Alphabetically and Creation date
  * Can be changed with /settings
{% endtab %}

{% tab title="Changed" %}


* **Updated mechanics**&#x20;
  * The config is now automatically reloaded when the server reloads&#x20;
  * You can now add unlimited lines to a lore in messages.yml
  * Changed other internal things
* **Improved private worlds**&#x20;
  * Private worlds are no longer just flat worlds
  * Now you can choose between all the "normal" worlds types (Normal, Flat, Void, Nether & End)
* **Other changes**&#x20;
  * Redesigned /settings GUI
  * The scoreboard and prefix are now stored in messages.yml, no longer in the config
{% endtab %}
{% endtabs %}

## v2.6.2 - 26.02.2020

{% tabs %}
{% tab title="Fixed" %}
* Fixed a bug where /worlds setStatus threw an error in Spigot versions <1.13
{% endtab %}
{% endtabs %}

## v2.6.1 - 23.01.2020

{% tabs %}
{% tab title="Fixed" %}
* Bug fix
{% endtab %}
{% endtabs %}

## v2.6 - 04.01.2020

{% tabs %}
{% tab title="Added" %}
* **Added "Nether" & "End" worlds**
  * To create such a world just click on the corresponding items when creating a world: End stone (End) and Netherrack (Nether)
{% endtab %}
{% endtabs %}

## v2.5.1 - 01.01.2020

{% tabs %}
{% tab title="Added" %}
* **Forgot to add the new commands to /buildsystem**\
  » Added /explosions and /noai
{% endtab %}
{% endtabs %}

## v2.5 - 30.12.2019

{% tabs %}
{% tab title="Added" %}
* **Disable entity AIs**&#x20;
  * Use /noai \[world] to disable entity AIs&#x20;
  * Permission: buildsystem.noai
* **Disable explosions**&#x20;
  * Use /explosions \[world] to disable explosions&#x20;
  * Permission: buildsystem.explosions
{% endtab %}
{% endtabs %}

## v2.4 - 15.12.2019

{% tabs %}
{% tab title="Added" %}
* **Added support for 1.13-1.15**
  * BuildSystem now support all versions from 1.8-1.15
  * It is not wise to load worlds from newer versions (e.g. 1.15) in older versions (e.g. 1.8)!
{% endtab %}

{% tab title="Other" %}
* **Other bug fixes, changes and new features**
  * The list of everything that has changed is too long to put here, so you can find them out yourselves ;)
{% endtab %}
{% endtabs %}

## v2.3.3 - 18.11.2019

{% tabs %}
{% tab title="Added" %}
* **Added "Burning Furnace"**
  * Always lit furnace in /blocks​
{% endtab %}

{% tab title="Fixed" %}
* Fixed a bug concerning custom spawns​
{% endtab %}
{% endtabs %}

## v2.3.2 - 16.11.2019

{% tabs %}
{% tab title="Fixed" %}
* Pitch and Yaw are no longer swapped in custom spawns
* Other smaller bug fixes​
{% endtab %}
{% endtabs %}

## v2.3.1 - 15.11.2019

{% tabs %}
{% tab title="Added" %}
* **More scoreboard placeholders**&#x20;
  * Added %permission% and %project% as variables that can be used in the scoreboard
{% endtab %}

{% tab title="Changed" %}
* /config reload now refreshes the scoreboard instantly​
{% endtab %}
{% endtabs %}

## v2.3 - 14.11.2019

{% tabs %}
{% tab title="Added" %}
* **Custom Spawnpoints**
  * You can now set the spawnpoint of each world with /worlds setSpawn&#x20;
  * Permission: buildsystem.setspawn​
{% endtab %}
{% endtabs %}

## v2.2 - 03.11.2019

{% tabs %}
{% tab title="Added" %}
* **Recoded scoreboard**
  * Now uses packets, shouldn't flicker anymore
* **Added the option to disable vanish in archived worlds**
  * Can be toggled in the config \[Reload config with /config reload!]​
* **/skull \<ID> now gives you a skull with a custom ID**
  * Get ID from [http://textures.minecraft.net/texture/](http://textures.minecraft.net/texture/)\<ID>​
{% endtab %}

{% tab title="Fixed" %}
* Removed bug where multiple scoreboard were shown at the same time​
* Blocks and armor stands can no longer be interacted with if they are in an archived world
{% endtab %}
{% endtabs %}

## v2.1.1 - 23.10.2019

{% tabs %}
{% tab title="Fixed" %}
* Fixed a (yes another) scoreboard bug​
{% endtab %}
{% endtabs %}

## v2.1 - 23.10.2019

{% tabs %}
{% tab title="Added" %}
* **Overview of all commands**
  * /buildsystem now gives you an overview of all commands
  * Only the commands of which you have the permission for are shown
{% endtab %}

{% tab title="Changed" %}
* Fixed a bug with the scoreboard » Added a few messages I had forgotten​
{% endtab %}
{% endtabs %}

## v2.0 - 22.10.2019

{% tabs %}
{% tab title="Added" %}
* **Custom messages**
  * You now have the option to change all of the plugin messages&#x20;
  * Messages are found in the messages.yml file​
{% endtab %}

{% tab title="Changed" %}
* Improved the 'new navigator': is now more responsive
* Fixed spellings mistakes
* Fixed some bugs
* Refactored lots of code
{% endtab %}
{% endtabs %}

## v1.8 - 10.10.2019

{% tabs %}
{% tab title="Added" %}
* **Added Scoreboard**
  * Text can be altered in the config
  * Can be enabled/disabled with /settings
{% endtab %}
{% endtabs %}

## v1.7.2 - 03.10.2019

{% tabs %}
{% tab title="Fixed" %}
* Fixed a bug where the player received the wrong block with /blocks​\

{% endtab %}
{% endtabs %}

## v1.7.1 - 28.09.2019

{% tabs %}
{% tab title="Added" %}
* **Added "Powered Redstone Lamp" block**
  * "Redstone Lamp" that always is lit
  * You can find the block in /blocks
{% endtab %}
{% endtabs %}

## v1.7 - 03.08.2019

{% tabs %}
{% tab title="Added" %}
* **Introducing: Templates**
  * Templates are a new and easy way to create worlds
  * Copy the template you want added into the game into the "templates" folder
  * Then when choosing to create a word you can choose between Predefined Worlds and Templates
{% endtab %}
{% endtabs %}

## v1.6.4 - 30.07.2019

{% tabs %}
{% tab title="Changed" %}
* Refactored some code
{% endtab %}

{% tab title="Fixed" %}
* Fixed a bug where the default join/quit messages weren't displayed correctly (without colour)
{% endtab %}
{% endtabs %}

## v1.6.3 - 09.07.2019

{% tabs %}
{% tab title="Fixed" %}
* Fixed a bug when not having the "buildsystem.gui" permission
{% endtab %}
{% endtabs %}

## v1.6.2 - 24.03.2019

{% tabs %}
{% tab title="Added" %}
* **Added permission**
  * New permission: buildsystem.gui
  * Enabled by default
  * Permission needed to open the "Worlds-GUI"​
{% endtab %}
{% endtabs %}

## v1.6.1 - 26.02.2019

{% tabs %}
{% tab title="Changed" %}
* **Small change**
  * Added /worlds setStatus \<world> to /worlds help
* **Refactored code**
{% endtab %}

{% tab title="Fixed" %}
* Fixed NoClip
{% endtab %}
{% endtabs %}

## v1.6 - 14.10.2018

{% tabs %}
{% tab title="Added" %}
* **Added two new blocks**
  * "Nether Portal"
  * "End Portal"​
{% endtab %}

{% tab title="Changed" %}
* When renaming a world, it's previous name is already in the anvil
* Refactored some code​
{% endtab %}

{% tab title="Fixed" %}
* Fixed a bug when renaming worlds​
{% endtab %}
{% endtabs %}

## v1.5.1 - 06.10.2018

{% tabs %}
{% tab title="Changed" %}
* **Improved /worlds "Help-Message"**
  * Clickable messages: Auto suggests command
  * Hoverable messages: Shows the permission needed to run the command
{% endtab %}
{% endtabs %}

## v1.5 - 01.10.2018

{% tabs %}
{% tab title="Added" %}
* **Rename worlds**
  * Use /worlds rename \<world> to rename a world
  * Permission: buildsystem.rename​\

{% endtab %}

{% tab title="Changed" %}
* Skulls in the private worlds GUI now have the texture of their player
* Small changes to creating worlds, changing permissions & changing statuses
{% endtab %}
{% endtabs %}

## v1.4 - 25.09.2018

{% tabs %}
{% tab title="Added" %}
* **Custom colours**
  * In /settings, each player now has the opportunity to change the glass colour in all of the GUIs
{% endtab %}
{% endtabs %}

## v1.3.1 - 21.09.2018

{% tabs %}
{% tab title="Fixed" %}
* Fixed a incorrectly named sub-command (/worlds setProject)​
{% endtab %}
{% endtabs %}

## v1.3 - 20.09.2018

{% tabs %}
{% tab title="Added" %}
* Added more blocks to /blocks
{% endtab %}
{% endtabs %}

## v1.2 - 13.09.2018

{% tabs %}
{% tab title="Added" %}
* Added tab complete to /day and /night​
{% endtab %}

{% tab title="Changed" %}
* Recoded the current tab completes
{% endtab %}
{% endtabs %}

## v1.1 - 11.09.2018

{% tabs %}
{% tab title="Changed" %}
* **Improved physics command**&#x20;
  * You can now use /physics to toggle block physics in other worlds (/physics \[world])
  * You can now tab complete worlds
* **Improved world switching**
  * You can now only enter a world if you have it's permission
  * But players can always join the default world or worlds with their permission set to "-"​
{% endtab %}
{% endtabs %}

## v1.0.2 - 10.09.2018

{% tabs %}
{% tab title="Changed" %}
* **Change to finished & archived worlds**
  * When entering worlds that have been set to have the archive status, the player will now not be able to build or break blocks in the world (was previously finished)
  * Worlds that have been set to have the finished status, act like "normal" worlds again
{% endtab %}
{% endtabs %}

## v1.0.1 - 09.09.2018

{% tabs %}
{% tab title="Changed" %}
* **Improved the creation of worlds**
* **When a world is created, the standard time is now 6000 ticks**
* **Refactored code**
  * Changed the way the config are created
  * Cleaned up some code​
{% endtab %}

{% tab title="Fixed" %}
* Fixed errors when interacting with worlds not registered by the plugin
* Fixed errors when creating worlds​
{% endtab %}
{% endtabs %}

## v1.0 - 09.09.2018

{% hint style="info" %}
Inital release
{% endhint %}
