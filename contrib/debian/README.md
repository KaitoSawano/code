
Debian
====================
This directory contains files used to package litemoneyd/litemoney-qt
for Debian-based Linux systems. If you compile litemoneyd/litemoney-qt yourself, there are some useful files here.

## litemoney: URI support ##


litemoney-qt.desktop  (Gnome / Open Desktop)
To install:

	sudo desktop-file-install litemoney-qt.desktop
	sudo update-desktop-database

If you build yourself, you will either need to modify the paths in
the .desktop file or copy or symlink your litemoney-qt binary to `/usr/bin`
and the `../../share/pixmaps/litemoney128.png` to `/usr/share/pixmaps`

litemoney-qt.protocol (KDE)

