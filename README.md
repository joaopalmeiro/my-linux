# my-linux

Notes and experiments on Linux distros.

## ASUS Eee PC 1005PE

- 32-bit architecture
- BIOS:
  - Press `F2`
  - To boot from USB, disable the following options:
    - _Boot_ > _Boot Settings Configuration_ > _Quiet Boot_ [Disabled]
    - _Boot_ > _Boot Booster_ [Disabled]
- OS: Q4OS Aquarius (Trinity desktop)

### Software

#### Evince (document/PDF viewer)

```bash
sudo apt-get install evince
```

#### Falkon (browser)

```bash
sudo apt-get install falkon
```

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

## Ubuntu VM on macOS

- https://formulae.brew.sh/cask/virtualbox
- Ubuntu Server for ARM: https://ubuntu.com/download/server/arm
- https://docs.getutm.app/guides/ubuntu/
- https://askubuntu.com/questions/434849/change-keyboard-layout-english-uk-on-command-line-to-english-us

### Change keyboard layout

```bash
sudo dpkg-reconfigure keyboard-configuration
```

```bash
sudo reboot
```

### Install Ubuntu Desktop (GUI)

```bash
sudo apt update
```

```bash
sudo apt install ubuntu-desktop
```

```bash
sudo reboot
```
