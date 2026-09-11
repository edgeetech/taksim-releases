# Windows installation

## Install Taksim v0.1.0

Download the installer from the public release, then run it from PowerShell:

```powershell
Invoke-WebRequest `
  -Uri 'https://github.com/edgeetech/taksim-releases/releases/download/v0.1.0/install-release.ps1' `
  -OutFile '.\install-release.ps1'

.\install-release.ps1 `
  -Repository edgeetech/taksim-releases `
  -Version 0.1.0
```

The SHA-256 digest of the v0.1.0 installer is:

```text
cba84510dc47e305116d10c41d2e9196d95f58bdb01c13ed03b9b776304a8aeb
```

The installer downloads the selected release archive and `SHA256SUMS.txt` over
HTTPS, checks the archive against the matching checksum entry, extracts it into
a version-specific directory under `%LOCALAPPDATA%\Taksim`, validates the
binary, and only then switches the `current` installation link.

Canonical user data is stored separately under `%USERPROFILE%\.taksim`. The
installer changes the versioned binary installation and does not remove or
replace that user-data directory.

## Verify the installation

Open a new PowerShell terminal and run:

```powershell
taksim version
taksim doctor
taksim install status
taksim claude --version
taksim codex --version
```

The final two commands verify managed-client launch wiring without sending a
paid inference request.
