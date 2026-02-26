# Portal Client Prerequisites

This guide will get your environment ready to use the [portal client](https://github.com/IGS/portal_client) for downloading data from the [VMRC Portal](https://portal.vmrc4health.org/).

> [!IMPORTANT]
> In order to follow these instructions, you will need an institutional Google account that has been granted access to the VMRC Google Cloud project. If you have not yet created this type of account, please follow the following [instructions](institutional_google_account_creation.md).

Once you've completed these steps, you'll be ready to follow the [portal client usage instructions](portal_client_usage.md).

---

## Overview

The portal client requires:
- A terminal (command-line interface)
- Python 3.11 or higher (with `pip` and `venv`)
- Google Cloud CLI (`gcloud`)

Follow the section below that matches your operating system.

---

## macOS

### 1. Open a Terminal

Open the **Terminal** app. You can find it via Spotlight Search (`Cmd + Space`, then type "Terminal") or under **Applications → Utilities → Terminal**.

### 2. Check Your Python Version

In your terminal, run:

```bash
python3 --version
```

You should see `Python 3.11.x` or higher. If you see a lower version or a `command not found` error, visit [python.org/downloads](https://www.python.org/downloads/) to install a current version (you may need to restart your terminal once the installation is complete to ensure `python` is on your PATH).

You can verify that `pip` and `venv` are available by running:

```bash
python3 -m pip --version
python3 -m venv --help
```

### 3. Install Google Cloud CLI

Follow the [official macOS installation instructions](https://cloud.google.com/sdk/docs/install#mac) for the Google Cloud CLI (the specific package you should download will depend on both your operating system and your CPU). Once installed, initialize and log in by running:

```bash
gcloud init
```

This will provide a URL to open in your browser to complete authentication.

Once authenticated and back in the terminal, when prompted, provide the following cloud project id:

```bash
vmrc-462716
```

---

## Linux

### 1. Open a Terminal

Open your distribution's terminal emulator (e.g., **GNOME Terminal**, **Konsole**, or **xterm**).

### 2. Check Your Python Version

```bash
python3 --version
```

You should see `Python 3.11.x` or higher. If your version is older, use your distribution's package manager to update. For example, on Ubuntu/Debian:

```bash
sudo apt update && sudo apt install python3 python3-pip python3-venv
```

Verify `pip` and `venv` are available:

```bash
python3 -m pip --version
python3 -m venv --help
```

### 3. Install Google Cloud CLI

Follow the [official Linux installation instructions](https://cloud.google.com/sdk/docs/install#linux) for the Google Cloud CLI (the specific package you should download will depend on both your operating system and your CPU). Once installed, initialize and log in:

```bash
gcloud init
```

This will provide a URL to open in your browser to complete authentication.

Once authenticated and back in the terminal, when prompted, provide the following cloud project id:

```bash
vmrc-462716
```

---

## Windows

Windows requires a few extra steps. Because the portal client is designed to run in a Unix-like environment, you will need to set up **Windows Subsystem for Linux (WSL)** — a feature built into Windows that lets you run a Linux environment directly on your machine without a virtual machine.

### 1. Install WSL

Follow Microsoft's official guide to install WSL:
[https://learn.microsoft.com/en-us/windows/wsl/install](https://learn.microsoft.com/en-us/windows/wsl/install)

We recommend installing the default distribution (**Ubuntu**). Once installed, open your **Ubuntu** terminal from the Start menu — this is the terminal you will use for all steps that follow.

### 2. Set Your WSL sudo Password

Several steps below require `sudo`. If this is a fresh WSL install, your user may not have a password set yet, which will cause `sudo` to fail. To set one, open **PowerShell** and run:

```powershell
wsl -u root
```

This opens a root shell inside WSL. Then set a password for your user (replace `<your-username>` with your WSL username):

```bash
passwd <your-username>
```

You will be prompted to enter and confirm a new password. Once done, type `exit` to return to PowerShell, then reopen your **Ubuntu** terminal to continue.

### 3. Update Package Lists and Python

WSL's Ubuntu may ship with an older version of Python. Run the following to update and install the required components:

```bash
sudo apt update && sudo apt upgrade -y
sudo apt install -y python3 python3-pip python3-venv
```

Verify your Python version is 3.11 or higher:

```bash
python3 --version
```

If the version is still below 3.11, you can install a specific version using the `deadsnakes` PPA:

```bash
sudo add-apt-repository ppa:deadsnakes/ppa
sudo apt update
sudo apt install -y python3.11 python3.11-venv
sudo apt install -y python3-pip
```

Then confirm:

```bash
python3.11 --version
```

> **Note:** If you installed Python 3.11 via `deadsnakes`, use `python3.11` in place of `python3` when following the portal client instructions.

### 4. Install Google Cloud CLI

The standard Linux `apt`-based installation instructions for gcloud may not work cleanly in WSL. Instead, use the following `curl` command from within your WSL terminal:

```bash
curl https://sdk.cloud.google.com | bash
```

Follow the prompts, then restart your WSL terminal to ensure `gcloud` is on your PATH. Once ready, initialize and log in:

```bash
gcloud init
```

This will provide a URL to open in your browser to complete authentication.

Once authenticated and back in the terminal, when prompted, provide the following cloud project id:

```bash
vmrc-462716
```

---

## You're Ready

Once you've completed the steps above, proceed to the [portal client usage instructions](portal_client_usage.md) to begin downloading your data.

If you run into issues with any of these setup steps, please [open an issue](https://github.com/vmrc4health/vmrc-docs/issues) on this repository.
