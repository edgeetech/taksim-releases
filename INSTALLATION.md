# Windows installation

## Install the latest release

In PowerShell (Windows PowerShell 5.1 or PowerShell 7, no admin needed):

```powershell
irm https://github.com/edgeetech/taksim-releases/releases/latest/download/install.ps1 | iex
```

The installer resolves the latest release, downloads `taksim-connector-win-x64.zip`,
`SHA256SUMS.txt` and `install-release.ps1` over HTTPS, verifies the archive and
`install-release.ps1` against `SHA256SUMS.txt` (it refuses to continue if an entry is
missing or does not match), installs into a version-specific directory under
`%LOCALAPPDATA%\Taksim`, switches the `current` link only after the binary validates,
adds Taksim to your user PATH, and runs `taksim setup`.

Rerun the same command, or run `taksim update --apply`, to upgrade. Continue with the
[Quick start](https://taksim.edgee.tech/docs/quick-start/).

### Options

Pin a version or skip setup:

```powershell
& ([scriptblock]::Create((irm https://github.com/edgeetech/taksim-releases/releases/latest/download/install.ps1))) -Version vX.Y.Z -NoSetup
```

### Offline or manual install

Download `install-release.ps1`, `taksim-connector-win-x64.zip` and `SHA256SUMS.txt`
from the same [release](https://github.com/edgeetech/taksim-releases/releases), check
them against `SHA256SUMS.txt` (`Get-FileHash <file> -Algorithm SHA256`), then run:

```powershell
.\install-release.ps1 -ArtifactPath .\taksim-connector-win-x64.zip -ChecksumPath .\SHA256SUMS.txt
```

## Your data

Canonical user data is stored separately under `%USERPROFILE%\.taksim`. The installers
change only the versioned binary installation and never remove or replace that
directory.

## Verify the installation

Open a new PowerShell terminal and run:

```powershell
taksim version
taksim doctor
taksim install status
```
