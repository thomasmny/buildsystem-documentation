---
description: When LuckPerms is installed, BuildSystem adds extra contexts
---

# LuckPerms Context

## Contexts

<table><thead><tr><th width="167">Context Key</th><th width="397">Description</th><th>Values</th></tr></thead><tbody><tr><td><code>build-mode</code></td><td>Whether the player is in build-mode (<code>/build</code>)</td><td><code>true</code>, <code>false</code></td></tr><tr><td><code>role</code></td><td>The player's role in the current world</td><td><code>creator</code>, <code>builder</code>, <code>guest</code></td></tr></tbody></table>

## Example

> You want players who are guests in a world (neither _creator_ nor _builder_) to remain in the gamemode they currently are in.

Now you can use the following context: `/lp user <user> permission set buildsystem.gamemode false buildsystem:role=guest`
