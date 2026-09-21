# Caura Scoop bucket

> **This bucket is retired. 0.11.0 is its final release.**
>
> Automated publishing was removed from the `caura-daemon` release workflow on
> 2026-09-09, so no version after 0.11.0 will appear here. 0.11.0 was pinned
> manually so that anyone already installed gets one last upgrade — it is the
> first release whose artifacts carry the `caura` name.
>
> Move to a supported channel when convenient: `npx caurad` or `uvx caurad`.
> See <https://caura.ai> for the current install guide.

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

Manifests were auto-published by GoReleaser from the `caura-daemon` release
workflow until 2026-09-09, when that configuration was removed. The 0.11.0
manifest was written by hand as the final release; nothing regenerates it.
