# Notes

- https://en.wikipedia.org/wiki/Light-weight_Linux_distribution
- Distros:
  - https://alpinelinux.org/
  - https://voidlinux.org/
  - https://puppylinux-woof-ce.github.io/
  - https://mxlinux.org/:
    - "MX Linux - Xfce is our flagship. It is a midweight desktop environment that aims to be fast and low-resource (...)"
  - https://sparkylinux.org/:
    - https://wiki.sparkylinux.org/doku.php/sparky_gui
  - https://www.q4os.org/:
    - https://www.q4os.org/forum/viewtopic.php?id=2560: "The VIA driver is a bit pain in Linux. You could boot Q4OS in recovery mode and try to fix the driver options. Start your computer and tap "Esc" key a few times, the Grub boot table appears. Go to Advanced options .. > recover mode and boot the system."
- https://winaero.com/check-if-processor-is-32-bit-64-bit-or-arm-in-windows-10/
- https://itsfoss.com/32-bit-linux-distributions/
- Zorin OS:
  - https://help.zorin.com/docs/getting-started/system-requirements/: `64-bit`
  - https://help.zorin.com/docs/getting-started/install-zorin-os/
- Software to create bootable USB drives:
  - https://etcher.balena.io/
- https://wiki.alpinelinux.org/wiki/Comparison_with_other_distros
- https://glua.ua.pt/pub/
- https://distrowatch.com/:
  - https://distrowatch.com/search.php?ostype=Linux&category=Old+Computers
- https://www.reddit.com/r/MXLinux/comments/11atmt3/comment/j9vem3u/?utm_source=share&utm_medium=web3x&utm_name=web3xcss&utm_term=1&utm_content=share_button
- [Top 5 Linux Distros For Older Hardware](https://www.youtube.com/watch?v=qUpdHF69BQY) video

## ASUS Eee PC 1005PE

### Alpine Linux

- Default user: `root`

```bash
setup-alpine
```

- Keyboard layout: `pt`
  - Variant: `pt`
- Disk: `sda`
  - Usage: `sys`

```bash
reboot
```

```bash
su
```

```bash
setup-desktop
```

```bash
xfce
```

or

```bash
gnome
```

```bash
reboot
```

```bash
poweroff
```

#### References

- https://superuser.com/a/1267008
- https://techoverflow.net/2021/01/09/what-is-the-alpine-linux-default-login-password/
- https://docs.alpinelinux.org/user-handbook/0.1a/Installing/setup_alpine.html
- https://breder.org/alpine-setup
- https://wiki.alpinelinux.org/wiki/Xfce
- https://docs.alpinelinux.org/user-handbook/0.1a/Working/post-install.html
- https://www.linux.org/threads/black-screen-with-blinking-cursor-not-booting-after-installation.46301/: `Ctrl+Alt+F1`
- https://gitlab.alpinelinux.org/alpine/aports/-/issues/14579
- https://linuxiac.com/how-to-install-alpine-linux/

### MX Linux

- Passwords: `demo` (user demo) and `root` (superuser root)
- _Select type of installation_: _Regular install using the entire disk_

## Commands

```powershell
echo %PROCESSOR_ARCHITECTURE%
```

## Snippets

```markdown
# learning-uxui

## UX Design Foundations (Uxcel)

- Microcopy ≠ Microcontent.
  - Microcopy: error messages, tooltips, button labels, links, navigation menus, etc.
  - Microcontent: page titles (HTML), page headings (headlines), summaries, tips, etc.
- Positive space: the space taken by design elements. Negative space.
- Micro space is the small space between lines, paragraphs, or grid images. Macro space is the large area around a design layout and between its major elements.
- Roles:
  - UX Designer. UX designers are focused on **function**.
  - UI Designer. UI designers are focused on **form**.
  - Visual/Graphic Designer.
  - Product Designer.
  - Information Architect.
  - Motion Designer.
  - Interaction Designer.
  - UX Researcher.
  - UX Engineer. Similar to UX Designer and able to code too.
  - Illustrator.
```
