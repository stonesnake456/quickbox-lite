

![QB-lite](https://i.loli.net/2019/09/16/nqx5mwdDVW3lY6a.png)

# Project QuickBox-Lite

[中文版](https://github.com/amefs/quickbox-lite/blob/master/README_zh.md)

---

This project is a modified version of the QuickBox community edition. This project aims to build a lightweight QuickBox software kit. Most of the functions of QuickBox CE are retained, but only the most commonly used stable third party software included. The prebuilt BT client also available here, which can significantly reduce the installation time as well as CPU requirement to compile them. Most of the software is available as modules. The panel no longer needs the support of ruTorrent. You can select what you need, and this is also why the project named "Lite".

For more information, please check our [wiki](https://github.com/amefs/quickbox-lite/wiki).

---

## Main feature

1. Graphical installation guide (Multi-language available)
2. Use Nginx instead of apache
3. Modular installation
4. Latest OS support
5. up to date apps (prebuild deb packages included)

---

## Script status

![Version](https://img.shields.io/badge/version-1.2.0-orange?style=flat-square)![GNU v3.0 License](https://img.shields.io/badge/license-GNU%20v3.0%20License-blue.svg?style=flat-square)

---

## How to install

### before install

Hardware requirement:

- CPU: At least a 64bit Compatible x86_64 CPU
- RAM: large than 1GB (recommend more for better performance)
- Storage: 20GB HDD (for seeding, you need more)

OS Support (amd64 only):

![Ubuntu18.04](https://img.shields.io/badge/Ubuntu%2018.04-passing-brightgreen.svg?style=flat-square)![Ubuntu16.04](https://img.shields.io/badge/Ubuntu%2016.04-passing-brightgreen.svg?style=flat-square)![Debian9](https://img.shields.io/badge/Debian%209-passing-brightgreen.svg?style=flat-square)![Debian10](https://img.shields.io/badge/Debian%2010-passing-brightgreen.svg?style=flat-square)

Server Support:

- Bare-metal server
- Dedicated server
- VPS with KVM/Xen/VMware (OpenVZ is not supported)

**OVH DEFAULT KERNEL NOTICE!**

> grsec is built into OVH's custom kernel and it absolutely wrecks havoc when using these panels where we depend on the ability for one user (www-data) to see the processes of another running user ($username).
> This can be seen clearly by using a task manager such as htop.
> With grsec enabled you can only see the processes owned by your user unless you run htop as root. As such, it is highly recommended to use the stock kernel for your distribution or at the very least installing an OVH kernel that is not compiled with grsec
> If you are using So You Start (SYS) as a host, you should opt to use the distribution kernel. You will see this as a check box option when installing your server. Otherwise, QuickBox will handle this for you on install.

### install the project

**You must be logged in as root to run this installation.**

**Run the following command to grab our latest stable release ...**

```
apt-get -yqq update; apt-get -yqq upgrade; apt-get -yqq install git lsb-release dos2unix; \
git clone https://github.com/amefs/quickbox-lite.git /etc/QuickBox; \
dos2unix /etc/QuickBox/setup.sh; \
bash /etc/QuickBox/setup.sh

```

### Want to run in development mode?

**Run the following command to grab current development repos ...**

```
mkdir /install/ && touch /install/.developer.lock; \
apt-get -yqq update; apt-get -yqq upgrade; apt-get -yqq install git lsb-release dos2unix; \
git clone --branch "development" https://github.com/amefs/quickbox-lite.git /etc/QuickBox; \
dos2unix /etc/QuickBox/setup.sh; \
bash /etc/QuickBox/setup.sh
```

### Already have QuickBox installed and want to switch over to development?

**EASY! Run the following command to grab current development repos ...**

```
mkdir /install/ && touch /install/.developer.lock; \
sudo box update quickbox
```

---

## Installed Features

- pureftp - vsftp (CuteFTP multi-segmented download friendly)
- SSH Server (for SSH terminal and sFTP connections)
- Web Console (Shellinabox)
- QuickBox Dashboard

---

## Available software

### Available when setup

- rTorrent (*0.9.4-0.9.8*)
  - ruTorrent
  - flood
- Transmission (*2.94*)
- qBittorrent (*4.2.1*)
- Deluge (*1.3.15, 2.0.3*)
- mktorrent (with `createtorrent` command as wrapper)
- FFmpeg
- Linux RAR
- File Browser
- BBR

### Available in dashboard

- Autodl-irssi
- BTSync
- FlexGet(both 2.x and 3.x)
- Netdata
- noVNC
- Plex
- Syncthing
- x2Go

### Available in CLI

- Denyhosts
- Fail2ban
- Let's Encrypt
- ZNC

## Have trouble with QuickBox Lite

If you still have questions about the QuickBox Lite or need to report bugs, be sure to read the [Wiki](https://github.com/amefs/quickbox-lite/wiki) first. When you still have trouble with it, please assign an issue [here](https://github.com/amefs/quickbox-lite/issues/new), I will try my best to help you.

