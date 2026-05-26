# Verify HDEX Q1 Release

This page explains how to verify the HDEX Q1 v0.1.0 Windows offline release.

## Trusted Public Key Fingerprint

```text
634e5b1771b549e9f64f5e5b079b3754fde4b47bd687dbbf8ecc837e6e7072f5
```

## Verify ZIP Hash

After downloading:

```powershell
Get-FileHash .\HDEX_Q1_0.1.0_Windows_Offline_Production_Assisted.zip -Algorithm SHA256
```

Expected:

```text
27fe306d86e6b0c06da50e2c1a78bfa78db3cd1d7f9572db0c243a71257c5bf6
```

## Verify Extracted Bundle

Extract the ZIP, open PowerShell inside `01_HDEX_Q1`, then run:

```powershell
.\hdex.exe --version
```

Verify release signature:

```powershell
.\hdex.exe release verify `
  --bundle . `
  --trusted-key-fingerprint 634e5b1771b549e9f64f5e5b079b3754fde4b47bd687dbbf8ecc837e6e7072f5 `
  --offline `
  --json
```

Verify bundle integrity:

```powershell
.\hdex.exe bundle verify `
  --bundle . `
  --trusted-key-fingerprint 634e5b1771b549e9f64f5e5b079b3754fde4b47bd687dbbf8ecc837e6e7072f5 `
  --offline `
  --json
```

Expected successful verification output:

```json
"status": "verified"
```

If verification fails, do not run the executable. Re-download from the official HDEX website or GitHub release mirror and compare hashes again.
