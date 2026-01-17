# xfdesktop-live-wallpaper

A fork of xfdesktop with modifications to support live/animated wallpapers on XFCE.

## What's Changed

| Change | Why |
|--------|-----|
| Window type → `NORMAL` | Allows stacking control (live wallpaper renders below) |
| Window title → `xfceliveDesktop` | Easy detection by wallpaper engines via `wmctrl` |
| RGBA visual enabled | Transparency support |
| `keep_below` disabled | Window can be positioned above live wallpaper |

Desktop icons and right-click menus still work normally.

## Usage

1. Build and install this patched xfdesktop
2. Set background to Transparent: `xfconf-query -c xfce4-desktop -p /backdrop/.../color-style -s 3`
3. Set image style to None: `xfconf-query -c xfce4-desktop -p /backdrop/.../image-style -s 0`
4. Run your live wallpaper engine

> **Note:** [live-dither-wp](https://github.com/arfelious/live-dither-wp) handles steps 2-3 itself.

---

[![License](https://img.shields.io/badge/License-GPL%20v2-blue.svg)](https://gitlab.xfce.org/xfce/xfdesktop/-/blob/master/COPYING)

# xfdesktop


Xfdesktop is a desktop manager for the Xfce Desktop Environment. It handles the following tasks:

  * background image / color
  * root menu, window list
  * minimized app icons
  * file icons on the desktop (using Thunar libs)

It can bring up an applications menu and a list of all running applications when you click on the desktop with the right or middle mouse button respectively. Settings are available via the Settings Manager.

----

### Homepage

[Xfdesktop documentation](https://docs.xfce.org/xfce/xfdesktop/start)

### Changelog

See [NEWS](https://gitlab.xfce.org/xfce/xfdesktop/-/blob/master/NEWS) for details on changes and fixes made in the current release.

### Source Code Repository

[Xfdesktop source code](https://gitlab.xfce.org/xfce/xfdesktop)

### Download a Release Tarball

[Xfdesktop archive](https://archive.xfce.org/src/xfce/xfdesktop)
    or
[Xfdesktop tags](https://gitlab.xfce.org/xfce/xfdesktop/-/tags)

### Installation

From source: 

    % cd xfdesktop
    % ./autogen.sh
    % make
    % make install

From release tarball:

    % tar xf xfdesktop-<version>.tar.bz2
    % cd xfdesktop-<version>
    % ./configure
    % make
    % make install

### Reporting Bugs

Visit the [reporting bugs](https://docs.xfce.org/xfce/xfdesktop/bugs) page to view currently open bug reports and instructions on reporting new bugs or submitting bugfixes.

