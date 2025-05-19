🚀 Nala: Your Friendly Package Manager Front-End! ✨
Nala is a sleek, user-friendly front-end for libapt-pkg, built on the python-apt API. 🎉 Designed to make package management a breeze, Nala simplifies the often confusing output of apt, with clear formatting, colorful displays, and smarter workflows. Whether you're a newbie or a seasoned Linux user, Nala’s got your back! 🛠️
📋 Table of Contents

Overview
Installation
Usage
Parallel Downloads
Fetch
History
Zsh/Fish Completions
Bug Reports or Feature Requests
Donations
Screenshots

📖 Overview
Nala is here to make package management fun and intuitive! 😎 By interfacing with python-apt, Nala:

Hides redundant apt messages 🧹
Formats package info clearly 📊
Uses color-coded outputs to show what’s happening during installs, removals, or upgrades 🌈

Why Nala? It’s perfect for new users who find apt overwhelming and pros who want a faster, prettier workflow. 💻
🛠️ Installation
Get Nala up and running in no time! 🚀 Check out our Installation Wiki for detailed steps tailored to your system. 📚
Quick Start:

Follow the wiki instructions to install Nala. 📦
Run nala update to sync your package lists. 🔄
Start managing packages like a pro! 🎮

🎮 Usage
Nala is packed with commands to simplify and supercharge your package management! 🚀 Below are the key ways to use Nala, with examples to get you started. All commands are designed to be intuitive, with clear, color-coded output to show exactly what’s happening. 🌈

Update Package Lists 📋Refresh your system’s package lists to get the latest available packages:  
nala update

Pro Tip: Run this before installing or upgrading to ensure you’re working with the latest data. 🔄

Install Packages 📦Install one or more packages with a clean, colorful summary:  
nala install package-name

Example:  
nala install vim

Nala will show which packages are being installed, upgraded, or removed, with color highlights (e.g., green for installs, red for removals). 🌟

Remove Packages 🗑️Uninstall packages and see a clear breakdown of what’s being removed:  
nala remove package-name

Example:  
nala remove vim

Use --purge to also remove configuration files:  
nala remove --purge vim


Upgrade Packages ⬆️Upgrade all installed packages to their latest versions:  
nala upgrade

This command combines nala update and package upgrades, showing a color-coded list of what’s being updated. 🛠️

Search for Packages 🔍Find packages in the repositories:  
nala search package-name

Example:  
nala search python

Nala displays results in a clean, readable format. 📜

Show Package Details ℹ️Get detailed information about a package, including versions, dependencies, and more:  
nala show package-name

Example:  
nala show apt

Perfect for checking before installing! 👀

Clean Up 🧹Remove cached package files to free up space:  
nala clean

Or remove all cached files, including those still needed:  
nala clean --all


Autoremove Unused Packages 🗑️Clean up unused dependencies left behind after package removals:  
nala autoremove


View Transaction History 🕰️Check your package management history:  
nala history

Undo or redo specific transactions:  
nala history undo <ID>
nala history redo <ID>

Example:  
nala history undo 5


Optimize Mirrors 🌍Use nala fetch to find and configure the fastest mirrors (see Fetch for details):  
nala fetch



Quick Tips:

Run nala --help to see all available commands and options. 📖
Nala’s output is color-coded: green for installs, red for removals, yellow for upgrades, and more! 🌈
Combine commands for efficiency, e.g., nala update && nala upgrade to refresh and upgrade in one go. ⚡

⚡ Parallel Downloads
Say goodbye to slow downloads! 🏎️ Nala’s parallel downloads feature is a game-changer:

Downloads 3 packages at a time per unique mirror in your sources.list. 📥
Alternates between mirrors to maximize speed. 🌐
Skips failed mirrors and tries the next one automatically. 🔄

Note: Nala handles downloading and verification independently of apt, ensuring a smoother experience. 🚀
🌍 Fetch
Meet nala fetch, your ticket to lightning-fast mirrors! ⚡

Automatically detects if you’re on Debian, Ubuntu, or derivatives like Pop!_OS. 🖥️
Fetches the full mirror list from your distro’s master repo. 📋
Tests latency and scores mirrors to pick the fastest 3 (configurable). 🏆
Writes the best mirrors to your sources.list. 📝

Pro Tip: Run nala fetch to optimize your download speeds in seconds! ⏱️
📜 History
Track your package adventures with nala history! 🕰️

Logs every install, remove, or upgrade in /var/lib/nala/history.json with a unique <ID>. 📂
View a summary of all transactions with nala history. 📋
Undo or redo actions with nala history undo <ID> or nala history redo <ID>. 🔄
Clear specific entries with nala history clear <ID> or wipe everything with nala history clear --all. 🧹

