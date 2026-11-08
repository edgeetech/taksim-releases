# Taksim Releases

> **Taksim is closed as a commercial product.** Its predeclared benchmark tests
> showed that routing did not beat a fixed Sonnet default, and we honoured the
> result. Read why: [Closing Taksim](https://asozyurt.com/writing/closing-taksim/)
> ([Türkçe](https://asozyurt.com/writing/taksim-kapanis/)). Benchmark results:
> [taksim.edgee.tech/benchmark](https://taksim.edgee.tech/benchmark/).
>
> The releases in this repository are kept for reference only. They are unsigned
> and unsupported: no further releases, fixes or security updates are planned.
> The code will be made public soon.

This repository was the public distribution channel for official Taksim binaries,
installers, and checksums. Application source code and private engineering data are
not published here.

## Installing an archived release (reference only)

The command below still works, but it installs an unsigned, unsupported release.
In PowerShell (Windows, no admin needed):

```powershell
irm https://github.com/edgeetech/taksim-releases/releases/latest/download/install.ps1 | iex
```

This installs the latest release and runs `taksim setup`. Reference docs:
[Quick start](https://taksim.edgee.tech/docs/quick-start/).

See [Windows installation and verification](INSTALLATION.md) for pinned versions,
offline installs, checksum verification, and the data-preservation boundary.

All releases: [Releases](https://github.com/edgeetech/taksim-releases/releases).

Documentation (reference): [taksim.edgee.tech](https://taksim.edgee.tech/)

Privacy: [taksim.edgee.tech/privacy](https://taksim.edgee.tech/privacy)

Terms: [taksim.edgee.tech/terms](https://taksim.edgee.tech/terms)
