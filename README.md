# KeyMaster — Releases

Installers, checksums, release notes and update manifests for **KeyMaster**,
a Windows-first interactive keyboard and arranger mastery platform.

**There is no application source code in this repository.** The source is
private. This repository exists so that an installed copy of KeyMaster can
fetch an update manifest and an installer over HTTPS **without carrying a
GitHub credential**, which is the only reason it is public.

---

## Everything here is an owner-QA beta

Every file published so far is a **pre-release build for owner testing**. None
of it is a public production release, and none of it is supported software.

Two consequences worth stating plainly:

- **Windows will warn you about the publisher.** These builds are not signed
  with a purchased Windows code-signing certificate yet. That warning is
  expected. Verify the SHA-256 checksum before running anything.
- **Behaviour may change between builds**, including behaviour you have got
  used to.

## Installing

Download from the [latest release](../../releases), then read `INSTALL.txt`
in that release. In short: run the `-setup.exe`, check the checksum first, and
confirm the version in the bottom-right corner of the application afterwards.

## Verifying a download

```powershell
Get-FileHash .\KeyMaster-<version>-windows-x64-setup.exe -Algorithm SHA256
```

Compare the result against `SHA256SUMS.txt` in the same release. If they do
not match, do not run the file.

## Your data stays on your machine

KeyMaster keeps every profile, every completion and every score in a local
SQLite database on the computer it is installed on. Nothing is uploaded, and
there is no account. Installing on a second computer gives that computer its
own empty database.

## Automatic updates

Not yet. Build 032 adds them, signed and verified. Until then a new version
means downloading a new installer from this page.
