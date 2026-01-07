bin-desktop
===========

This repo is a collection of scripts for use with various Linux desktop environments.

Usage
-----

Within the root of this project (`bin-desktop`) is a directory named `bin-desktop`. Create a symlink at `${HOME}/.local/bin/bin-desktop` that points to the *subdirectory* named `bin-desktop`.

Table of contents
-----------------

- [Usage](#usage)
- [Scripts](#scripts)
    - [artix_cinnamon_audiostart](#artix_cinnamon_audiostart)
    - [notif_ram-usage](#notif_ram-usage)

Scripts
-------

### artix_cinnamon_audiostart

Date created: 2025 Nov 12, Wed

`artix_cinnamon_audiostart` was written to address an issue with Artix Cinnamon desktops -- `pipewire` doesn't start automatically with the desktop, and has to be called with a script.

`artix_cinnamon_audiostart` solves this by killing all audio-related processes and restarting them. This can be paired with Cinnamon's built-in "startup" settings, and the script can be configured to run when the desktop starts, enabling audio automatically (just like with machines running `systemd`).

### notif_ram-usage

Date created: 2025 Mar 11, Tue

`notif_ram-usage` was originally written to allow GNOME desktop users a way to receive notifications when RAM usage gets above a specified threshold.

When paired with the included cronjob, `notif_ram-usage` runs in the background every few minutes, and will send a notification if RAM usage gets too high.
