# Caura Scoop bucket

## Install

```powershell
scoop bucket add caura-ai https://github.com/caura-ai/scoop-bucket
scoop install caura-ai/caura
caura --version
```

To upgrade Caura later, run `scoop update caura`.

## Moving from the old package name

Scoop cannot automatically migrate an installation under the old `memclaw`
package name because it does not support same-bucket renames. Before
uninstalling it, confirm that your existing Caura state directory is intact and
back it up. Then uninstall the old package and install the current one:

```powershell
scoop uninstall memclaw
scoop update
scoop install caura-ai/caura
```

This replaces the Scoop package only; it does not automatically move or rename
your state directory.

Manifests are auto-published by GoReleaser from the `caura-daemon` release
workflow on each stable release.
