# BergaHallen KTM Installer & Manager

**The recommended way to install and manage a self-hosted BergaHallen KTM Server.**

Installer & Manager is designed to make server installation approachable even if you do not normally work with Linux from the command line.

**[Project homepage](https://bergahallenktm.github.io/)** · **[Release downloads](https://github.com/bergahallenktm/bergahallenktm-server-installer/releases)** · **[Server repository](https://github.com/bergahallenktm/bergahallenktm-server)**

> **Development Preview**  
> Preview releases are intended for testing and may change between versions. Read the release notes before installing or upgrading.

---

## Who should use this?

Use Installer & Manager if you:

- are installing BergaHallen KTM Server for the first time,
- want the supported installation path,
- have limited Linux/CLI experience,
- want a web-based interface for normal server management,
- do not want to manually assemble the server deployment.

This is the **recommended server installation method**.

---

## Download

**[Download an Installer Download the latest Installer & Manager release Manager release →](https://github.com/bergahallenktm/bergahallenktm-server-installer/releases)**

For the supported Ubuntu Server/amd64 release, download the `.deb` package listed under **Assets**.

A release should normally provide:

```text
BergaHallen-KTM-Installer-Manager-<VERSION>-ubuntu24.04-amd64.deb
SHA256SUMS.txt
```

Use the exact filename published by the release; the example above is a naming convention, not a hard-coded current filename.

---

## Before you install

Prepare:

- a supported Ubuntu Server installation,
- a physical server or full virtual machine,
- an account with `sudo` access,
- network access required by the installation process,
- a web browser on a device that can reach the server.

LXC/CT and nested-container environments are not part of the supported installation path.

Always check the release notes for the exact supported platform and any version-specific requirements.

---

## Basic installation flow

After downloading the `.deb` package to the server:

```bash
sudo apt install ./<downloaded-package>.deb
```

Then follow the post-install information printed by the package to open **Manager Web** and continue the setup.

The release documentation should always state the Manager Web address/port or explain how to retrieve it after installation.

---

## What Manager is intended to handle

The Manager Web interface is the normal administration surface for supported management tasks, including the installation lifecycle and available service controls.

Depending on the installed version, supported actions may include:

- installing the BergaHallen KTM Server,
- checking server status,
- starting/stopping supported services,
- enabling/disabling supported components,
- updating the installation,
- running diagnostics,
- managing supported local-service features.

The exact available functions are version-dependent. Use the release notes for the version you installed as the authoritative feature list.

---

## Verify the download

The release includes a `SHA256SUMS.txt` file.

On Linux:

```bash
sha256sum -c SHA256SUMS.txt
```

Only install the package when the verification reports `OK`.

---

## After installation

Keep the installation information produced by the installer. It should tell you where BergaHallen KTM stores configuration, persistent data, backups and logs, together with the address used to access Manager Web.

For troubleshooting, the Manager/installer diagnostic tools should be preferred before manually changing files.

---

## Manual server installation

If you intentionally do not want to use Installer & Manager, the standalone server distribution is available separately:

**[BergaHallen KTM Server →](https://github.com/bergahallenktm/bergahallenktm-server)**

That path is intended for advanced/manual deployment.

---

## Troubleshooting

When asking for help, include:

- Installer & Manager version,
- Ubuntu version,
- the exact error message,
- relevant diagnostic output,
- whether the problem occurred during package installation, Manager Web setup or server installation.

Remove passwords, secrets, tokens and private keys before sharing logs.

---

## Related links

- **[BergaHallen KTM homepage](https://bergahallenktm.github.io/)**
- **[Project documentation](https://github.com/bergahallenktm/bergahallenktm)**
- **[Server repository](https://github.com/bergahallenktm/bergahallenktm-server)**

BergaHallen KTM is an independent fan-made project and is not affiliated with or endorsed by Wizards of the Coast.
