---
description: >-
  World Folders are an improved way of managing how worlds are stored within the
  navigator.
---

# folder

## Creating a folder

Folder creation is done [via the navigator](../../getting-started/creating-a-folder.md#creating-a-new-folder).

### Permission

```
buildsystem.create.folder
```

## Adding worlds to a folder

{% hint style="warning" %}
A world can only be in one folder at a time.
{% endhint %}

### Usage

```
/worlds folder <folder> add <world>
```

### Permission

```
buildsystem.folder.add
```

## Removing worlds from a folder

### Usage

```
/worlds folder <folder> remove <world>
```

### Permission

```
buildsystem.folder.remove
```

## Deleting a folder

{% hint style="warning" %}
A folder can only be deleted after all contained worlds have been removed.
{% endhint %}

### Usage

```
/worlds folder <folder> delete
```

### Permission

```
buildsystem.folder.delete
```

## Setting a folder's permission

### Usage

```
/worlds folder <folder> setPermission
```

### Permission

```
buildsystem.folder.setpermission
```

## Setting a folder's project

### Usage

```
/worlds folder <folder> setProject
```

### Permission

```
buildsystem.folder.setproject
```

## Setting a folder's navigator icon

### Usage

```
/worlds folder <folder> setItem
```

### Permission

```
buildsystem.folder.setitem
```
