# IAP - ILG (releases)

This repository holds **public installers** for **IAP - ILG**, an internal fork of [IAP Desktop](https://github.com/GoogleCloudPlatform/iap-desktop). Source code lives elsewhere; this repo is for **installers**, **release notes**, and **in-app update checks**.

Releases are published from a **local maintainer** workflow (not stored in this repository): copy the x64 MSI into `installer-files/` next to your clone, then run `scripts\Publish-Release.ps1` with GitHub CLI authenticated for this repo.

## Installing

1. Download the MSI for your PC (64-bit Windows is the usual choice):
   - **x64:** [IapDesktopX64.msi](https://github.com/Kyle-Chandler-GFS/IAP-ILG-RELEASES/releases/latest/download/IapDesktopX64.msi) (from the [latest release](https://github.com/Kyle-Chandler-GFS/IAP-ILG-RELEASES/releases/latest))
2. Run the MSI and complete the wizard (per-user install; admin rights are not required for the default layout).
3. If you already have **another** IAP Desktop–family build installed with a **higher** product version, Windows may block this MSI as a “downgrade.” Uninstall the older product first, or install a release whose **version number is greater** than what is already installed.

## Publisher / SmartScreen

When you run an MSI that was **downloaded from the web**, Windows may show **Unknown publisher** or **Windows protected your PC**. That is normal until the package is signed in a way SmartScreen trusts. We may adopt a **code signing** approach in the future to reduce those prompts.

## Updates

The application checks **GitHub Releases** on this repository. When a newer **non-prerelease** exists, you may get an **Update available** prompt; accepting it typically **opens the browser** to download the new MSI (not a silent auto-install).

Release **tags** must be plain versions (e.g. `1.0.1`), **not** `v1.0.1`. Each release publishes the 64-bit installer as **`IapDesktopX64.msi`** so the download link stays stable.

## Support

Contact your **Technical Service Team**.
