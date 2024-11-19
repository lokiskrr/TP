# TP2 : Le terminal vous a déjà manqué non

# I. Gameshell
```
done :) 
```

# II. Files and users
- [TP2 : Le terminal vous a déjà manqué non](#tp2--le-terminal-vous-a-déjà-manqué-non)
- [I. Gameshell](#i-gameshell)
- [II. Files and users](#ii-files-and-users)
- [1. Fichiers](#1-fichiers)
  - [A. Find me](#a-find-me)
- [2. Users](#2-users)
  - [A. Nouveau user](#a-nouveau-user)
  - [B. Infos enregistrées par le système](#b-infos-enregistrées-par-le-système)
  - [C. Hint sur la ligne de commande](#c-hint-sur-la-ligne-de-commande)
  - [D. Connexion sur le nouvel utilisateur](#d-connexion-sur-le-nouvel-utilisateur)
- [III. Programmes et paquets](#iii-programmes-et-paquets)
- [1. Programmes et processus](#1-programmes-et-processus)
  - [A. Run then kill](#a-run-then-kill)
  - [B. Tâche de fond](#b-tâche-de-fond)
  - [C. Find paths](#c-find-paths)
  - [D. La variable PATH](#d-la-variable-path)
- [2. Paquets](#2-paquets)
- [IV. Poupée russe](#iv-poupée-russe)

# 1. Fichiers

## A. Find me

🌞 **Trouver le chemin vers le répertoire personnel de votre utilisateur**

```bash
fata@debian:/$ cd /home/
```

🌞 **Vérifier les permissions du répertoire personnel de votre utilisateurs**

```bash
fata@debian:/home$ ls -l
total 4
drwx------ 16 fata fata 4096 Nov 12 18:16 fata
```
🌞 **Trouver le chemin du fichier de configuration du serveur SSH**

```bash
je suis pas trop sur de ça 

fata@debian:/home$ find / -name "sshd_config"
find: ‘/proc/tty/driver’: Permission denied
find: ‘/proc/1/task/1/fd’: Permission denied
find: ‘/proc/1/task/1/fdinfo’: Permission denied
find: ‘/proc/1/task/1/ns’: Permission denied
find: ‘/proc/1/fd’: Permission denied
find: ‘/proc/1/map_files’: Permission denied
find: ‘/proc/1/fdinfo’: Permission denied
find: ‘/proc/1/ns’: Permission denied
find: ‘/proc/2/task/2/fd’: Permission denied
find: ‘/proc/2/task/2/fdinfo’: Permission denied
find: ‘/proc/2/task/2/ns’: Permission denied
find: ‘/proc/2/fd’: Permission denied
find: ‘/proc/2/map_files’: Permission denied
find: ‘/proc/2/fdinfo’: Permission denied
find: ‘/proc/2/ns’: Permission denied
find: ‘/proc/3/task/3/fd’: Permission denied
find: ‘/proc/3/task/3/fdinfo’: Permission denied
find: ‘/proc/3/task/3/ns’: Permission denied
find: ‘/proc/3/fd’: Permission denied
find: ‘/proc/3/map_files’: Permission denied
find: ‘/proc/3/fdinfo’: Permission denied
find: ‘/proc/3/ns’: Permission denied
find: ‘/proc/4/task/4/fd’: Permission denied
find: ‘/proc/4/task/4/fdinfo’: Permission denied
find: ‘/proc/4/task/4/ns’: Permission denied
find: ‘/proc/4/fd’: Permission denied
find: ‘/proc/4/map_files’: Permission denied
find: ‘/proc/4/fdinfo’: Permission denied
find: ‘/proc/4/ns’: Permission denied
find: ‘/proc/5/task/5/fd’: Permission denied
find: ‘/proc/5/task/5/fdinfo’: Permission denied
find: ‘/proc/5/task/5/ns’: Permission denied
find: ‘/proc/5/fd’: Permission denied
find: ‘/proc/5/map_files’: Permission denied
find: ‘/proc/5/fdinfo’: Permission denied
find: ‘/proc/5/ns’: Permission denied
find: ‘/proc/6/task/6/fd’: Permission denied
find: ‘/proc/6/task/6/fdinfo’: Permission denied
find: ‘/proc/6/task/6/ns’: Permission denied
find: ‘/proc/6/fd’: Permission denied
find: ‘/proc/6/map_files’: Permission denied
find: ‘/proc/6/fdinfo’: Permission denied
find: ‘/proc/6/ns’: Permission denied
find: ‘/proc/10/task/10/fd’: Permission denied
find: ‘/proc/10/task/10/fdinfo’: Permission denied
find: ‘/proc/10/task/10/ns’: Permission denied
find: ‘/proc/10/fd’: Permission denied
find: ‘/proc/10/map_files’: Permission denied
find: ‘/proc/10/fdinfo’: Permission denied
find: ‘/proc/10/ns’: Permission denied
find: ‘/proc/11/task/11/fd’: Permission denied
find: ‘/proc/11/task/11/fdinfo’: Permission denied
find: ‘/proc/11/task/11/ns’: Permission denied
find: ‘/proc/11/fd’: Permission denied
find: ‘/proc/11/map_files’: Permission denied
find: ‘/proc/11/fdinfo’: Permission denied
find: ‘/proc/11/ns’: Permission denied
find: ‘/proc/12/task/12/fd’: Permission denied
find: ‘/proc/12/task/12/fdinfo’: Permission denied
find: ‘/proc/12/task/12/ns’: Permission denied
find: ‘/proc/12/fd’: Permission denied
find: ‘/proc/12/map_files’: Permission denied
find: ‘/proc/12/fdinfo’: Permission denied
find: ‘/proc/12/ns’: Permission denied
find: ‘/proc/13/task/13/fd’: Permission denied
find: ‘/proc/13/task/13/fdinfo’: Permission denied
find: ‘/proc/13/task/13/ns’: Permission denied
find: ‘/proc/13/fd’: Permission denied
find: ‘/proc/13/map_files’: Permission denied
find: ‘/proc/13/fdinfo’: Permission denied
find: ‘/proc/13/ns’: Permission denied
find: ‘/proc/14/task/14/fd’: Permission denied
find: ‘/proc/14/task/14/fdinfo’: Permission denied
find: ‘/proc/14/task/14/ns’: Permission denied
find: ‘/proc/14/fd’: Permission denied
find: ‘/proc/14/map_files’: Permission denied
find: ‘/proc/14/fdinfo’: Permission denied
find: ‘/proc/14/ns’: Permission denied
find: ‘/proc/15/task/15/fd’: Permission denied
find: ‘/proc/15/task/15/fdinfo’: Permission denied
find: ‘/proc/15/task/15/ns’: Permission denied
find: ‘/proc/15/fd’: Permission denied
find: ‘/proc/15/map_files’: Permission denied
find: ‘/proc/15/fdinfo’: Permission denied
find: ‘/proc/15/ns’: Permission denied
find: ‘/proc/16/task/16/fd’: Permission denied
find: ‘/proc/16/task/16/fdinfo’: Permission denied
find: ‘/proc/16/task/16/ns’: Permission denied
find: ‘/proc/16/fd’: Permission denied
find: ‘/proc/16/map_files’: Permission denied
find: ‘/proc/16/fdinfo’: Permission denied
find: ‘/proc/16/ns’: Permission denied
find: ‘/proc/18/task/18/fd’: Permission denied
find: ‘/proc/18/task/18/fdinfo’: Permission denied
find: ‘/proc/18/task/18/ns’: Permission denied
find: ‘/proc/18/fd’: Permission denied
find: ‘/proc/18/map_files’: Permission denied
find: ‘/proc/18/fdinfo’: Permission denied
find: ‘/proc/18/ns’: Permission denied
find: ‘/proc/20/task/20/fd’: Permission denied
find: ‘/proc/20/task/20/fdinfo’: Permission denied
find: ‘/proc/20/task/20/ns’: Permission denied
find: ‘/proc/20/fd’: Permission denied
find: ‘/proc/20/map_files’: Permission denied
find: ‘/proc/20/fdinfo’: Permission denied
find: ‘/proc/20/ns’: Permission denied
find: ‘/proc/21/task/21/fd’: Permission denied
find: ‘/proc/21/task/21/fdinfo’: Permission denied
find: ‘/proc/21/task/21/ns’: Permission denied
find: ‘/proc/21/fd’: Permission denied
find: ‘/proc/21/map_files’: Permission denied
find: ‘/proc/21/fdinfo’: Permission denied
find: ‘/proc/21/ns’: Permission denied
find: ‘/proc/22/task/22/fd’: Permission denied
find: ‘/proc/22/task/22/fdinfo’: Permission denied
find: ‘/proc/22/task/22/ns’: Permission denied
find: ‘/proc/22/fd’: Permission denied
find: ‘/proc/22/map_files’: Permission denied
find: ‘/proc/22/fdinfo’: Permission denied
find: ‘/proc/22/ns’: Permission denied
find: ‘/proc/23/task/23/fd’: Permission denied
find: ‘/proc/23/task/23/fdinfo’: Permission denied
find: ‘/proc/23/task/23/ns’: Permission denied
find: ‘/proc/23/fd’: Permission denied
find: ‘/proc/23/map_files’: Permission denied
find: ‘/proc/23/fdinfo’: Permission denied
find: ‘/proc/23/ns’: Permission denied
find: ‘/proc/24/task/24/fd’: Permission denied
find: ‘/proc/24/task/24/fdinfo’: Permission denied
find: ‘/proc/24/task/24/ns’: Permission denied
find: ‘/proc/24/fd’: Permission denied
find: ‘/proc/24/map_files’: Permission denied
find: ‘/proc/24/fdinfo’: Permission denied
find: ‘/proc/24/ns’: Permission denied
find: ‘/proc/27/task/27/fd’: Permission denied
find: ‘/proc/27/task/27/fdinfo’: Permission denied
find: ‘/proc/27/task/27/ns’: Permission denied
find: ‘/proc/27/fd’: Permission denied
find: ‘/proc/27/map_files’: Permission denied
find: ‘/proc/27/fdinfo’: Permission denied
find: ‘/proc/27/ns’: Permission denied
find: ‘/proc/28/task/28/fd’: Permission denied
find: ‘/proc/28/task/28/fdinfo’: Permission denied
find: ‘/proc/28/task/28/ns’: Permission denied
find: ‘/proc/28/fd’: Permission denied
find: ‘/proc/28/map_files’: Permission denied
find: ‘/proc/28/fdinfo’: Permission denied
find: ‘/proc/28/ns’: Permission denied
find: ‘/proc/29/task/29/fd’: Permission denied
find: ‘/proc/29/task/29/fdinfo’: Permission denied
find: ‘/proc/29/task/29/ns’: Permission denied
find: ‘/proc/29/fd’: Permission denied
find: ‘/proc/29/map_files’: Permission denied
find: ‘/proc/29/fdinfo’: Permission denied
find: ‘/proc/29/ns’: Permission denied
find: ‘/proc/30/task/30/fd’: Permission denied
find: ‘/proc/30/task/30/fdinfo’: Permission denied
find: ‘/proc/30/task/30/ns’: Permission denied
find: ‘/proc/30/fd’: Permission denied
find: ‘/proc/30/map_files’: Permission denied
find: ‘/proc/30/fdinfo’: Permission denied
find: ‘/proc/30/ns’: Permission denied
find: ‘/proc/31/task/31/fd’: Permission denied
find: ‘/proc/31/task/31/fdinfo’: Permission denied
find: ‘/proc/31/task/31/ns’: Permission denied
find: ‘/proc/31/fd’: Permission denied
find: ‘/proc/31/map_files’: Permission denied
find: ‘/proc/31/fdinfo’: Permission denied
find: ‘/proc/31/ns’: Permission denied
find: ‘/proc/32/task/32/fd’: Permission denied
find: ‘/proc/32/task/32/fdinfo’: Permission denied
find: ‘/proc/32/task/32/ns’: Permission denied
find: ‘/proc/32/fd’: Permission denied
find: ‘/proc/32/map_files’: Permission denied
find: ‘/proc/32/fdinfo’: Permission denied
find: ‘/proc/32/ns’: Permission denied
find: ‘/proc/33/task/33/fd’: Permission denied
find: ‘/proc/33/task/33/fdinfo’: Permission denied
find: ‘/proc/33/task/33/ns’: Permission denied
find: ‘/proc/33/fd’: Permission denied
find: ‘/proc/33/map_files’: Permission denied
find: ‘/proc/33/fdinfo’: Permission denied
find: ‘/proc/33/ns’: Permission denied
find: ‘/proc/34/task/34/fd’: Permission denied
find: ‘/proc/34/task/34/fdinfo’: Permission denied
find: ‘/proc/34/task/34/ns’: Permission denied
find: ‘/proc/34/fd’: Permission denied
find: ‘/proc/34/map_files’: Permission denied
find: ‘/proc/34/fdinfo’: Permission denied
find: ‘/proc/34/ns’: Permission denied
find: ‘/proc/35/task/35/fd’: Permission denied
find: ‘/proc/35/task/35/fdinfo’: Permission denied
find: ‘/proc/35/task/35/ns’: Permission denied
find: ‘/proc/35/fd’: Permission denied
find: ‘/proc/35/map_files’: Permission denied
find: ‘/proc/35/fdinfo’: Permission denied
find: ‘/proc/35/ns’: Permission denied
find: ‘/proc/36/task/36/fd’: Permission denied
find: ‘/proc/36/task/36/fdinfo’: Permission denied
find: ‘/proc/36/task/36/ns’: Permission denied
find: ‘/proc/36/fd’: Permission denied
find: ‘/proc/36/map_files’: Permission denied
find: ‘/proc/36/fdinfo’: Permission denied
find: ‘/proc/36/ns’: Permission denied
find: ‘/proc/37/task/37/fd’: Permission denied
find: ‘/proc/37/task/37/fdinfo’: Permission denied
find: ‘/proc/37/task/37/ns’: Permission denied
find: ‘/proc/37/fd’: Permission denied
find: ‘/proc/37/map_files’: Permission denied
find: ‘/proc/37/fdinfo’: Permission denied
find: ‘/proc/37/ns’: Permission denied
find: ‘/proc/38/task/38/fd’: Permission denied
find: ‘/proc/38/task/38/fdinfo’: Permission denied
find: ‘/proc/38/task/38/ns’: Permission denied
find: ‘/proc/38/fd’: Permission denied
find: ‘/proc/38/map_files’: Permission denied
find: ‘/proc/38/fdinfo’: Permission denied
find: ‘/proc/38/ns’: Permission denied
find: ‘/proc/44/task/44/fd’: Permission denied
find: ‘/proc/44/task/44/fdinfo’: Permission denied
find: ‘/proc/44/task/44/ns’: Permission denied
find: ‘/proc/44/fd’: Permission denied
find: ‘/proc/44/map_files’: Permission denied
find: ‘/proc/44/fdinfo’: Permission denied
find: ‘/proc/44/ns’: Permission denied
find: ‘/proc/46/task/46/fd’: Permission denied
find: ‘/proc/46/task/46/fdinfo’: Permission denied
find: ‘/proc/46/task/46/ns’: Permission denied
find: ‘/proc/46/fd’: Permission denied
find: ‘/proc/46/map_files’: Permission denied
find: ‘/proc/46/fdinfo’: Permission denied
find: ‘/proc/46/ns’: Permission denied
find: ‘/proc/48/task/48/fd’: Permission denied
find: ‘/proc/48/task/48/fdinfo’: Permission denied
find: ‘/proc/48/task/48/ns’: Permission denied
find: ‘/proc/48/fd’: Permission denied
find: ‘/proc/48/map_files’: Permission denied
find: ‘/proc/48/fdinfo’: Permission denied
find: ‘/proc/48/ns’: Permission denied
find: ‘/proc/49/task/49/fd’: Permission denied
find: ‘/proc/49/task/49/fdinfo’: Permission denied
find: ‘/proc/49/task/49/ns’: Permission denied
find: ‘/proc/49/fd’: Permission denied
find: ‘/proc/49/map_files’: Permission denied
find: ‘/proc/49/fdinfo’: Permission denied
find: ‘/proc/49/ns’: Permission denied
find: ‘/proc/54/task/54/fd’: Permission denied
find: ‘/proc/54/task/54/fdinfo’: Permission denied
find: ‘/proc/54/task/54/ns’: Permission denied
find: ‘/proc/54/fd’: Permission denied
find: ‘/proc/54/map_files’: Permission denied
find: ‘/proc/54/fdinfo’: Permission denied
find: ‘/proc/54/ns’: Permission denied
find: ‘/proc/59/task/59/fd’: Permission denied
find: ‘/proc/59/task/59/fdinfo’: Permission denied
find: ‘/proc/59/task/59/ns’: Permission denied
find: ‘/proc/59/fd’: Permission denied
find: ‘/proc/59/map_files’: Permission denied
find: ‘/proc/59/fdinfo’: Permission denied
find: ‘/proc/59/ns’: Permission denied
find: ‘/proc/60/task/60/fd’: Permission denied
find: ‘/proc/60/task/60/fdinfo’: Permission denied
find: ‘/proc/60/task/60/ns’: Permission denied
find: ‘/proc/60/fd’: Permission denied
find: ‘/proc/60/map_files’: Permission denied
find: ‘/proc/60/fdinfo’: Permission denied
find: ‘/proc/60/ns’: Permission denied
find: ‘/proc/125/task/125/fd’: Permission denied
find: ‘/proc/125/task/125/fdinfo’: Permission denied
find: ‘/proc/125/task/125/ns’: Permission denied
find: ‘/proc/125/fd’: Permission denied
find: ‘/proc/125/map_files’: Permission denied
find: ‘/proc/125/fdinfo’: Permission denied
find: ‘/proc/125/ns’: Permission denied
find: ‘/proc/126/task/126/fd’: Permission denied
find: ‘/proc/126/task/126/fdinfo’: Permission denied
find: ‘/proc/126/task/126/ns’: Permission denied
find: ‘/proc/126/fd’: Permission denied
find: ‘/proc/126/map_files’: Permission denied
find: ‘/proc/126/fdinfo’: Permission denied
find: ‘/proc/126/ns’: Permission denied
find: ‘/proc/127/task/127/fd’: Permission denied
find: ‘/proc/127/task/127/fdinfo’: Permission denied
find: ‘/proc/127/task/127/ns’: Permission denied
find: ‘/proc/127/fd’: Permission denied
find: ‘/proc/127/map_files’: Permission denied
find: ‘/proc/127/fdinfo’: Permission denied
find: ‘/proc/127/ns’: Permission denied
find: ‘/proc/128/task/128/fd’: Permission denied
find: ‘/proc/128/task/128/fdinfo’: Permission denied
find: ‘/proc/128/task/128/ns’: Permission denied
find: ‘/proc/128/fd’: Permission denied
find: ‘/proc/128/map_files’: Permission denied
find: ‘/proc/128/fdinfo’: Permission denied
find: ‘/proc/128/ns’: Permission denied
find: ‘/proc/129/task/129/fd’: Permission denied
find: ‘/proc/129/task/129/fdinfo’: Permission denied
find: ‘/proc/129/task/129/ns’: Permission denied
find: ‘/proc/129/fd’: Permission denied
find: ‘/proc/129/map_files’: Permission denied
find: ‘/proc/129/fdinfo’: Permission denied
find: ‘/proc/129/ns’: Permission denied
find: ‘/proc/130/task/130/fd’: Permission denied
find: ‘/proc/130/task/130/fdinfo’: Permission denied
find: ‘/proc/130/task/130/ns’: Permission denied
find: ‘/proc/130/fd’: Permission denied
find: ‘/proc/130/map_files’: Permission denied
find: ‘/proc/130/fdinfo’: Permission denied
find: ‘/proc/130/ns’: Permission denied
find: ‘/proc/131/task/131/fd’: Permission denied
find: ‘/proc/131/task/131/fdinfo’: Permission denied
find: ‘/proc/131/task/131/ns’: Permission denied
find: ‘/proc/131/fd’: Permission denied
find: ‘/proc/131/map_files’: Permission denied
find: ‘/proc/131/fdinfo’: Permission denied
find: ‘/proc/131/ns’: Permission denied
find: ‘/proc/138/task/138/fd’: Permission denied
find: ‘/proc/138/task/138/fdinfo’: Permission denied
find: ‘/proc/138/task/138/ns’: Permission denied
find: ‘/proc/138/fd’: Permission denied
find: ‘/proc/138/map_files’: Permission denied
find: ‘/proc/138/fdinfo’: Permission denied
find: ‘/proc/138/ns’: Permission denied
find: ‘/proc/141/task/141/fd’: Permission denied
find: ‘/proc/141/task/141/fdinfo’: Permission denied
find: ‘/proc/141/task/141/ns’: Permission denied
find: ‘/proc/141/fd’: Permission denied
find: ‘/proc/141/map_files’: Permission denied
find: ‘/proc/141/fdinfo’: Permission denied
find: ‘/proc/141/ns’: Permission denied
find: ‘/proc/179/task/179/fd’: Permission denied
find: ‘/proc/179/task/179/fdinfo’: Permission denied
find: ‘/proc/179/task/179/ns’: Permission denied
find: ‘/proc/179/fd’: Permission denied
find: ‘/proc/179/map_files’: Permission denied
find: ‘/proc/179/fdinfo’: Permission denied
find: ‘/proc/179/ns’: Permission denied
find: ‘/proc/180/task/180/fd’: Permission denied
find: ‘/proc/180/task/180/fdinfo’: Permission denied
find: ‘/proc/180/task/180/ns’: Permission denied
find: ‘/proc/180/fd’: Permission denied
find: ‘/proc/180/map_files’: Permission denied
find: ‘/proc/180/fdinfo’: Permission denied
find: ‘/proc/180/ns’: Permission denied
find: ‘/proc/224/task/224/fd’: Permission denied
find: ‘/proc/224/task/224/fdinfo’: Permission denied
find: ‘/proc/224/task/224/ns’: Permission denied
find: ‘/proc/224/fd’: Permission denied
find: ‘/proc/224/map_files’: Permission denied
find: ‘/proc/224/fdinfo’: Permission denied
find: ‘/proc/224/ns’: Permission denied
find: ‘/proc/259/task/259/fd’: Permission denied
find: ‘/proc/259/task/259/fdinfo’: Permission denied
find: ‘/proc/259/task/259/ns’: Permission denied
find: ‘/proc/259/fd’: Permission denied
find: ‘/proc/259/map_files’: Permission denied
find: ‘/proc/259/fdinfo’: Permission denied
find: ‘/proc/259/ns’: Permission denied
find: ‘/proc/265/task/265/fd’: Permission denied
find: ‘/proc/265/task/265/fdinfo’: Permission denied
find: ‘/proc/265/task/265/ns’: Permission denied
find: ‘/proc/265/task/400/fd’: Permission denied
find: ‘/proc/265/task/400/fdinfo’: Permission denied
find: ‘/proc/265/task/400/ns’: Permission denied
find: ‘/proc/265/fd’: Permission denied
find: ‘/proc/265/map_files’: Permission denied
find: ‘/proc/265/fdinfo’: Permission denied
find: ‘/proc/265/ns’: Permission denied
find: ‘/proc/353/task/353/fd’: Permission denied
find: ‘/proc/353/task/353/fdinfo’: Permission denied
find: ‘/proc/353/task/353/ns’: Permission denied
find: ‘/proc/353/fd’: Permission denied
find: ‘/proc/353/map_files’: Permission denied
find: ‘/proc/353/fdinfo’: Permission denied
find: ‘/proc/353/ns’: Permission denied
find: ‘/proc/468/task/468/fd’: Permission denied
find: ‘/proc/468/task/468/fdinfo’: Permission denied
find: ‘/proc/468/task/468/ns’: Permission denied
find: ‘/proc/468/task/492/fd’: Permission denied
find: ‘/proc/468/task/492/fdinfo’: Permission denied
find: ‘/proc/468/task/492/ns’: Permission denied
find: ‘/proc/468/task/502/fd’: Permission denied
find: ‘/proc/468/task/502/fdinfo’: Permission denied
find: ‘/proc/468/task/502/ns’: Permission denied
find: ‘/proc/468/fd’: Permission denied
find: ‘/proc/468/map_files’: Permission denied
find: ‘/proc/468/fdinfo’: Permission denied
find: ‘/proc/468/ns’: Permission denied
find: ‘/proc/472/task/472/fd’: Permission denied
find: ‘/proc/472/task/472/fdinfo’: Permission denied
find: ‘/proc/472/task/472/ns’: Permission denied
find: ‘/proc/472/fd’: Permission denied
find: ‘/proc/472/map_files’: Permission denied
find: ‘/proc/472/fdinfo’: Permission denied
find: ‘/proc/472/ns’: Permission denied
find: ‘/proc/474/task/474/fd’: Permission denied
find: ‘/proc/474/task/474/fdinfo’: Permission denied
find: ‘/proc/474/task/474/ns’: Permission denied
find: ‘/proc/474/fd’: Permission denied
find: ‘/proc/474/map_files’: Permission denied
find: ‘/proc/474/fdinfo’: Permission denied
find: ‘/proc/474/ns’: Permission denied
find: ‘/proc/476/task/476/fd’: Permission denied
find: ‘/proc/476/task/476/fdinfo’: Permission denied
find: ‘/proc/476/task/476/ns’: Permission denied
find: ‘/proc/476/fd’: Permission denied
find: ‘/proc/476/map_files’: Permission denied
find: ‘/proc/476/fdinfo’: Permission denied
find: ‘/proc/476/ns’: Permission denied
find: ‘/proc/480/task/480/fd’: Permission denied
find: ‘/proc/480/task/480/fdinfo’: Permission denied
find: ‘/proc/480/task/480/ns’: Permission denied
find: ‘/proc/480/task/487/fd’: Permission denied
find: ‘/proc/480/task/487/fdinfo’: Permission denied
find: ‘/proc/480/task/487/ns’: Permission denied
find: ‘/proc/480/task/501/fd’: Permission denied
find: ‘/proc/480/task/501/fdinfo’: Permission denied
find: ‘/proc/480/task/501/ns’: Permission denied
find: ‘/proc/480/fd’: Permission denied
find: ‘/proc/480/map_files’: Permission denied
find: ‘/proc/480/fdinfo’: Permission denied
find: ‘/proc/480/ns’: Permission denied
find: ‘/proc/483/task/483/fd’: Permission denied
find: ‘/proc/483/task/483/fdinfo’: Permission denied
find: ‘/proc/483/task/483/ns’: Permission denied
find: ‘/proc/483/task/497/fd’: Permission denied
find: ‘/proc/483/task/497/fdinfo’: Permission denied
find: ‘/proc/483/task/497/ns’: Permission denied
find: ‘/proc/483/task/503/fd’: Permission denied
find: ‘/proc/483/task/503/fdinfo’: Permission denied
find: ‘/proc/483/task/503/ns’: Permission denied
find: ‘/proc/483/fd’: Permission denied
find: ‘/proc/483/map_files’: Permission denied
find: ‘/proc/483/fdinfo’: Permission denied
find: ‘/proc/483/ns’: Permission denied
find: ‘/proc/484/task/484/fd’: Permission denied
find: ‘/proc/484/task/484/fdinfo’: Permission denied
find: ‘/proc/484/task/484/ns’: Permission denied
find: ‘/proc/484/task/510/fd’: Permission denied
find: ‘/proc/484/task/510/fdinfo’: Permission denied
find: ‘/proc/484/task/510/ns’: Permission denied
find: ‘/proc/484/task/520/fd’: Permission denied
find: ‘/proc/484/task/520/fdinfo’: Permission denied
find: ‘/proc/484/task/520/ns’: Permission denied
find: ‘/proc/484/fd’: Permission denied
find: ‘/proc/484/map_files’: Permission denied
find: ‘/proc/484/fdinfo’: Permission denied
find: ‘/proc/484/ns’: Permission denied
find: ‘/proc/485/task/485/fd’: Permission denied
find: ‘/proc/485/task/485/fdinfo’: Permission denied
find: ‘/proc/485/task/485/ns’: Permission denied
find: ‘/proc/485/task/522/fd’: Permission denied
find: ‘/proc/485/task/522/fdinfo’: Permission denied
find: ‘/proc/485/task/522/ns’: Permission denied
find: ‘/proc/485/task/527/fd’: Permission denied
find: ‘/proc/485/task/527/fdinfo’: Permission denied
find: ‘/proc/485/task/527/ns’: Permission denied
find: ‘/proc/485/fd’: Permission denied
find: ‘/proc/485/map_files’: Permission denied
find: ‘/proc/485/fdinfo’: Permission denied
find: ‘/proc/485/ns’: Permission denied
find: ‘/proc/486/task/486/fd’: Permission denied
find: ‘/proc/486/task/486/fdinfo’: Permission denied
find: ‘/proc/486/task/486/ns’: Permission denied
find: ‘/proc/486/fd’: Permission denied
find: ‘/proc/486/map_files’: Permission denied
find: ‘/proc/486/fdinfo’: Permission denied
find: ‘/proc/486/ns’: Permission denied
find: ‘/proc/491/task/491/fd’: Permission denied
find: ‘/proc/491/task/491/fdinfo’: Permission denied
find: ‘/proc/491/task/491/ns’: Permission denied
find: ‘/proc/491/task/509/fd’: Permission denied
find: ‘/proc/491/task/509/fdinfo’: Permission denied
find: ‘/proc/491/task/509/ns’: Permission denied
find: ‘/proc/491/task/515/fd’: Permission denied
find: ‘/proc/491/task/515/fdinfo’: Permission denied
find: ‘/proc/491/task/515/ns’: Permission denied
find: ‘/proc/491/task/540/fd’: Permission denied
find: ‘/proc/491/task/540/fdinfo’: Permission denied
find: ‘/proc/491/task/540/ns’: Permission denied
find: ‘/proc/491/task/575/fd’: Permission denied
find: ‘/proc/491/task/575/fdinfo’: Permission denied
find: ‘/proc/491/task/575/ns’: Permission denied
find: ‘/proc/491/fd’: Permission denied
find: ‘/proc/491/map_files’: Permission denied
find: ‘/proc/491/fdinfo’: Permission denied
find: ‘/proc/491/ns’: Permission denied
find: ‘/proc/494/task/494/fd’: Permission denied
find: ‘/proc/494/task/494/fdinfo’: Permission denied
find: ‘/proc/494/task/494/ns’: Permission denied
find: ‘/proc/494/fd’: Permission denied
find: ‘/proc/494/map_files’: Permission denied
find: ‘/proc/494/fdinfo’: Permission denied
find: ‘/proc/494/ns’: Permission denied
find: ‘/proc/500/task/500/fd’: Permission denied
find: ‘/proc/500/task/500/fdinfo’: Permission denied
find: ‘/proc/500/task/500/ns’: Permission denied
find: ‘/proc/500/task/547/fd’: Permission denied
find: ‘/proc/500/task/547/fdinfo’: Permission denied
find: ‘/proc/500/task/547/ns’: Permission denied
find: ‘/proc/500/task/548/fd’: Permission denied
find: ‘/proc/500/task/548/fdinfo’: Permission denied
find: ‘/proc/500/task/548/ns’: Permission denied
find: ‘/proc/500/fd’: Permission denied
find: ‘/proc/500/map_files’: Permission denied
find: ‘/proc/500/fdinfo’: Permission denied
find: ‘/proc/500/ns’: Permission denied
find: ‘/proc/504/task/504/fd’: Permission denied
find: ‘/proc/504/task/504/fdinfo’: Permission denied
find: ‘/proc/504/task/504/ns’: Permission denied
find: ‘/proc/504/fd’: Permission denied
find: ‘/proc/504/map_files’: Permission denied
find: ‘/proc/504/fdinfo’: Permission denied
find: ‘/proc/504/ns’: Permission denied
find: ‘/proc/505/task/505/fd’: Permission denied
find: ‘/proc/505/task/505/fdinfo’: Permission denied
find: ‘/proc/505/task/505/ns’: Permission denied
find: ‘/proc/505/fd’: Permission denied
find: ‘/proc/505/map_files’: Permission denied
find: ‘/proc/505/fdinfo’: Permission denied
find: ‘/proc/505/ns’: Permission denied
find: ‘/proc/536/task/536/fd’: Permission denied
find: ‘/proc/536/task/536/fdinfo’: Permission denied
find: ‘/proc/536/task/536/ns’: Permission denied
find: ‘/proc/536/task/553/fd’: Permission denied
find: ‘/proc/536/task/553/fdinfo’: Permission denied
find: ‘/proc/536/task/553/ns’: Permission denied
find: ‘/proc/536/task/560/fd’: Permission denied
find: ‘/proc/536/task/560/fdinfo’: Permission denied
find: ‘/proc/536/task/560/ns’: Permission denied
find: ‘/proc/536/fd’: Permission denied
find: ‘/proc/536/map_files’: Permission denied
find: ‘/proc/536/fdinfo’: Permission denied
find: ‘/proc/536/ns’: Permission denied
find: ‘/proc/561/task/561/fd’: Permission denied
find: ‘/proc/561/task/561/fdinfo’: Permission denied
find: ‘/proc/561/task/561/ns’: Permission denied
find: ‘/proc/561/fd’: Permission denied
find: ‘/proc/561/map_files’: Permission denied
find: ‘/proc/561/fdinfo’: Permission denied
find: ‘/proc/561/ns’: Permission denied
find: ‘/proc/579/task/579/fd’: Permission denied
find: ‘/proc/579/task/579/fdinfo’: Permission denied
find: ‘/proc/579/task/579/ns’: Permission denied
find: ‘/proc/579/task/580/fd’: Permission denied
find: ‘/proc/579/task/580/fdinfo’: Permission denied
find: ‘/proc/579/task/580/ns’: Permission denied
find: ‘/proc/579/task/581/fd’: Permission denied
find: ‘/proc/579/task/581/fdinfo’: Permission denied
find: ‘/proc/579/task/581/ns’: Permission denied
find: ‘/proc/579/fd’: Permission denied
find: ‘/proc/579/map_files’: Permission denied
find: ‘/proc/579/fdinfo’: Permission denied
find: ‘/proc/579/ns’: Permission denied
find: ‘/proc/613/task/613/fd’: Permission denied
find: ‘/proc/613/task/613/fdinfo’: Permission denied
find: ‘/proc/613/task/613/ns’: Permission denied
find: ‘/proc/613/task/629/fd’: Permission denied
find: ‘/proc/613/task/629/fdinfo’: Permission denied
find: ‘/proc/613/task/629/ns’: Permission denied
find: ‘/proc/613/task/630/fd’: Permission denied
find: ‘/proc/613/task/630/fdinfo’: Permission denied
find: ‘/proc/613/task/630/ns’: Permission denied
find: ‘/proc/613/fd’: Permission denied
find: ‘/proc/613/map_files’: Permission denied
find: ‘/proc/613/fdinfo’: Permission denied
find: ‘/proc/613/ns’: Permission denied
find: ‘/proc/655/task/655/fd’: Permission denied
find: ‘/proc/655/task/655/fdinfo’: Permission denied
find: ‘/proc/655/task/655/ns’: Permission denied
find: ‘/proc/655/task/659/fd’: Permission denied
find: ‘/proc/655/task/659/fdinfo’: Permission denied
find: ‘/proc/655/task/659/ns’: Permission denied
find: ‘/proc/655/task/660/fd’: Permission denied
find: ‘/proc/655/task/660/fdinfo’: Permission denied
find: ‘/proc/655/task/660/ns’: Permission denied
find: ‘/proc/655/fd’: Permission denied
find: ‘/proc/655/map_files’: Permission denied
find: ‘/proc/655/fdinfo’: Permission denied
find: ‘/proc/655/ns’: Permission denied
find: ‘/proc/739/task/739/fd’: Permission denied
find: ‘/proc/739/task/739/fdinfo’: Permission denied
find: ‘/proc/739/task/739/ns’: Permission denied
find: ‘/proc/739/task/741/fd’: Permission denied
find: ‘/proc/739/task/741/fdinfo’: Permission denied
find: ‘/proc/739/task/741/ns’: Permission denied
find: ‘/proc/739/task/742/fd’: Permission denied
find: ‘/proc/739/task/742/fdinfo’: Permission denied
find: ‘/proc/739/task/742/ns’: Permission denied
find: ‘/proc/739/fd’: Permission denied
find: ‘/proc/739/map_files’: Permission denied
find: ‘/proc/739/fdinfo’: Permission denied
find: ‘/proc/739/ns’: Permission denied
find: ‘/proc/760/task/760/fd’: Permission denied
find: ‘/proc/760/task/760/fdinfo’: Permission denied
find: ‘/proc/760/task/760/ns’: Permission denied
find: ‘/proc/760/task/763/fd’: Permission denied
find: ‘/proc/760/task/763/fdinfo’: Permission denied
find: ‘/proc/760/task/763/ns’: Permission denied
find: ‘/proc/760/task/765/fd’: Permission denied
find: ‘/proc/760/task/765/fdinfo’: Permission denied
find: ‘/proc/760/task/765/ns’: Permission denied
find: ‘/proc/760/fd’: Permission denied
find: ‘/proc/760/map_files’: Permission denied
find: ‘/proc/760/fdinfo’: Permission denied
find: ‘/proc/760/ns’: Permission denied
find: ‘/proc/1071/task/1071/fd’: Permission denied
find: ‘/proc/1071/task/1071/fdinfo’: Permission denied
find: ‘/proc/1071/task/1071/ns’: Permission denied
find: ‘/proc/1071/task/1072/fd’: Permission denied
find: ‘/proc/1071/task/1072/fdinfo’: Permission denied
find: ‘/proc/1071/task/1072/ns’: Permission denied
find: ‘/proc/1071/task/1073/fd’: Permission denied
find: ‘/proc/1071/task/1073/fdinfo’: Permission denied
find: ‘/proc/1071/task/1073/ns’: Permission denied
find: ‘/proc/1071/fd’: Permission denied
find: ‘/proc/1071/map_files’: Permission denied
find: ‘/proc/1071/fdinfo’: Permission denied
find: ‘/proc/1071/ns’: Permission denied
find: ‘/proc/1098/task/1098/fd’: Permission denied
find: ‘/proc/1098/task/1098/fdinfo’: Permission denied
find: ‘/proc/1098/task/1098/ns’: Permission denied
find: ‘/proc/1098/fd’: Permission denied
find: ‘/proc/1098/map_files’: Permission denied
find: ‘/proc/1098/fdinfo’: Permission denied
find: ‘/proc/1098/ns’: Permission denied
find: ‘/proc/1225/task/1225/fd’: Permission denied
find: ‘/proc/1225/task/1225/fdinfo’: Permission denied
find: ‘/proc/1225/task/1225/ns’: Permission denied
find: ‘/proc/1225/fd’: Permission denied
find: ‘/proc/1225/map_files’: Permission denied
find: ‘/proc/1225/fdinfo’: Permission denied
find: ‘/proc/1225/ns’: Permission denied
find: ‘/proc/1700/task/1700/fd’: Permission denied
find: ‘/proc/1700/task/1700/fdinfo’: Permission denied
find: ‘/proc/1700/task/1700/ns’: Permission denied
find: ‘/proc/1700/fd’: Permission denied
find: ‘/proc/1700/map_files’: Permission denied
find: ‘/proc/1700/fdinfo’: Permission denied
find: ‘/proc/1700/ns’: Permission denied
find: ‘/proc/2054/task/2054/fd’: Permission denied
find: ‘/proc/2054/task/2054/fdinfo’: Permission denied
find: ‘/proc/2054/task/2054/ns’: Permission denied
find: ‘/proc/2054/task/2055/fd’: Permission denied
find: ‘/proc/2054/task/2055/fdinfo’: Permission denied
find: ‘/proc/2054/task/2055/ns’: Permission denied
find: ‘/proc/2054/task/2057/fd’: Permission denied
find: ‘/proc/2054/task/2057/fdinfo’: Permission denied
find: ‘/proc/2054/task/2057/ns’: Permission denied
find: ‘/proc/2054/fd’: Permission denied
find: ‘/proc/2054/map_files’: Permission denied
find: ‘/proc/2054/fdinfo’: Permission denied
find: ‘/proc/2054/ns’: Permission denied
find: ‘/proc/3395/task/3395/fd’: Permission denied
find: ‘/proc/3395/task/3395/fdinfo’: Permission denied
find: ‘/proc/3395/task/3395/ns’: Permission denied
find: ‘/proc/3395/fd’: Permission denied
find: ‘/proc/3395/map_files’: Permission denied
find: ‘/proc/3395/fdinfo’: Permission denied
find: ‘/proc/3395/ns’: Permission denied
find: ‘/proc/3396/task/3396/fd’: Permission denied
find: ‘/proc/3396/task/3396/fdinfo’: Permission denied
find: ‘/proc/3396/task/3396/ns’: Permission denied
find: ‘/proc/3396/fd’: Permission denied
find: ‘/proc/3396/map_files’: Permission denied
find: ‘/proc/3396/fdinfo’: Permission denied
find: ‘/proc/3396/ns’: Permission denied
find: ‘/proc/3508/task/3508/fd’: Permission denied
find: ‘/proc/3508/task/3508/fdinfo’: Permission denied
find: ‘/proc/3508/task/3508/ns’: Permission denied
find: ‘/proc/3508/fd’: Permission denied
find: ‘/proc/3508/map_files’: Permission denied
find: ‘/proc/3508/fdinfo’: Permission denied
find: ‘/proc/3508/ns’: Permission denied
find: ‘/proc/3989/task/3989/fd’: Permission denied
find: ‘/proc/3989/task/3989/fdinfo’: Permission denied
find: ‘/proc/3989/task/3989/ns’: Permission denied
find: ‘/proc/3989/fd’: Permission denied
find: ‘/proc/3989/map_files’: Permission denied
find: ‘/proc/3989/fdinfo’: Permission denied
find: ‘/proc/3989/ns’: Permission denied
find: ‘/proc/10458/task/10458/fd’: Permission denied
find: ‘/proc/10458/task/10458/fdinfo’: Permission denied
find: ‘/proc/10458/task/10458/ns’: Permission denied
find: ‘/proc/10458/fd’: Permission denied
find: ‘/proc/10458/map_files’: Permission denied
find: ‘/proc/10458/fdinfo’: Permission denied
find: ‘/proc/10458/ns’: Permission denied
find: ‘/proc/17795/task/17795/fd’: Permission denied
find: ‘/proc/17795/task/17795/fdinfo’: Permission denied
find: ‘/proc/17795/task/17795/ns’: Permission denied
find: ‘/proc/17795/fd’: Permission denied
find: ‘/proc/17795/map_files’: Permission denied
find: ‘/proc/17795/fdinfo’: Permission denied
find: ‘/proc/17795/ns’: Permission denied
find: ‘/proc/17803/task/17803/fd’: Permission denied
find: ‘/proc/17803/task/17803/fdinfo’: Permission denied
find: ‘/proc/17803/task/17803/ns’: Permission denied
find: ‘/proc/17803/fd’: Permission denied
find: ‘/proc/17803/map_files’: Permission denied
find: ‘/proc/17803/fdinfo’: Permission denied
find: ‘/proc/17803/ns’: Permission denied
find: ‘/proc/18962/task/18962/fd’: Permission denied
find: ‘/proc/18962/task/18962/fdinfo’: Permission denied
find: ‘/proc/18962/task/18962/ns’: Permission denied
find: ‘/proc/18962/task/18963/fd’: Permission denied
find: ‘/proc/18962/task/18963/fdinfo’: Permission denied
find: ‘/proc/18962/task/18963/ns’: Permission denied
find: ‘/proc/18962/task/18964/fd’: Permission denied
find: ‘/proc/18962/task/18964/fdinfo’: Permission denied
find: ‘/proc/18962/task/18964/ns’: Permission denied
find: ‘/proc/18962/task/18965/fd’: Permission denied
find: ‘/proc/18962/task/18965/fdinfo’: Permission denied
find: ‘/proc/18962/task/18965/ns’: Permission denied
find: ‘/proc/18962/task/18967/fd’: Permission denied
find: ‘/proc/18962/task/18967/fdinfo’: Permission denied
find: ‘/proc/18962/task/18967/ns’: Permission denied
find: ‘/proc/18962/fd’: Permission denied
find: ‘/proc/18962/map_files’: Permission denied
find: ‘/proc/18962/fdinfo’: Permission denied
find: ‘/proc/18962/ns’: Permission denied
find: ‘/proc/18988/task/18988/fd’: Permission denied
find: ‘/proc/18988/task/18988/fdinfo’: Permission denied
find: ‘/proc/18988/task/18988/ns’: Permission denied
find: ‘/proc/18988/fd’: Permission denied
find: ‘/proc/18988/map_files’: Permission denied
find: ‘/proc/18988/fdinfo’: Permission denied
find: ‘/proc/18988/ns’: Permission denied
find: ‘/proc/19005/task/19005/fd’: Permission denied
find: ‘/proc/19005/task/19005/fdinfo’: Permission denied
find: ‘/proc/19005/task/19005/ns’: Permission denied
find: ‘/proc/19005/fd’: Permission denied
find: ‘/proc/19005/map_files’: Permission denied
find: ‘/proc/19005/fdinfo’: Permission denied
find: ‘/proc/19005/ns’: Permission denied
find: ‘/proc/19812/task/19812/fd’: Permission denied
find: ‘/proc/19812/task/19812/fdinfo’: Permission denied
find: ‘/proc/19812/task/19812/ns’: Permission denied
find: ‘/proc/19812/fd’: Permission denied
find: ‘/proc/19812/map_files’: Permission denied
find: ‘/proc/19812/fdinfo’: Permission denied
find: ‘/proc/19812/ns’: Permission denied
find: ‘/proc/19816/task/19816/fd’: Permission denied
find: ‘/proc/19816/task/19816/fdinfo’: Permission denied
find: ‘/proc/19816/task/19816/ns’: Permission denied
find: ‘/proc/19816/fd’: Permission denied
find: ‘/proc/19816/map_files’: Permission denied
find: ‘/proc/19816/fdinfo’: Permission denied
find: ‘/proc/19816/ns’: Permission denied
find: ‘/proc/19819/task/19819/fd’: Permission denied
find: ‘/proc/19819/task/19819/fdinfo’: Permission denied
find: ‘/proc/19819/task/19819/ns’: Permission denied
find: ‘/proc/19819/fd’: Permission denied
find: ‘/proc/19819/map_files’: Permission denied
find: ‘/proc/19819/fdinfo’: Permission denied
find: ‘/proc/19819/ns’: Permission denied
find: ‘/.cache’: Permission denied
find: ‘/lost+found’: Permission denied
find: ‘/run/gdm3’: Permission denied
find: ‘/run/udisks2’: Permission denied
find: ‘/run/cups/certs’: Permission denied
find: ‘/run/user/1000/systemd/inaccessible/dir’: Permission denied
find: ‘/run/sudo’: Permission denied
find: ‘/run/credentials/systemd-tmpfiles-setup.service’: Permission denied
find: ‘/run/credentials/systemd-tmpfiles-setup-dev.service’: Permission denied
find: ‘/run/credentials/systemd-sysctl.service’: Permission denied
find: ‘/run/credentials/systemd-sysusers.service’: Permission denied
find: ‘/run/systemd/propagate’: Permission denied
find: ‘/run/systemd/unit-root’: Permission denied
find: ‘/run/systemd/inaccessible/dir’: Permission denied
find: ‘/run/initramfs’: Permission denied
find: ‘/root’: Permission denied
find: ‘/tmp/systemd-private-4f15d220a9734c03a26d66ff5d527b83-systemd-timesyncd.service-avBAJK’: Permission denied
find: ‘/tmp/systemd-private-4f15d220a9734c03a26d66ff5d527b83-upower.service-d3Fo72’: Permission denied
find: ‘/tmp/systemd-private-4f15d220a9734c03a26d66ff5d527b83-fwupd.service-rZKleD’: Permission denied
find: ‘/tmp/tracker-extract-3-files.113’: Permission denied
find: ‘/tmp/systemd-private-4f15d220a9734c03a26d66ff5d527b83-colord.service-BEQUHt’: Permission denied
find: ‘/tmp/systemd-private-4f15d220a9734c03a26d66ff5d527b83-systemd-logind.service-ZhEfZs’: Permission denied
find: ‘/tmp/systemd-private-4f15d220a9734c03a26d66ff5d527b83-low-memory-monitor.service-5xo5tB’: Permission denied
find: ‘/tmp/systemd-private-4f15d220a9734c03a26d66ff5d527b83-power-profiles-daemon.service-y12B4B’: Permission denied
find: ‘/tmp/systemd-private-4f15d220a9734c03a26d66ff5d527b83-ModemManager.service-MfKhTr’: Permission denied
find: ‘/tmp/systemd-private-4f15d220a9734c03a26d66ff5d527b83-switcheroo-control.service-WF7nrN’: Permission denied
find: ‘/tmp/systemd-private-4f15d220a9734c03a26d66ff5d527b83-geoclue.service-9xrqav’: Permission denied
find: ‘/usr/share/polkit-1/rules.d’: Permission denied
/usr/share/openssh/sshd_config
find: ‘/sys/kernel/tracing’: Permission denied
find: ‘/sys/kernel/debug’: Permission denied
find: ‘/sys/fs/pstore’: Permission denied
find: ‘/sys/fs/bpf’: Permission denied
find: ‘/etc/polkit-1/rules.d’: Permission denied
find: ‘/etc/ssl/private’: Permission denied
find: ‘/etc/cups/ssl’: Permission denied
/etc/ssh/sshd_config
find: ‘/var/cache/apparmor/201d1af9.0’: Permission denied
find: ‘/var/cache/apt/archives/partial’: Permission denied
find: ‘/var/cache/ldconfig’: Permission denied
find: ‘/var/cache/private’: Permission denied
find: ‘/var/cache/cups’: Permission denied
find: ‘/var/tmp/systemd-private-4f15d220a9734c03a26d66ff5d527b83-geoclue.service-EpYlzC’: Permission denied
find: ‘/var/tmp/systemd-private-4f15d220a9734c03a26d66ff5d527b83-fwupd.service-uOlbCL’: Permission denied
find: ‘/var/tmp/systemd-private-4f15d220a9734c03a26d66ff5d527b83-systemd-timesyncd.service-BvISGv’: Permission denied
find: ‘/var/tmp/systemd-private-4f15d220a9734c03a26d66ff5d527b83-power-profiles-daemon.service-7PjQBY’: Permission denied
find: ‘/var/tmp/systemd-private-4f15d220a9734c03a26d66ff5d527b83-low-memory-monitor.service-x8naP1’: Permission denied
find: ‘/var/tmp/systemd-private-4f15d220a9734c03a26d66ff5d527b83-ModemManager.service-KKlvZR’: Permission denied
find: ‘/var/tmp/systemd-private-4f15d220a9734c03a26d66ff5d527b83-systemd-logind.service-jpPk57’: Permission denied
find: ‘/var/tmp/systemd-private-4f15d220a9734c03a26d66ff5d527b83-upower.service-Z3dSlz’: Permission denied
find: ‘/var/tmp/systemd-private-4f15d220a9734c03a26d66ff5d527b83-switcheroo-control.service-80gagm’: Permission denied
find: ‘/var/tmp/systemd-private-4f15d220a9734c03a26d66ff5d527b83-colord.service-oBa1vg’: Permission denied
find: ‘/var/log/speech-dispatcher’: Permission denied
find: ‘/var/log/private’: Permission denied
find: ‘/var/log/gdm3’: Permission denied
find: ‘/var/spool/cron/crontabs’: Permission denied
find: ‘/var/spool/cups’: Permission denied
find: ‘/var/lib/udisks2’: Permission denied
find: ‘/var/lib/apt/lists/partial’: Permission denied
find: ‘/var/lib/polkit-1’: Permission denied
find: ‘/var/lib/NetworkManager’: Permission denied
find: ‘/var/lib/AccountsService/users’: Permission denied
find: ‘/var/lib/bluetooth’: Permission denied
find: ‘/var/lib/colord/.cache’: Permission denied
find: ‘/var/lib/private’: Permission denied
find: ‘/var/lib/fwupd/gnupg’: Permission denied
find: ‘/var/lib/gdm3’: Permission denied
```
# 2. Users

## A. Nouveau user

🌞 **Créer un nouvel utilisateur**

```bash
fata@debian:/home$ su
Password:
root@debian:/home# sudo useradd -m -d /home/papier_alu marmotte
root@debian:/home# echo "marmotte:chocolat" | sudo chpasswd
root@debian:/home# grep marmotte /etc/passwd
marmotte:x:1001:1001::/home/papier_alu:/bin/sh
root@debian:/home# exit
fata@debian:/home$ su - marmotte
Password:
$ whoami
marmotte
```

## B. Infos enregistrées par le système

🌞 Prouver que cet utilisateur a été créé

```bash
fata@debian:/home$ su
Password:
root@debian:/home# sudo cat /etc/passwd | grep marmotte
marmotte:x:1001:1001::/home/papier_alu:/bin/sh
```

🌞 Déterminer le hash du password de l'utilisateur marmotte

```bash
root@debian:/home# sudo cat /etc/shadow | grep marmotte
marmotte:$y$j9T$jFWVYI6DlmJ.2swl7Asij1$0cfBRoAtPY3GQvy0CIE6srBkqsZYpp3Do9SR843JhO/:20039:0:99999:7:::
```
## C. Hint sur la ligne de commande

## D. Connexion sur le nouvel utilisateur

🌞 **Tapez une commande pour vous déconnecter : fermer votre session utilisateur**

```bash
root@debian:/home# exit
exit
fata@debian:/home$
```
🌞 **Assurez-vous que vous pouvez vous connecter en tant que l'utilisateur `marmotte`**

```bash
fata@debian:/home$ su - marmotte
Password:
$ whoami
marmotte
$
```
# III. Programmes et paquets

# 1. Programmes et processus

## A. Run then kill

🌞 **Lancer un processus `sleep`**

```bash
fata@debian:~$ sleep 1000
```
🌞 **Terminez le processus `sleep` depuis le deuxième terminal**

```bash
fata@debian:~$ ps -fe | grep sleep
fata        6329    6278  0 17:36 pts/1    00:00:00 sleep 1000
fata        6378    6361  0 17:37 pts/2    00:00:00 grep sleep

fata@debian:~$ kill
```
## B. Tâche de fond

🌞 **Lancer un nouveau processus `sleep`, mais en tâche de fond**

```bash
fata@debian:~$ sleep 1000 &
[1] 6541
```

🌞 **Visualisez la commande en tâche de fond**

```bash
fata@debian:~$ ps -fe | grep sleep
fata        6541    6503  0 17:40 pts/1    00:00:00 sleep 1000
fata        6543    6503  0 17:41 pts/1    00:00:00 grep sleep
```

Le PID : 6541

## C. Find paths

🌞 **Trouver le chemin où est stocké le programme `sleep`**

```bash
fata@debian:~$ su - root
Password:
root@debian:~# find / -name "sleep"
find: ‘/run/user/1000/doc’: Permission denied
find: ‘/run/user/1000/gvfs’: Permission denied
find: ‘/run/user/1001/doc’: Permission denied
find: ‘/run/user/1001/gvfs’: Permission denied
/usr/bin/sleep
/usr/lib/klibc/bin/sleep
```

🌞 Tant qu'on est à chercher des chemins : **trouver les chemins vers tous les fichiers qui s'appellent `.bashrc`**

```bash
root@debian:~# find / -name "*.bashrc"
find: ‘/run/user/1000/doc’: Permission denied
find: ‘/run/user/1000/gvfs’: Permission denied
find: ‘/run/user/1001/doc’: Permission denied
find: ‘/run/user/1001/gvfs’: Permission denied
/root/.bashrc
/home/papier_alu/.bashrc
/home/fata/.bashrc
/usr/share/doc/adduser/examples/adduser.local.conf.examples/bash.bashrc
/usr/share/doc/adduser/examples/adduser.local.conf.examples/skel/dot.bashrc
/usr/share/base-files/dot.bashrc
/etc/bash.bashrc
/etc/skel/.bashrc
```

## D. La variable PATH

🌞 **Vérifier que**

```bash
root@debian:~# find / -name "sleep"
find: ‘/run/user/1000/doc’: Permission denied
find: ‘/run/user/1000/gvfs’: Permission denied
find: ‘/run/user/1001/doc’: Permission denied
find: ‘/run/user/1001/gvfs’: Permission denied
/usr/bin/sleep
/usr/lib/klibc/bin/sleep
root@debian:~# find / -name "ssh"
find: ‘/run/user/1000/doc’: Permission denied
find: ‘/run/user/1000/gvfs’: Permission denied
/run/user/1000/keyring/ssh
/run/user/1000/gcr/ssh
find: ‘/run/user/1001/doc’: Permission denied
find: ‘/run/user/1001/gvfs’: Permission denied
/run/user/1001/keyring/ssh
/run/user/1001/gcr/ssh
/usr/share/runit/meta/ssh
/usr/share/bash-completion/completions/ssh
/usr/bin/ssh
/usr/lib/apt/methods/ssh
/etc/runit/runsvdir/default/ssh
/etc/default/ssh
/etc/sv/ssh
/etc/init.d/ssh
/etc/ssh
/var/log/runit/ssh
root@debian:~# find / -name "ping"
find: ‘/run/user/1000/doc’: Permission denied
find: ‘/run/user/1000/gvfs’: Permission denied
find: ‘/run/user/1001/doc’: Permission denied
find: ‘/run/user/1001/gvfs’: Permission denied
/usr/share/bash-completion/completions/ping
/usr/bin/ping
```

```bash 
root@debian:~# echo $PATH
/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

# 2. Paquets

🌞 **Installer le paquet `firefox`**

```bash
root@debian:~# apt install git
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following additional packages will be installed:
  git-man liberror-perl patch
Suggested packages:
  git-daemon-run | git-daemon-sysvinit git-doc git-email
  git-gui gitk gitweb git-cvs git-mediawiki git-svn ed
  diffutils-doc
The following NEW packages will be installed:
  git git-man liberror-perl patch
0 upgraded, 4 newly installed, 0 to remove and 73 not upgraded.
Need to get 9,467 kB of archives.
After this operation, 48.5 MB of additional disk space will be used.
Do you want to continue? [Y/n] y
Get:1 http://deb.debian.org/debian bookworm/main amd64 liberror-perl all 0.17029-2 [29.0 kB]
Get:2 http://deb.debian.org/debian bookworm/main amd64 git-man all 1:2.39.5-0+deb12u1 [2,054 kB]
Get:3 http://deb.debian.org/debian bookworm/main amd64 git amd64 1:2.39.5-0+deb12u1 [7,256 kB]
Get:4 http://deb.debian.org/debian bookworm/main amd64 patch amd64 2.7.6-7 [128 kB]
Fetched 9,467 kB in 1s (18.6 MB/s)
Selecting previously unselected package liberror-perl.
(Reading database ... 151590 files and directories currently installed.)
Preparing to unpack .../liberror-perl_0.17029-2_all.deb ...
Unpacking liberror-perl (0.17029-2) ...
Selecting previously unselected package git-man.
Preparing to unpack .../git-man_1%3a2.39.5-0+deb12u1_all.deb ...
Unpacking git-man (1:2.39.5-0+deb12u1) ...
Selecting previously unselected package git.
Preparing to unpack .../git_1%3a2.39.5-0+deb12u1_amd64.deb ...
Unpacking git (1:2.39.5-0+deb12u1) ...
Selecting previously unselected package patch.
Preparing to unpack .../patch_2.7.6-7_amd64.deb ...
Unpacking patch (2.7.6-7) ...
Setting up liberror-perl (0.17029-2) ...
Setting up patch (2.7.6-7) ...
Setting up git-man (1:2.39.5-0+deb12u1) ...
Setting up git (1:2.39.5-0+deb12u1) ...
Processing triggers for man-db (2.11.2-2) ...
```

🌞 **Utiliser une commande pour lancer Firefox**

```bash
root@debian:~# firefox
Error: no DISPLAY environment variable specified
```

🌞 **Mais aussi déterminer...**

```bash
 ???? not working :(
```

# IV. Poupée russe

🌞 **Récupérer le fichier `meow`**

```bash
root@debian:~# wget https://gitlab.com/it4lik/b1-os/-/raw/main/tp/2/meow
--2024-11-11 16:57:35--  https://gitlab.com/it4lik/b1-os/-/raw/main/tp/2/meow
--2024-11-19 17:53:39--  https://gitlab.com/it4lik/b1-os/-/raw/main/tp/2/meow
Resolving gitlab.com (gitlab.com)... 172.65.251.78, 2606:4700:90:0:f22e:fbec:5bed:a9b9
Connecting to gitlab.com (gitlab.com)|172.65.251.78|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 18016947 (17M) [application/octet-stream]
Saving to: ‘meow’

meow            100%[=======>]  17.18M  22.3MB/s    in 0.8s

2024-11-19 17:53:40 (22.3 MB/s) - ‘meow’ saved [18016947/18016947]

-bash: --2024-11-11: command not found
```

🌞 **Trouver le dossier `dawa/`**

```bash
root@debian:~# file meow
meow: Zip archive data, at least v2.0 to extract, compression method=deflate
root@debian:~# mv meow meow.zip
root@debian:~# unzip meow.zip
Archive:  meow.zip
  inflating: meow
root@debian:~# ls dawa/
ls: cannot access 'dawa/': No such file or directory
root@debian:~# file meow.zip
meow.zip: Zip archive data, at least v2.0 to extract, compression method=deflate
root@debian:~# ls
meow  meow.zip
root@debian:~# file meow
meow: XZ compressed data, checksum CRC64
root@debian:~# mv meow meow.xz
root@debian:~# xz -d meow.xz
root@debian:~# file meow
meow: bzip2 compressed data, block size = 900k
root@debian:~# mv meow meow.bz2
root@debian:~# bunzip2 meow.bz2
root@debian:~# file meow
meow: RAR archive data, v5
```

🌞 **Dans le dossier `dawa/`, déterminer le chemin vers**

```bash

```