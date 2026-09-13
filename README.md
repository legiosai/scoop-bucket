# scoop-bucket

The [scoop](https://scoop.sh) bucket for [Legios](https://github.com/legiosai)
tools.

```powershell
scoop bucket add legios https://github.com/legiosai/scoop-bucket
scoop install quartermaster
```

## What's in here

| | |
|---|---|
| [**quartermaster**](https://github.com/legiosai/quartermaster) | How much quota you have left, in every agent account on the machine: every Claude Code profile, plus Codex and opencode. |

## How it gets updated

Nobody edits these by hand. Tagging a release in the tool's own repository runs
its release workflow, which builds the artifacts, publishes them, and pushes the
manifest here with the hashes of what it just built.

That is the whole point of doing it that way: a manifest edited by hand is a
manifest that drifts, and the drift is invisible until someone installs an old
version.

Each manifest also carries `checkver` and `autoupdate`, so scoop's own bot can
follow along.
