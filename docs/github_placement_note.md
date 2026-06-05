# GitHub Placement Note

Automatic placement has been performed under:

```text
c3infogm-rgb/c3-its-poc
docs/verification_rate_gap/
```

A dedicated repository was not created automatically because the available GitHub connector actions exposed file/branch/PR operations, but not new repository creation.

If a dedicated public repository is later desired, create:

```text
c3infogm-rgb/verification-rate-gap
```

Then copy the contents of this skeleton into that repository.

## Suggested manual commands after extracting this ZIP

```powershell
git clone https://github.com/c3infogm-rgb/verification-rate-gap.git
cd verification-rate-gap
Copy-Item -Recurse <extracted_zip_contents>\* .
git add .
git commit -m "Add Verification Rate Gap research note companion kit"
git push origin main
```

## Existing fallback placement

The artifact set has been staged in the existing C3 ITS PoC repository under:

```text
docs/verification_rate_gap/
```

This is acceptable as an internal companion location until a dedicated public repository is created.
