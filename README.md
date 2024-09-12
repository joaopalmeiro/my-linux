# my-linux

Notes and experiments on Linux distros.

## ASUS Eee PC 1005PE

- 32-bit architecture
- BIOS:
  - Press `F2`
  - To boot from USB, disable the following options:
    - _Boot_ > _Boot Settings Configuration_ > _Quiet Boot_ [Disabled]
    - _Boot_ > _Boot Booster_ [Disabled]

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

```bash
reboot
```

### References

- https://superuser.com/a/1267008
- https://techoverflow.net/2021/01/09/what-is-the-alpine-linux-default-login-password/
- https://docs.alpinelinux.org/user-handbook/0.1a/Installing/setup_alpine.html
- https://breder.org/alpine-setup
- https://wiki.alpinelinux.org/wiki/Xfce
- https://docs.alpinelinux.org/user-handbook/0.1a/Working/post-install.html
- https://www.linux.org/threads/black-screen-with-blinking-cursor-not-booting-after-installation.46301/: `Ctrl+Alt+F1`
- https://gitlab.alpinelinux.org/alpine/aports/-/issues/14579

## Format USB via diskpart (Windows)

- Open Terminal

```powershell
diskpart
```

```powershell
list disk
```

```powershell
select disk <NUMBER>
```

> For example:
>
> ```powershell
> select disk 1
> ```

```powershell
list disk
```

```powershell
clean
```

```powershell
list disk
```

```powershell
create partition primary
```

```powershell
list partition
```

```powershell
select partition 1
```

```powershell
active
```

```powershell
format fs=fat32 quick
```

```powershell
exit
```

### References

- https://superuser.com/a/1741354
- https://www.windowscentral.com/how-clean-and-format-storage-drive-using-diskpart-windows-10
