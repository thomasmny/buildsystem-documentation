# Creating Worlds

## Public worlds

In order to create a _public_ world the following permission is needed:

```
buildsystem.create.public
```

Set the maximum amount of _public_ worlds a player can create with

```
buildsystem.create.public.<amount>
```

## Private worlds

In order to create a _private_ world the following permission is needed:

```
buildsystem.create.private
```

Set the maximum amount of _private_ worlds a player can create with

```
buildsystem.create.private.<amount>
```

## Type restrictions

Allows server owners to restrict which world types can be created

| Normal | <pre><code>buildsystem.create.type.normal
</code></pre> |
| ------ | ------------------------------------------------------- |
| Flat   | <pre><code>buildsystem.create.type.flat
</code></pre>   |
| Nether | <pre><code>buildsystem.create.type.nether
</code></pre> |
| End    | <pre><code>buildsystem.create.type.end
</code></pre>    |
| Void   | <pre><code>buildsystem.create.type.void
</code></pre>   |
