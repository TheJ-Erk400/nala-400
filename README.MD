# 🚀 Nala: Your Ultimate Package Management Sidekick! ✨

Nala is a sleek, user-friendly front-end for `libapt-pkg`, built on the `python-apt` API. 🎯  
It transforms the often complex `apt` experience into a clear, colorful, and intuitive workflow, perfect for Linux beginners and seasoned pros alike. 💻

---

<p align="center">
  <a href="https://discord.gg/JEFpg73yr7">
    <img src="https://img.shields.io/discord/923757419253882920?color=5865F2&label=Discord&logo=discord&logoColor=FFFFFF&style=flat-square" alt="Discord">
  </a>
  <a href="https://www.codacy.com/gl/volian/nala/dashboard?utm_source=gitlab.com&utm_medium=referral&utm_content=volian/nala&utm_campaign=Badge_Grade">
    <img src="https://app.codacy.com/project/badge/Grade/686108742fe042c6b31965b5cf51a042" alt="Codacy">
  </a>
  <a href="https://gitlab.com/volian/nala">
    <img src="https://img.shields.io/badge/GitLab-Repository-FC6D26?style=flat-square&logo=gitlab" alt="GitLab">
  </a>
  <a href="https://liberapay.com/Volian-Linux">
    <img src="https://img.shields.io/badge/Liberapay-Donate-F6C915?style=flat-square&logo=liberapay" alt="Donate">
  </a>
</p>

---

## 📋 Table of Contents

- [Overview](#overview)
- [Installation](#installation)
- [Usage](#usage)
- [Parallel Downloads](#parallel-downloads)
- [Fetch](#fetch)
- [History](#history)
- [Shell Completions](#shell-completions)
- [Bug Reports & Feature Requests](#bug-reports--feature-requests)
- [Donations](#donations)
- [Screenshots](#screenshots)

---

## 📖 Overview

Nala redefines package management with simplicity and clarity! 😎  
By leveraging `python-apt`, Nala:

- Filters out redundant `apt` messages 🧹
- Displays package details in a clean, organized format 📊
- Uses vibrant, color-coded outputs for installs, removals, and upgrades 🌈

**Why Nala?**  
It’s perfect for beginners overwhelmed by `apt` and experts craving a faster, more visually appealing workflow. 🚀

---

## 🛠️ Installation

Get Nala up and running in minutes! ⚡  
Check our detailed [Installation Wiki](https://gitlab.com/volian/nala/-/wikis/Installation) for tailored instructions. 📚

**Quick Start**:

1. Install Nala using the wiki instructions. 📦
2. Run `nala update` to sync package lists. 🔄
3. Manage packages like a pro! 🎮

---

## 🎮 Usage

Nala offers intuitive commands with clear, color-coded feedback (green for installs, red for removals, yellow for upgrades). 🌟

### Update Package Lists 📋

Refresh your package index:

```bash
nala update
```

*Pro Tip*: Run this before installing or upgrading for the latest package data. 🔄

---

### Install Packages 📦

Install with a colorful summary:

```bash
nala install <package-name>
```

**Example**:

```bash
nala install vim
```

Nala highlights what’s being installed, upgraded, or removed. 🌈

---

### Remove Packages 🗑️

Uninstall with a clear breakdown:

```bash
nala remove <package-name>
```

**Example**:

```bash
nala remove vim
```

Add `--purge` to remove configuration files:

```bash
nala remove --purge vim
```

---

### Upgrade Packages ⬆️

Update all packages to their latest versions:

```bash
nala upgrade
```

Combines `nala update` with upgrades, showing a color-coded summary. 🛠️

---

### Search for Packages 🔍

Find packages in repositories:

```bash
nala search <package-name>
```

**Example**:

```bash
nala search python
```

Results are clean and readable. 📜

---

### Show Package Details ℹ️

View package details like versions and dependencies:

```bash
nala show <package-name>
```

**Example**:

```bash
nala show apt
```

Ideal for pre-installation checks! 👀

---

### Clean Up 🧹

Free up space by removing cached package files:

```bash
nala clean
```

Remove all cached files, including those still needed:

```bash
nala clean --all
```

---

### Autoremove Unused Packages 🗑️

Clean up unused dependencies:

```bash
nala autoremove
```

---

### View Transaction History 🕰️

Review package management history:

```bash
nala history
```

Undo or redo transactions:

```bash
nala history undo <ID>
nala history redo <ID>
```

**Example**:

```bash
nala history undo 5
```

---

### Optimize Mirrors 🌍

Configure the fastest mirrors (see [Fetch](#fetch)):

```bash
nala fetch
```

---

**Quick Tips**:

- Use `nala --help` for all commands and options. 📖
- Combine commands like `nala update && nala upgrade` for efficiency. ⚡
- Enjoy color-coded outputs for instant clarity! 🌈

---

## ⚡ Parallel Downloads

Nala’s parallel downloads supercharge your experience: 🏎️

- Downloads 3 packages at once per unique mirror in `sources.list`. 📥
- Alternates mirrors for maximum speed. 🌐
- Skips failed mirrors automatically. 🔄

*Note*: Nala handles downloading and verification independently of `apt`. 🚀

---

## 🌍 Fetch

Optimize downloads with `nala fetch`! ⚡

- Detects Debian, Ubuntu, or derivatives like Pop!_OS. 🖥️
- Retrieves the full mirror list from your distro’s master repo. 📋
- Tests latency and selects the fastest 3 mirrors (configurable). 🏆
- Updates `sources.list` with the best mirrors. 📝

**Pro Tip**: Run `nala fetch` to boost download speeds instantly! ⏱️

---

## 📜 History

Track your package management with `nala history`! 🕰️

- Logs every install, remove, or upgrade in `/var/lib/nala/history.json` with a unique `<ID>`. 📂
- View transaction summaries with `nala history`. 📋
- Undo or redo actions:

  ```bash
  nala history undo <ID>
  nala history redo <ID>
  ```

- Clear entries or wipe history:

  ```bash
  nala history clear <ID>
  nala history clear --all
  ```

Inspired by `dnf`, Nala’s history keeps you in control! 🎮

---

## 🐚 Shell Completions

Nala enhances your shell with seamless completions! 🐟

- Supports Bash, Zsh, and Fish via `typer`. 🛠️
- Install Nala, restart your shell, and enjoy auto-completions. ✨

---

## 🐛 Bug Reports & Feature Requests

Got a bug or idea? 💡 We’re listening!

- **Official Repo**: [https://gitlab.com/volian/nala](https://gitlab.com/volian/nala) 🏠
- File reports or requests on GitLab. 📩
- *Note*: GitHub and Debian Salsa are mirrors; GitLab is the primary hub. 🔗

---

## 💖 Donations

Love Nala? Keep the project thriving! 🎁  
Donate at: [https://liberapay.com/Volian-Linux](https://liberapay.com/Volian-Linux) 💸

---

## 📸 Screenshots

See Nala in action! 🖼️

- Package installation in progress
- Fetching mirrors
- History commands
- And more!

Visit the [official repo](https://gitlab.com/volian/nala) for visuals. 🌟

---

⭐ **Star us on GitLab** to support Nala and make package management awesome! 🚀
````

---

⭐ **Star us on GitLab** to support Nala and make package management awesome! 🚀  
