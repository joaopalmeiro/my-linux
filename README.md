# my-linux

Notes and experiments on Linux distros.

## Lenovo ThinkPad T490

- https://ubuntu.com/download/desktop
  - https://documentation.ubuntu.com/desktop/en/latest/how-to/create-a-bootable-usb-stick/
  - https://formulae.brew.sh/cask/balenaetcher

### Software

```bash
sudo apt update && sudo apt install curl git
```

Install [1Password](https://support.1password.com/install-linux/#debian-or-ubuntu) and set up [SSH](https://developer.1password.com/docs/ssh/get-started/).

```bash
git config --global user.email "<EMAIL>" && git config --global user.name "João Palmeiro"
```

```bash
sudo snap install spotify && sudo snap install steam && sudo snap install okular && sudo snap install code --classic && sudo snap install ghostty --classic
```

```bash
cp vscode_settings.json ~/.config/Code/User/settings.json
```

Install the [VS Code extensions](https://github.com/joaopalmeiro/dotfiles/tree/main#vs-code).

#### Epson Perfection V39 II

Download the [Epson Scan2 driver](https://download-center.epson.com/softwares/?device_id=Perfection+V39II&region=PT&os=DEBX64&language=en).

Unzip the downloaded file, open the folder, right-click on the `install.sh` file, and _Run as a Program_.

Install the [dependencies](https://download-center.epson.com/f/module/6ea06a0a-3010-4360-926f-b81554132eb1/overview/epsonscan2_e_1.1.pdf):

```bash
sudo apt update && sudo apt install qtbase5-dev
```

```bash
epsonscan2
```

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

## Ubuntu VM (ARM) on macOS

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
