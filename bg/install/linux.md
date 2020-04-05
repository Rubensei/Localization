---
title: Linux
description: Getting started with a PreMiD installation on Linux
published: true
date: 2020-03-15T17:29:16.527Z
tags:
---

> Before going any further, make sure your system meets all the [requirements](/install/requirements).{.is-info}

The installation of the application is very important as the extension can not do anything by itself.

# Инсталирай

<table>
  <tr>
    <th>Supported Linux Distribution</th>
    <th>Method</th>
    <th>Installing</th>
    <th>Additional Notes</th>
  </tr>
  <tr>
    <td>всичко
</td>
    <td>Portable <a href="https://github.com/PreMiD/Linux/releases/latest">AppImage</a></td>
    <td>
        <code>wget https://github.com/PreMiD/Linux/releases/latest/download/PreMiD-Portable.AppImage && chmod +x PreMiD*.AppImage</code><br>run <code>./PreMiD*.AppImage</code> afterwards or just double-click it
    </td>
    <td><b>This is the recommended package</b> to use, either if you want to try PreMiD or just don't want to install it ( or maybe put it in a USB stick ), it's always up to date but <i>doesn't auto-launch at the system startup</i>, so if you get tired of having to open it each time, use the other methods bellow ( according to your Linux distribution )</td>
  </tr>
  <tr>
    <td rowspan="5">Arch Linux</td>
    <td rowspan="5"><a href="https://aur.archlinux.org/packages/premid">Arch User Repository</a></td>
    <td>Using yay :<br><code>yay -S premid</code><br></td>
    <td rowspan="4">If your distro uses pacman, then you have to install one of the helpers first. If you don't have any, Yay is recommended, run :<br><code>git clone https://aur.archlinux.org/yay.git && cd yay && makepkg -si</code><br>then <code>yay -S premid</code>, as instructed in the previous column.<br><br>Other AUR/Pacman helpers work as well, although each one's functionality is different so you may face issues while using them.</td>
  </tr>
  <tr>
    <td>Using pakku :<br><code>pakku -S premid</code></td>
  </tr>
  <tr>
    <td>Using pacaur :<br><code>pacaur -S premid</code></td>
  </tr>
  <tr>
    <td>Using trizen :<br><code>trizen -S premid</code></td>
  </tr>
  <tr>
    <td><a href="https://wiki.archlinux.org/index.php/Arch_User_Repository#Installing_packages">Manually</a></td>
    <td>Not recommended, not beginner-friendly and doesn't auto update.</td>
  </tr>
  <tr>
    <td>Others</td>
    <td>-</td>
    <td>-</td>
    <td>Soon (TM), use the AppImage for now</td>
  </tr>
</table>

> Do not forget to [add the **extension**](/install).{.is-warning}

# More info
https://github.com/PreMiD/Linux

![](https://a.icons8.com/TqgWTTfw/Oy7xHF/svg.svg) {.align-abstopright}