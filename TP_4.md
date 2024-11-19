# TP4 : Safé d partission

## Sommaire

- [TP4 : Safé d partission](#tp4--safé-d-partission)
  - [Sommaire](#sommaire)
- [0. Prérequis](#0-prérequis)
- [I. Clean install](#i-clean-install)
  - [1. Ptite intro](#1-ptite-intro)
  - [2. Installz](#2-installz)
  - [3. Vérification](#3-vérification)
  - [4. Taille et inodes](#4-taille-et-inodes)
- [II. Partitioning](#ii-partitioning)
  - [1. d disk partou](#1-d-disk-partou)
  - [2. Grow !](#2-grow-)
  - [3. Montage automatique](#3-montage-automatique)
  - [4. Bonus : options de montage](#4-bonus--options-de-montage)

# 0. Prérequis
# I. Clean install
## 1. Ptite intro
## 2. Installz
## 3. Vérification

🌞 **Lister les périphériques de stockage branchés à la machine**

```bash

```

🌞 **Lister les *partitions* en cours d'utilisation**

```bash

```

## 4. Taille et inodes

🌞 **Lister la quantité d'*inodes* disponibles sur chaque *partition***

```bash

```

🌞 **Déterminer la taille (avec `du`) et l'*inode* (avec `ls`) de chacun des fichiers suivants :**

```bash

```

# II. Partitioning

## 1. d disk partou

🌞 **Repérer le nom des nouveaux disques**

```bash

```

🌞 **Ajouter ces deux disques comme des PV LVM**

```bash

```

🌞 **Créer un VG nommé `cat`**

```bash

```

🌞 **Créer un LV nommé `meoooow`**

```bash

```

🌞 **Formater la partition (le LV) en autre chose que ext4**

```bash

```

🌞 **Créer le *point de montage* `/mnt/meow`**

```bash

```

🌞 **Monter la *partition* `meoooow` sur le point de montage que vous avez créé**

```bash

```

🌞 **Vérifier avec la commande adaptée que la *partition* est utilisable et qu'elle fait 3G**

```bash

```

## 2. Grow !

🌞 **Agrandir la *partition* `/home`**

```bash

```
  
🌞 **Constatez l'agrandissement**

```bash

```

🌞 **Indiquez au filesystem que vous avez agrandi la *partition* sur laquelle il est posé**

```bash

```

🌞 **Prouvez en affichant la liste des *partitions* que la *partition* fait désormais 2G de plus**

```bash

```

🌞 **Agrandir la *partition* `meoooow` pour qu'elle occupe tout l'espace libre de son VG**

```bash

```

🌞 **Déterminer la taille de la nouvelle *partition***

```bash

```

## 3. Montage automatique

🌞 **Modifier le fichier `/etc/fstab` pour que la *partition* soit montée `/mnt/meow` automatiquement**

```bash

```

## 4. Bonus : options de montage

⭐ **Déterminer quelles options de montage permettrait d'améliorer le niveau de sécurité des données contenues sur une *partition*.**