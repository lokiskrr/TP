# TP3 : Process et identité

- [TP3 : Process et identité](#tp3--process-et-identité)
- [I. Utilisateurs](#i-utilisateurs)
  - [1. Liste des users](#1-liste-des-users)
  - [2. Hash des passwords](#2-hash-des-passwords)
  - [3. Sudo](#3-sudo)
    - [A. Intro](#a-intro)
    - [B. Practice](#b-practice)
- [II. Processes](#ii-processes)
  - [1. Jouer avec la commande ps](#1-jouer-avec-la-commande-ps)
  - [2. Parent, enfant, et meurtre](#2-parent-enfant-et-meurtre)
- [III. Services](#iii-services)
  - [1. Intro](#1-intro)
  - [2. Analyser un service existant](#2-analyser-un-service-existant)
    - [A. Configuration du service SSH](#a-configuration-du-service-ssh)
    - [B. Le service en lui-même](#b-le-service-en-lui-même)
  - [4. Créez votre propre service](#4-créez-votre-propre-service)

# I. Utilisateurs
## 1. Liste des users

🌞 **Afficher la ligne du fichier qui concerne votre utilisateur**

```bash
fata@debian:~$ cat /etc/passwd | grep fata
fata:x:1000:1000:fata,,,:/home/fata:/bin/bash
```

🌞 **Afficher la ligne du fichier qui concerne votre utilisateur ET celle de `root` en même temps**

```bash
fata@debian:~$ cat /etc/passwd | grep -E "fata|root"
root:x:0:0:root:/root:/bin/bash
fata:x:1000:1000:fata,,,:/home/fata:/bin/bash
```

🌞 **Afficher la liste des groupes d'utilisateurs de la *machine***

```bash
fata@debian:~$ cat /etc/passwd |cut -d":" -f1
root
daemon
bin
sys
sync
games
man
lp
mail
news
uucp
proxy
www-data
backup
list
irc
_apt
nobody
systemd-network
tss
systemd-timesync
messagebus
avahi-autoipd
usbmux
dnsmasq
avahi
speech-dispatcher
fwupd-refresh
saned
geoclue
polkitd
rtkit
colord
gnome-initial-setup
Debian-gdm
fata
sshd
marmotte
```


🌞 **Afficher la ligne du fichier qui concerne votre utilisateur ET celle de `root` en même temps**

```bash
fata@debian:~$ cut -d":" -f1,6 | grep -E "naly|root" /etc/passwd
root:x:0:0:root:/root:/bin/bash
```

## 2. Hash des passwords

🌞 **Afficher la ligne qui contient le hash du mot de passe de votre utilisateur**

```bash
root@debian:~# sudo cat /etc/shadow | grep fata
fata:$y$j9T$J.mqtWs1wAzSQ2NOTHYlG.$9aBPN.u874lvEUucSXBnqYdVSdXjgniLTwZfebYZmG8:20033:0:99999:7:::
```

## 3. Sudo
### A. Intro

🌞 **Faites en sorte que votre utilisateur puisse taper n'importe quelle commande `sudo`**

```bash

```

### B. Practice

🌞 **Créer un groupe d'utilisateurs**

```bash
root@debian:~# sudo -u root groupadd stronk_admins
```

🌞 **Créer un utilisateur**

```bash
root@debian:~# sudo useradd -m imbob
root@debian:~# sudo usermod -aG imbob,stronk_admins imbob
root@debian:~# sudo passwd imbob
New password:
Retype new password:
passwd: password updated successfully
```

🌞 **Prouver que l'utilisateur `imbob` est créé**

```bash
root@debian:~# cat /etc/passwd |grep imbob
imbob:x:1002:1003::/home/imbob:/bin/sh
```

🌞 **Prouver que l'utilisateur `imbob` a un password défini**

```bash
root@debian:~# sudo cat /etc/shadow |grep imbob
imbob:$y$j9T$nVuhG6xU/MeUxxrVKSPhZ0$kyEOOBy5ZaauT/i1BqXPIlc.mEFteXSBYzI3J3ht6P9:20046:0:99999:7:::
```

🌞 **Prouver que l'utilisateur `imbob` appartient au groupe `stronk_admins`**

```bash
root@debian:~# sudo cat /etc/group | grep "stronk_admins"
stronk_admins:x:1002:imbob
```

🌞 **Créer un deuxième utilisateur**

```bash
root@debian:~# sudo useradd -m imnotbobsorry
root@debian:~# sudo passwd imnotbobsorry
New password:
Retype new password:
passwd: password updated successfully
```

🌞 **Modifier la configuration de `sudo` pour que**

```bash

```

🌞 **Créer le dossier `/home/goodguy`** (avec une commande)

```bash
root@debian:~# sudo mkdir /home/goodguy
```

🌞 **Changer le répertoire personnel de `imbob`**

```bash
fata@debian:~$ sudo usermod -d /home/goodguy imbob
[sudo] password for fata:

fata@debian:~$ cat /etc/passwd | grep imbob
imbob:x:1002:1003::/home/goodguy:/bin/sh
```

🌞 **Créer le dossier `/home/badguy`**

```bash
root@debian:~# sudo mkdir /home/badguy
```
🌞 **Changer le répertoire personnel de `imnotbobsorry`**

```bash
root@debian:~# sudo mkdir /home/badguy
root@debian:~# sudo usermod -d /home/badguy imnotbobsorry
root@debian:~# cat /etc/passwd | grep imnotbobsorry
imnotbobsorry:x:1003:1004::/home/badguy:/bin/sh
```

🌞 **Prouver que les permissions du dossier `/home/gooduy` sont incohérentes**

```bash
root@debian:~# ls -ld /home/goodguy
drwxr-xr-x 2 root root 4096 Nov 19 18:08 /home/goodguy
root@debian:~# grep imbob /etc/passwd
imbob:x:1002:1003::/home/goodguy:/bin/sh
root@debian:~# sudo chown imbob:imbob /home/goodguy
root@debian:~# sudo su - imbob
$
```

🌞 **Modifier les permissions de `/home/goodguy`**

```bash

```

🌞 **Modifier les permissions de `/home/badguy`**

```bash

```

🌞 **Connectez-vous sur l'utilisateur `imbob`**

```bash
fata@debian:~$ su - root
Password:
root@debian:~# sudo su - imbob
$ 
```

🌞 **Connectez-vous sur l'utilisateur `imnotbobsorry`**

```bash

```

# II. Processes

## 1. Jouer avec la commande ps

🌞 **Affichez les processus `bash`**

```bash
fata@debian:~$ ps -ef |grep bash
fata        4171    4142  0 17:17 pts/0    00:00:00 bash
root        5886    5885  0 17:31 pts/0    00:00:00 -bash
fata        7638    7621  0 19:15 pts/1    00:00:00 -bash
fata        7651    7638  0 19:15 pts/1    00:00:00 grep bash
```

🌞 **Affichez tous les processus lancés par votre utilisateur**

```bash
fata@debian:~$ ps -ef |grep ^fata
fata        2957       1  0 17:17 ?        00:00:00 /lib/systemd/systemd --user
fata        2958    2957  0 17:17 ?        00:00:00 (sd-pam)
fata        2974    2957  0 17:17 ?        00:00:00 /usr/bin/pipewire
fata        2983    2957  0 17:17 ?        00:00:00 /usr/bin/wireplumber
fata        2984    2957  0 17:17 ?        00:00:00 /usr/bin/pipewire-pulse
fata        2985    2957  0 17:17 ?        00:00:00 /usr/bin/gnome-keyring-daemon --foreground --components=pkcs11,secrets --control-directory=/run/user/1000/keyring
fata        2996    2957  0 17:17 ?        00:00:00 /usr/bin/dbus-daemon --session --address=systemd: --nofork --nopidfile --systemd-activation --syslog-only
fata        3003    2935  0 17:17 tty3     00:00:00 /usr/libexec/gdm-wayland-session /usr/bin/gnome-session
fata        3006    2957  0 17:17 ?        00:00:00 /usr/libexec/gvfsd
fata        3023    3003  0 17:17 tty3     00:00:00 /usr/libexec/gnome-session-binary
fata        3090    2957  0 17:17 ?        00:00:00 /usr/libexec/gvfsd-fuse /run/user/1000/gvfs -f
fata        3124    2957  0 17:17 ?        00:00:00 /usr/libexec/gcr-ssh-agent /run/user/1000/gcr
fata        3125    2957  0 17:17 ?        00:00:00 /usr/libexec/gnome-session-ctl --monitor
fata        3126    2957  0 17:17 ?        00:00:00 ssh-agent -D -a /run/user/1000/openssh_agent
fata        3132    2957  0 17:17 ?        00:00:00 /usr/libexec/gnome-session-binary --systemd-service --session=gnome
fata        3151    3132  0 17:17 ?        00:00:00 /usr/libexec/at-spi-bus-launcher --launch-immediately
fata        3152    2957  0 17:17 ?        00:00:37 /usr/bin/gnome-shell
fata        3158    3151  0 17:17 ?        00:00:00 /usr/bin/dbus-daemon --config-file=/usr/share/defaults/at-spi2/accessibility.conf --nofork --print-address 11 --address=unix:path=/run/user/1000/at-spi/bus
fata        3238    2957  0 17:17 ?        00:00:00 /usr/libexec/xdg-permission-store
fata        3240    2957  0 17:17 ?        00:00:00 /usr/libexec/gnome-shell-calendar-server
fata        3249    2957  0 17:17 ?        00:00:00 /usr/libexec/evolution-source-registry
fata        3263    2957  0 17:17 ?        00:00:00 /usr/libexec/goa-daemon
fata        3266    2957  0 17:17 ?        00:00:00 /usr/libexec/evolution-calendar-factory
fata        3275    2957  0 17:17 ?        00:00:00 /usr/libexec/evolution-addressbook-factory
fata        3302    2957  0 17:17 ?        00:00:00 /usr/libexec/gvfs-udisks2-volume-monitor
fata        3304    2957  0 17:17 ?        00:00:00 /usr/libexec/goa-identity-service
fata        3313    2957  0 17:17 ?        00:00:00 /usr/libexec/gvfs-goa-volume-monitor
fata        3317    2957  0 17:17 ?        00:00:00 /usr/libexec/gvfs-mtp-volume-monitor
fata        3321    2957  0 17:17 ?        00:00:00 /usr/libexec/gvfs-gphoto2-volume-monitor
fata        3325    2957  0 17:17 ?        00:00:00 /usr/libexec/gvfs-afc-volume-monitor
fata        3331    2957  0 17:17 ?        00:00:00 /usr/bin/gjs /usr/share/gnome-shell/org.gnome.Shell.Notifications
fata        3333    2957  0 17:17 ?        00:00:00 /usr/libexec/at-spi2-registryd --use-gnome-session
fata        3344    2957  0 17:17 ?        00:00:00 sh -c /usr/bin/ibus-daemon --panel disable $([ "$XDG_SESSION_TYPE" = "x11" ] && echo "--xim")
fata        3345    2957  0 17:17 ?        00:00:00 /usr/libexec/gsd-a11y-settings
fata        3347    2957  0 17:17 ?        00:00:00 /usr/libexec/gsd-color
fata        3348    2957  0 17:17 ?        00:00:00 /usr/libexec/gsd-datetime
fata        3349    2957  0 17:17 ?        00:00:00 /usr/libexec/gsd-housekeeping
fata        3350    2957  0 17:17 ?        00:00:00 /usr/libexec/gsd-keyboard
fata        3351    2957  0 17:17 ?        00:00:00 /usr/libexec/gsd-media-keys
fata        3352    2957  0 17:17 ?        00:00:00 /usr/libexec/gsd-power
fata        3355    2957  0 17:17 ?        00:00:00 /usr/libexec/gsd-print-notifications
fata        3359    3132  0 17:17 ?        00:00:00 /usr/libexec/gsd-disk-utility-notify
fata        3360    2957  0 17:17 ?        00:00:00 /usr/libexec/gsd-rfkill
fata        3362    2957  0 17:17 ?        00:00:00 /usr/libexec/gsd-screensaver-proxy
fata        3363    2957  0 17:17 ?        00:00:00 /usr/libexec/gsd-sharing
fata        3365    2957  0 17:17 ?        00:00:00 /usr/libexec/gsd-smartcard
fata        3366    2957  0 17:17 ?        00:00:00 /usr/libexec/gsd-sound
fata        3367    3344  0 17:17 ?        00:00:01 /usr/bin/ibus-daemon --panel disable
fata        3372    2957  0 17:17 ?        00:00:00 /usr/libexec/gsd-usb-protection
fata        3373    2957  0 17:17 ?        00:00:00 /usr/libexec/gsd-wacom
fata        3375    3132  0 17:17 ?        00:00:00 /usr/libexec/evolution-data-server/evolution-alarm-notify
fata        3380    3132  0 17:17 ?        00:00:29 /usr/bin/gnome-software --gapplication-service
fata        3467    2957  0 17:17 ?        00:00:00 /usr/bin/gjs /usr/share/gnome-shell/org.gnome.ScreenSaver
fata        3490    2957  0 17:17 ?        00:00:00 /usr/libexec/gsd-printer
fata        3515    3367  0 17:17 ?        00:00:00 /usr/libexec/ibus-dconf
fata        3518    3367  0 17:17 ?        00:00:01 /usr/libexec/ibus-extension-gtk3
fata        3522    2957  0 17:17 ?        00:00:00 /usr/libexec/ibus-portal
fata        3550    3367  0 17:17 ?        00:00:00 /usr/libexec/ibus-engine-simple
fata        3554    2957  0 17:17 ?        00:00:00 /usr/libexec/xdg-desktop-portal
fata        3562    2957  0 17:17 ?        00:00:00 /usr/libexec/xdg-document-portal
fata        3590    2957  0 17:17 ?        00:00:00 /usr/libexec/xdg-desktop-portal-gnome
fata        3610    2957  0 17:17 ?        00:00:00 /usr/libexec/tracker-miner-fs-3
fata        3618    2957  0 17:17 ?        00:00:00 /usr/libexec/xdg-desktop-portal-gtk
fata        4142    2957  0 17:17 ?        00:00:03 /usr/libexec/gnome-terminal-server
fata        4171    4142  0 17:17 pts/0    00:00:00 bash
fata        4359    2957  0 17:18 ?        00:00:00 /usr/libexec/gvfsd-metadata
fata        4631    2957  0 17:18 ?        00:00:00 /usr/libexec/dconf-service
fata        7621    7608  0 19:15 ?        00:00:00 sshd: fata@pts/1
fata        7638    7621  0 19:15 pts/1    00:00:00 -bash
fata        7684    7638 99 19:15 pts/1    00:00:00 ps -ef
fata        7685    7638  0 19:15 pts/1    00:00:00 grep ^fata
```

🌞 **Affichez le top 5 des processus qui utilisent le plus de RAM**

```bash
fata@debian:~$ ps -ef --sort=-%mem | head -n 6
UID          PID    PPID  C STIME TTY          TIME CMD
fata        3152    2957  0 17:17 ?        00:00:38 /usr/bin/gnome-shell
marmotte    1743    1100  0 17:16 ?        00:00:06 /usr/libexec/gnome-initial-setup --existing-user
marmotte    1487    1249  0 17:16 ?        00:00:32 /usr/bin/gnome-software --gapplication-service
marmotte    1266    1100  0 17:16 ?        00:00:12 /usr/bin/gnome-shell
fata        3380    3132  0 17:17 ?        00:00:29 /usr/bin/gnome-software --gapplication-service
```

🌞 **Affichez le *PID* du processus du service SSH**

```bash
fata@debian:~$ ps -C sshd |head -n 2
    PID TTY          TIME CMD
    655 ?        00:00:00 sshd
```

🌞 **Affichez le nom du processus avec l'identifiant le plus petit**

```bash
fata@debian:~$ ps --sort=pid -eo pid | head -n 2
    PID
      1
```

## 2. Parent, enfant, et meurtre

🌞 **Déterminer le *PID* de votre shell actuel**

```bash
fata@debian:~$ echo $$
7638
```

🌞 **Déterminer le *PPID* de votre shell actuel**

```bash
fata@debian:~$ ps -ef | grep $$ | head -n 1
fata        7638    7621  0 19:15 pts/1    00:00:00 -bash
```

🌞 **Déterminer le nom de ce *processus***

```bash
fata@debian:~$ ps -p $(ps -p $$ -o ppid=) -o comm=
sshd
```

🌞 **Lancer un *processus* `sleep 9999` en tâche de fond**

```bash
fata@debian:~$ sleep 9999 &
[1] 7703
fata@debian:~$ ps -ef | grep sleep | head -n 1
fata        7703    7638  0 19:18 pts/1    00:00:00 sleep 9999
fata@debian:~$ echo $$
7638
```

🌞 **Fermez votre session SSH**

```bash
fata@debian:~$ ps -ef | grep sleep
fata        7703    7638  0 19:18 pts/1    00:00:00 sleep 9999
fata        7709    7638  0 19:18 pts/1    00:00:00 grep sleep
```

# III. Services

## 1. Intro

## 2. Analyser un service existant

🌞 **S'assurer que le service `ssh` est démarré**

```bash
fata@debian:~$ systemctl status
● debian
    State: running
    Units: 292 loaded (incl. loaded aliases)
     Jobs: 0 queued
   Failed: 0 units
    Since: Tue 2024-11-19 17:15:48 CET; 2h 3min ago
  systemd: 252.30-1~deb12u2
   CGroup: /
           ├─init.scope
           │ └─1 /sbin/init
           ├─system.slice
           │ ├─ModemManager.service
           │ │ └─515 /usr/sbin/ModemManager
           │ ├─NetworkManager.service
           │ │ └─487 /usr/sbin/NetworkManager --no-daemon
           │ ├─accounts-daemon.service
           │ │ └─448 /usr/libexec/accounts-daemon
           │ ├─avahi-daemon.service
           │ │ ├─461 "avahi-daemon: running [debian.local]"
           │ │ └─484 "avahi-daemon: chroot helper"
           │ ├─colord.service
           │ │ └─811 /usr/libexec/colord
           │ ├─cron.service
           │ │ └─464 /usr/sbin/cron -f
           │ ├─cups-browsed.service
           │ │ └─654 /usr/sbin/cups-browsed
           │ ├─cups.service
           │ │ ├─644 /usr/sbin/cupsd -l
           │ │ └─652 /usr/lib/cups/notifier/dbus dbus://
           │ ├─dbus.service
           │ │ └─466 /usr/bin/dbus-daemon --system --address=sy>
lines 1-31
```
```bash 
fata@debian:~$ su - root
Password:
root@debian:~# sudo systemctl list-units -t service -a
  UNIT                                  LOAD      ACTIVE   SUB >
  accounts-daemon.service               loaded    active   runn>
  alsa-restore.service                  loaded    inactive dead>
  alsa-state.service                    loaded    inactive dead>
  anacron.service                       loaded    inactive dead>
  apparmor.service                      loaded    active   exit>
  apt-daily-upgrade.service             loaded    inactive dead>
  apt-daily.service                     loaded    inactive dead>
● auditd.service                        not-found inactive dead>
● auto-cpufreq.service                  not-found inactive dead>
  avahi-daemon.service                  loaded    active   runn>
  colord.service                        loaded    active   runn>
● connman.service                       not-found inactive dead>
● console-screen.service                not-found inactive dead>
  console-setup.service                 loaded    active   exit>
  cron.service                          loaded    active   runn>
  cups-browsed.service                  loaded    active   runn>
  cups.service                          loaded    active   runn>
  dbus.service                          loaded    active   runn>
  dpkg-db-backup.service                loaded    inactive dead>
  e2scrub_all.service                   loaded    inactive dead>
  e2scrub_reap.service                  loaded    inactive dead>
  emergency.service                     loaded    inactive dead>
  fstrim.service                        loaded    inactive dead>
  fwupd-refresh.service                 loaded    inactive dead>
  fwupd.service                         loaded    active   runn>
  gdm.service                           loaded    active   runn>
  geoclue.service                       loaded    active   runn>
  getty-static.service                  loaded    inactive dead>
  getty@tty1.service                    loaded    inactive dead>
  ifupdown-pre.service                  loaded    active   exit>
lines 1-31
```

🌞 **Isolez la ligne qui indique le nom du programme lancé**

```bash
root@debian:~# systemctl status ssh
● ssh.service - OpenBSD Secure Shell server
     Loaded: loaded (/lib/systemd/system/ssh.service; enabled; >
     Active: active (running) since Tue 2024-11-19 17:15:50 CET>
       Docs: man:sshd(8)
             man:sshd_config(5)
    Process: 645 ExecStartPre=/usr/sbin/sshd -t (code=exited, s>
   Main PID: 655 (sshd)
      Tasks: 1 (limit: 2284)
     Memory: 5.8M
        CPU: 520ms
     CGroup: /system.slice/ssh.service
             └─655 "sshd: /usr/sbin/sshd -D [listener] 0 of 10->

Nov 19 17:40:15 debian sshd[6470]: pam_env(sshd:session): depre>
Nov 19 18:02:00 debian sshd[6801]: Accepted password for fata f>
Nov 19 18:02:00 debian sshd[6801]: pam_unix(sshd:session): sess>
Nov 19 18:02:00 debian sshd[6801]: pam_env(sshd:session): depre>
Nov 19 18:08:30 debian sshd[7204]: Accepted password for fata f>
Nov 19 18:08:30 debian sshd[7204]: pam_unix(sshd:session): sess>
Nov 19 18:08:30 debian sshd[7204]: pam_env(sshd:session): depre>
Nov 19 19:15:00 debian sshd[7608]: Accepted password for fata f>
Nov 19 19:15:00 debian sshd[7608]: pam_unix(sshd:session): sess>
Nov 19 19:15:00 debian sshd[7608]: pam_env(sshd:session): depre>
lines 1-23/23 (END)
```

🌞 **Déterminer le port sur lequel écoute le service SSH**

```bash
root@debian:~# sudo ss -lnpt | grep 'sshd'
LISTEN 0      128          0.0.0.0:22        0.0.0.0:*    users:(("sshd",pid=655,fd=3))
LISTEN 0      128             [::]:22           [::]:*    users:(("sshd",pid=655,fd=4))
```

🌞 **Consulter les logs du service SSH**

```bash
root@debian:~# journalctl |grep "sshd"
Nov 07 00:40:37 debian useradd[3916]: new user: name=sshd, UID=114, GID=65534, home=/run/sshd, shell=/usr/sbin/nologin, from=none
Nov 07 00:40:39 debian sshd[3989]: Server listening on 0.0.0.0 port 22.
Nov 07 00:40:39 debian sshd[3989]: Server listening on :: port 22.
Nov 07 00:47:04 debian sshd[4080]: Accepted password for fata from 192.168.103.1 port 55192 ssh2
Nov 07 00:47:04 debian sshd[4080]: pam_unix(sshd:session): session opened for user fata(uid=1000) by (uid=0)
Nov 07 00:47:04 debian sshd[4080]: pam_env(sshd:session): deprecated reading of user environment enabled
Nov 07 00:52:22 debian sshd[4160]: Connection closed by 192.168.103.3 port 41112 [preauth]
Nov 07 20:51:49 debian sshd[4094]: Received disconnect from 192.168.103.1 port 55192:11: disconnected by user
Nov 07 20:51:49 debian sshd[4094]: Disconnected from user fata 192.168.103.1 port 55192
Nov 07 20:51:49 debian sshd[4080]: pam_unix(sshd:session): session closed for user fata
Nov 12 18:07:34 debian sshd[17752]: Accepted password for fata from 192.168.103.1 port 58662 ssh2
Nov 12 18:07:34 debian sshd[17752]: pam_unix(sshd:session): session opened for user fata(uid=1000) by (uid=0)
Nov 12 18:07:34 debian sshd[17752]: pam_env(sshd:session): deprecated reading of user environment enabled
Nov 12 18:14:13 debian sshd[17765]: Received disconnect from 192.168.103.1 port 58662:11: disconnected by user
Nov 12 18:14:13 debian sshd[17765]: Disconnected from user fata 192.168.103.1 port 58662
Nov 12 18:14:13 debian sshd[17752]: pam_unix(sshd:session): session closed for user fata
Nov 12 18:15:06 debian sshd[18988]: Accepted password for fata from 192.168.103.1 port 58695 ssh2
Nov 12 18:15:06 debian sshd[18988]: pam_unix(sshd:session): session opened for user fata(uid=1000) by (uid=0)
Nov 12 18:15:06 debian sshd[18988]: pam_env(sshd:session): deprecated reading of user environment enabled
Nov 12 19:15:11 debian sshd[19950]: Accepted password for fata from 192.168.103.1 port 59299 ssh2
Nov 12 19:15:11 debian sshd[19950]: pam_unix(sshd:session): session opened for user fata(uid=1000) by (uid=0)
Nov 12 19:15:11 debian sshd[19950]: pam_env(sshd:session): deprecated reading of user environment enabled
Nov 12 19:18:05 debian sshd[19005]: Received disconnect from 192.168.103.1 port 58695:11: disconnected by user
Nov 12 19:18:05 debian sshd[19005]: Disconnected from user fata 192.168.103.1 port 58695
Nov 12 19:18:05 debian sshd[18988]: pam_unix(sshd:session): session closed for user fata
Nov 12 19:21:16 debian sshd[19966]: Received disconnect from 192.168.103.1 port 59299:11: disconnected by user
Nov 12 19:21:16 debian sshd[19966]: Disconnected from user fata 192.168.103.1 port 59299
Nov 12 19:21:16 debian sshd[19950]: pam_unix(sshd:session): session closed for user fata
Nov 12 19:29:26 debian sshd[20164]: Invalid user user from 192.168.103.1 port 51373
Nov 12 19:29:28 debian sshd[20164]: pam_unix(sshd:auth): check pass; user unknown
Nov 12 19:29:28 debian sshd[20164]: pam_unix(sshd:auth): authentication failure; logname= uid=0 euid=0 tty=ssh ruser= rhost=192.168.103.1
Nov 12 19:29:30 debian sshd[20164]: Failed password for invalid user user from 192.168.103.1 port 51373 ssh2
Nov 12 19:29:36 debian sshd[20164]: pam_unix(sshd:auth): check pass; user unknown
Nov 12 19:29:39 debian sshd[20164]: Failed password for invalid user user from 192.168.103.1 port 51373 ssh2
Nov 12 19:29:50 debian sshd[20164]: pam_unix(sshd:auth): check pass; user unknown
Nov 12 19:29:52 debian sshd[20164]: Failed password for invalid user user from 192.168.103.1 port 51373 ssh2
Nov 12 19:29:53 debian sshd[20164]: Connection reset by invalid user user 192.168.103.1 port 51373 [preauth]
Nov 12 19:29:53 debian sshd[20164]: PAM 2 more authentication failures; logname= uid=0 euid=0 tty=ssh ruser= rhost=192.168.103.1
Nov 12 19:29:59 debian sshd[20166]: Invalid user user from 192.168.103.1 port 51376
Nov 12 19:30:01 debian sshd[20166]: pam_unix(sshd:auth): check pass; user unknown
Nov 12 19:30:01 debian sshd[20166]: pam_unix(sshd:auth): authentication failure; logname= uid=0 euid=0 tty=ssh ruser= rhost=192.168.103.1
Nov 12 19:30:03 debian sshd[20166]: Failed password for invalid user user from 192.168.103.1 port 51376 ssh2
Nov 12 19:30:06 debian sshd[20166]: pam_unix(sshd:auth): check pass; user unknown
Nov 12 19:30:08 debian sshd[20166]: Failed password for invalid user user from 192.168.103.1 port 51376 ssh2
Nov 12 19:30:36 debian sshd[20166]: pam_unix(sshd:auth): check pass; user unknown
Nov 12 19:30:38 debian sshd[20166]: Failed password for invalid user user from 192.168.103.1 port 51376 ssh2
Nov 12 19:30:38 debian sshd[20166]: Connection reset by invalid user user 192.168.103.1 port 51376 [preauth]
Nov 12 19:30:38 debian sshd[20166]: PAM 2 more authentication failures; logname= uid=0 euid=0 tty=ssh ruser= rhost=192.168.103.1
Nov 12 19:32:35 debian sshd[20449]: Invalid user user from 192.168.103.1 port 51390
Nov 12 19:32:37 debian sshd[20449]: pam_unix(sshd:auth): check pass; user unknown
Nov 12 19:32:37 debian sshd[20449]: pam_unix(sshd:auth): authentication failure; logname= uid=0 euid=0 tty=ssh ruser= rhost=192.168.103.1
Nov 12 19:32:38 debian sshd[20449]: Failed password for invalid user user from 192.168.103.1 port 51390 ssh2
Nov 17 21:37:27 debian sshd[21726]: Invalid user username from 192.168.103.1 port 53583
Nov 17 21:37:29 debian sshd[21726]: pam_unix(sshd:auth): check pass; user unknown
Nov 17 21:37:29 debian sshd[21726]: pam_unix(sshd:auth): authentication failure; logname= uid=0 euid=0 tty=ssh ruser= rhost=192.168.103.1
Nov 17 21:37:31 debian sshd[21726]: Failed password for invalid user username from 192.168.103.1 port 53583 ssh2
Nov 17 21:37:40 debian sshd[21726]: Failed password for invalid user username from 192.168.103.1 port 53583 ssh2
Nov 17 21:37:42 debian sshd[21726]: Failed password for invalid user username from 192.168.103.1 port 53583 ssh2
Nov 17 21:37:42 debian sshd[21726]: Connection reset by invalid user username 192.168.103.1 port 53583 [preauth]
Nov 17 21:38:17 debian sshd[21728]: Invalid user username from 192.168.103.1 port 53586
Nov 17 21:38:22 debian sshd[21728]: pam_unix(sshd:auth): check pass; user unknown
Nov 17 21:38:22 debian sshd[21728]: pam_unix(sshd:auth): authentication failure; logname= uid=0 euid=0 tty=ssh ruser= rhost=192.168.103.1
Nov 17 21:38:23 debian sshd[21728]: Failed password for invalid user username from 192.168.103.1 port 53586 ssh2
Nov 19 16:27:34 debian sshd[21728]: Failed password for invalid user username from 192.168.103.1 port 53586 ssh2
Nov 19 16:27:35 debian sshd[21728]: Failed password for invalid user username from 192.168.103.1 port 53586 ssh2
Nov 19 16:27:35 debian sshd[21728]: Connection reset by invalid user username 192.168.103.1 port 53586 [preauth]
Nov 19 16:28:51 debian sudo[21892]:     root : TTY=pts/0 ; PWD=/ ; USER=root ; COMMAND=/usr/bin/nano /etc/ssh/sshd_config
Nov 19 17:15:50 debian sshd[655]: Server listening on 0.0.0.0 port 22.
Nov 19 17:15:50 debian sshd[655]: Server listening on :: port 22.
Nov 19 17:33:16 debian sshd[6239]: Invalid user username from 192.168.103.1 port 54321
Nov 19 17:33:18 debian sshd[6239]: pam_unix(sshd:auth): check pass; user unknown
Nov 19 17:33:18 debian sshd[6239]: pam_unix(sshd:auth): authentication failure; logname= uid=0 euid=0 tty=ssh ruser= rhost=192.168.103.1
Nov 19 17:33:20 debian sshd[6239]: Failed password for invalid user username from 192.168.103.1 port 54321 ssh2
Nov 19 17:33:43 debian sshd[6239]: Failed password for invalid user username from 192.168.103.1 port 54321 ssh2
Nov 19 17:33:44 debian sshd[6239]: Failed password for invalid user username from 192.168.103.1 port 54321 ssh2
Nov 19 17:33:44 debian sshd[6239]: Connection reset by invalid user username 192.168.103.1 port 54321 [preauth]
Nov 19 17:33:56 debian sshd[6243]: Invalid user user from 192.168.103.1 port 54329
Nov 19 17:34:01 debian sshd[6243]: pam_unix(sshd:auth): check pass; user unknown
Nov 19 17:34:01 debian sshd[6243]: pam_unix(sshd:auth): authentication failure; logname= uid=0 euid=0 tty=ssh ruser= rhost=192.168.103.1
Nov 19 17:34:03 debian sshd[6243]: Failed password for invalid user user from 192.168.103.1 port 54329 ssh2
Nov 19 17:34:05 debian sshd[6243]: Failed password for invalid user user from 192.168.103.1 port 54329 ssh2
Nov 19 17:34:05 debian sshd[6243]: Failed password for invalid user user from 192.168.103.1 port 54329 ssh2
Nov 19 17:34:05 debian sshd[6243]: Connection reset by invalid user user 192.168.103.1 port 54329 [preauth]
Nov 19 17:34:13 debian sshd[6245]: Accepted password for fata from 192.168.103.1 port 54330 ssh2
Nov 19 17:34:13 debian sshd[6245]: pam_unix(sshd:session): session opened for user fata(uid=1000) by (uid=0)
Nov 19 17:34:13 debian sshd[6245]: pam_env(sshd:session): deprecated reading of user environment enabled
Nov 19 17:37:47 debian sshd[6331]: Accepted password for fata from 192.168.103.1 port 54373 ssh2
Nov 19 17:37:47 debian sshd[6331]: pam_unix(sshd:session): session opened for user fata(uid=1000) by (uid=0)
Nov 19 17:37:47 debian sshd[6331]: pam_env(sshd:session): deprecated reading of user environment enabled
Nov 19 17:40:11 debian sshd[6268]: Received disconnect from 192.168.103.1 port 54330:11: disconnected by user
Nov 19 17:40:11 debian sshd[6268]: Disconnected from user fata 192.168.103.1 port 54330
Nov 19 17:40:11 debian sshd[6245]: pam_unix(sshd:session): session closed for user fata
Nov 19 17:40:11 debian sshd[6345]: Received disconnect from 192.168.103.1 port 54373:11: disconnected by user
Nov 19 17:40:11 debian sshd[6345]: Disconnected from user fata 192.168.103.1 port 54373
Nov 19 17:40:11 debian sshd[6331]: pam_unix(sshd:session): session closed for user fata
Nov 19 17:40:15 debian sshd[6470]: Accepted password for fata from 192.168.103.1 port 54396 ssh2
Nov 19 17:40:15 debian sshd[6470]: pam_unix(sshd:session): session opened for user fata(uid=1000) by (uid=0)
Nov 19 17:40:15 debian sshd[6470]: pam_env(sshd:session): deprecated reading of user environment enabled
Nov 19 18:01:53 debian sshd[6485]: Received disconnect from 192.168.103.1 port 54396:11: disconnected by user
Nov 19 18:01:53 debian sshd[6485]: Disconnected from user fata 192.168.103.1 port 54396
Nov 19 18:01:53 debian sshd[6470]: pam_unix(sshd:session): session closed for user fata
Nov 19 18:02:00 debian sshd[6801]: Accepted password for fata from 192.168.103.1 port 54617 ssh2
Nov 19 18:02:00 debian sshd[6801]: pam_unix(sshd:session): session opened for user fata(uid=1000) by (uid=0)
Nov 19 18:02:00 debian sshd[6801]: pam_env(sshd:session): deprecated reading of user environment enabled
Nov 19 18:08:27 debian sshd[6816]: Received disconnect from 192.168.103.1 port 54617:11: disconnected by user
Nov 19 18:08:27 debian sshd[6816]: Disconnected from user fata 192.168.103.1 port 54617
Nov 19 18:08:27 debian sshd[6801]: pam_unix(sshd:session): session closed for user fata
Nov 19 18:08:30 debian sshd[7204]: Accepted password for fata from 192.168.103.1 port 54712 ssh2
Nov 19 18:08:30 debian sshd[7204]: pam_unix(sshd:session): session opened for user fata(uid=1000) by (uid=0)
Nov 19 18:08:30 debian sshd[7204]: pam_env(sshd:session): deprecated reading of user environment enabled
Nov 19 19:14:57 debian sshd[7218]: Received disconnect from 192.168.103.1 port 54712:11: disconnected by user
Nov 19 19:14:57 debian sshd[7218]: Disconnected from user fata 192.168.103.1 port 54712
Nov 19 19:14:57 debian sshd[7204]: pam_unix(sshd:session): session closed for user fata
Nov 19 19:15:00 debian sshd[7608]: Accepted password for fata from 192.168.103.1 port 54910 ssh2
Nov 19 19:15:00 debian sshd[7608]: pam_unix(sshd:session): session opened for user fata(uid=1000) by (uid=0)
Nov 19 19:15:00 debian sshd[7608]: pam_env(sshd:session): deprecated reading of user environment enabled
```

### A. Configuration du service SSH

🌞 **Identifier le fichier de configuration du serveur SSH**

```bash
root@debian:~# ls -l /etc/ssh/sshd_config
-rw-r--r-- 1 root root 3223 Jun 22 21:38 /etc/ssh/sshd_config
```

🌞 **Modifier le fichier de conf**

```bash
root@debian:~# echo $RANDOM
11982
```

🌞 **Redémarrer le service**

```bash
root@debian:~# systemctl restart sshd
```

🌞 **Effectuer une connexion SSH sur le nouveau port**

```bash
root@debian:~# sudo ss -lnpt | grep sshd
LISTEN 0      128          0.0.0.0:22        0.0.0.0:*    users:(("sshd",pid=7764,fd=3))
LISTEN 0      128             [::]:22           [::]:*    users:(("sshd",pid=7764,fd=4))
```

### B. Le service en lui-même

🌞 **Trouver le fichier `ssh.service`**

```bash
root@debian:~# systemctl show -p FragmentPath ssh.service
FragmentPath=/lib/systemd/system/ssh.service
```

🌞 **Déterminer quel est le programme lancé**

```bash
root@debian:~# systemctl show ssh.service -p ExecStart
ExecStart={ path=/usr/sbin/sshd ; argv[]=/usr/sbin/sshd -D $SSH>
lines 1-1/1 (END)
```

## 4. Créez votre propre service

🌞 **Déterminer le dossier qui contient la commande `python3`**

```bash
fata@debian:~$ which python3
/usr/bin/python3
```

🌞 **Créez un fichier `/etc/systemd/system/meow_web.service`**

```bash

```

🌞 **Indiquez à l'OS que vous avez modifié les *services***

```bash

```

🌞 **Démarrez votre service**

```bash

```

🌞 **Assurez-vous que le service `meow_web` est actif**

```bash

```

🌞 **Déterminer le PID du *processus* Python en cours d'exécution**

```bash

```

🌞 **Prouvez que le *programme* écoute derrière le port 8888**

```bash

```
🌞 **Faire en sote que le *service* se lance automatiquement au démarrage de la machine**

```bash

```