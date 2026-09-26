# Taksim Releases

This repository is the public distribution channel for official Taksim binaries,
installers, and checksums. Application source code and private engineering data are
not published here.

## Install

In PowerShell (Windows, no admin needed):

```powershell
irm https://github.com/edgeetech/taksim-releases/releases/latest/download/install.ps1 | iex
```

This installs the latest release and runs `taksim setup`. Rerun it, or run
`taksim update --apply`, to upgrade. Next steps:
[Quick start](https://taksim.edgee.tech/docs/quick-start/).

See [Windows installation and verification](INSTALLATION.md) for pinned versions,
offline installs, checksum verification, and the data-preservation boundary.

All releases: [Releases](https://github.com/edgeetech/taksim-releases/releases).

Documentation: [taksim.edgee.tech](https://taksim.edgee.tech/)

Privacy: [taksim.edgee.tech/privacy](https://taksim.edgee.tech/privacy)

Terms: [taksim.edgee.tech/terms](https://taksim.edgee.tech/terms)
