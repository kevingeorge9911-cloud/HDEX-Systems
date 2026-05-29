---
name: Verification failure
about: Report failed hash, signature, release, bundle, or fingerprint verification
title: "[Verification]: "
labels: verification
assignees: ""
---

## Summary

Describe the verification problem clearly.

## Release Asset Used

- ZIP filename:
- FINAL_HASHES filename:
- Download source:
- HDEX Q1 version:

## Verification Step That Failed

Select the failed step:

- [ ] ZIP hash check
- [ ] FINAL_HASHES check
- [ ] Version check
- [ ] Release verification
- [ ] Bundle verification
- [ ] Trusted fingerprint validation
- [ ] Other

## Command Used

```powershell
Paste the command here.
```

## Output

```text
Paste non-sensitive output here.
```

## Expected Result

```json
"status": "verified"
```

## Actual Result

Explain what happened instead.

## Safety Confirmation

- [ ] I did not run the executable after verification failed.
- [ ] I removed private keys, passwords, tokens, secrets, and confidential data from this report.