Inspired by dnf, Nala’s history feature keeps you in control! 🎮
🐚 Zsh/Fish Completions
Nala makes your shell experience silky smooth! 🐟

Bash, Zsh, and Fish completions are powered by typer. 🛠️
Just install Nala, restart your shell, and enjoy auto-completions with zero setup. ✨

🐛 Bug Reports or Feature Requests
Found a bug or have a brilliant idea? 💡 We’d love to hear from you!

Official Repo: https://gitlab.com/volian/nala 🏠
File bug reports or feature requests on GitLab. 📩
Note: Our GitHub and Debian Salsa repos are official mirrors, but GitLab is the primary hub. 🔗

💖 Donations
Love Nala? Support the project and keep the good vibes going! 🎁
Donate at: https://liberapay.com/Volian-Linux 💸
📸 Screenshots
See Nala in action! 🖼️

Install in Progress
Fetching Mirrors
History Commands
More Features


⭐ Star this repo on GitLab to show your support! Let’s make package management awesome together! 🚀





~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: https://img.shields.io/discord/923757419253882920?color=5865F2&label=Discord&logo=discord&logoColor=FFFFFF&style=flat-square
	:target: https://discord.gg/JEFpg73yr7
	:alt: Discord
.. image:: https://app.codacy.com/project/badge/Grade/686108742fe042c6b31965b5cf51a042
	:target: https://www.codacy.com/gl/volian/nala/dashboard?utm_source=gitlab.com&amp;utm_medium=referral&amp;utm_content=volian/nala&amp;utm_campaign=Badge_Grade
	:alt: Codacy

.. contents:: Table of Contents
	:depth: 1
	:local:
	:backlinks: none

# Nala
======

Nala is a front-end for ``libapt-pkg``. Specifically we interface using the ``python-apt`` api.

Especially for newer users it can be hard to understand what ``apt`` is trying to do when installing or upgrading.

We aim to solve this by not showing some redundant messages, formatting the packages better, and using color to
show specifically what will happen with a package during an install, removal, or upgrade.

# Installation
==============

For installation instructions see our `wiki page <https://gitlab.com/volian/nala/-/wikis/Installation>`_.

# Parallel Downloads
====================

Outside of pretty formatting, the number 1 reason to use Nala over ``apt`` is parallel downloads.

Nala will download 3 packages at a time per unique mirror in your ``sources.list`` file.
This constraint is to limit how hard Nala hits mirrors.
Opening multiple connections to the same mirror is great for speeding up downloading many small packages.

Additionally, we alternate downloads between the available mirrors to improve download speeds even further.
If a mirror fails for whatever reason, we just try the next until all defined mirrors are exhausted.

`Note: Nala does not use APT for package downloading and verification`

# Fetch
=======

Which brings us to our next standout feature, ``nala fetch``.

This command works similar to how most people use ``netselect`` and ``netselect-apt``.
``nala fetch`` will check if your distro is either Debian or Ubuntu.
Nala will then go get all the mirrors from the respective master list.
Once done we test the latency and score each mirror.
Nala will choose the fastest 3 mirrors (configurable) and write them to a file.

`At the moment fetch will only work on Debian, Ubuntu, and derivatives still tied to the main repos. Such as Pop!_OS`

# History
=========

Our last big feature is the ``nala history`` command.

If you're familiar with ``dnf`` this works much in the same way.
Each Install, Remove, or Upgrade we store in /var/lib/nala/history.json with a unique ``<ID>`` number.

At any time you can call ``nala history`` to print a summary of every transaction ever made.
You can then further manipulate this with commands such as ``nala history undo <ID>`` or ``nala history redo <ID>``.

If there is something in the history file that you don't want you can use the ``nala history clear <ID>`` It will remove that entry.

Alternatively, for the ``clear`` command, we accept ``--all`` which will remove the entire history.

# Zsh/fish Completions
======================

Nala's bash, Zsh, and fish completions are now handled with ``typer``.

There is nothing you need to do but install Nala and restart your shell for them to work.

# Bug Reports or Feature Requests
=================================

Nala is mirrored on several sites such as GitHub and even Debian Salsa.

The official repository is https://gitlab.com/volian/nala

We ask that you please go here to report a bug or request a feature.

The other repositories are official, but just mirrors of what is on GitLab.

# Donations
===========

If you would like to support the project you can donate at the link below.

https://liberapay.com/Volian-Linux

# Images
========

.. image:: /imgs/nala-install-1.png
.. image:: /imgs/nala-install-2.png

.. image:: /imgs/nala-fetch.png

.. image:: /imgs/nala-history-info.png
.. image:: /imgs/nala-history-undo-1.png
.. image:: /imgs/nala-history-undo-2.png

.. image:: /imgs/nala-update.png
.. image:: /imgs/nala-show-apt.png
