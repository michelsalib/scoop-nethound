# Scoop bucket for nethound

[nethound](https://github.com/michelsalib/nethound) shows which process (or container) listens on each
port, who can reach it, who is connected to it, and how everything on your machine connects.

```powershell
scoop bucket add nethound https://github.com/michelsalib/scoop-nethound
scoop install nethound/nethound
```

This installs the standalone `nethound.exe` from the GitHub release. Update with
`scoop update nethound`. Run it from an administrator terminal to see other users' command lines too.

For completion (commands, options, and for `who` and `kill` the ports listening now), add this line to
your PowerShell profile (`notepad $PROFILE`):

```powershell
nethound completion powershell | Out-String | Invoke-Expression
```

nethound was called netbeagle up to 0.7.0, and this bucket scoop-netbeagle. `netbeagle.json` stays at
0.8.0, which says how to switch: `scoop uninstall netbeagle`, then the two lines above.

`bucket/nethound.json` is generated for each release by `scripts/packages.ts` in the nethound
repository, from the release's `SHA256SUMS`.
