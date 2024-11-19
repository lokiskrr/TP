# TP5 : Le compilateur ton pire meilleur ami

## Sommaire

- [TP5 : Le compilateur ton pire meilleur ami](#tp5--le-compilateur-ton-pire-meilleur-ami)
  - [Sommaire](#sommaire)
- [0. Prérequis](#0-prérequis)
- [I. Programme minimal](#i-programme-minimal)
  - [1. Compilation](#1-compilation)
  - [2. Analyse du programme compilé](#2-analyse-du-programme-compilé)
  - [2. Librairie et compilation dynamique](#2-librairie-et-compilation-dynamique)
    - [A. Intro lib](#a-intro-lib)
    - [B. Intro compilation dynamique](#b-intro-compilation-dynamique)
    - [C. Tracer les appels à des librairies](#c-tracer-les-appels-à-des-librairies)
  - [3. Compilation statique](#3-compilation-statique)
  - [4. Compilation cross-platform](#4-compilation-cross-platform)
- [II. Ptits challenges de cracking](#ii-ptits-challenges-de-cracking)
  - [1. Install Ghidra](#1-install-ghidra)
  - [2. Patch manuel programme simple](#2-patch-manuel-programme-simple)
  - [3. Root-me](#3-root-me)
  - [4. Ptit chall maison](#4-ptit-chall-maison)

# 0. Prérequis

🌞 **Créer un répertoire de travail dans votre répertoire personnel**

```bash 

```

# I. Programme minimal

## 1. Compilation

```bash 
done :)
```

## 2. Analyse du programme compilé

🌞 **Retrouvez à l'aide de `readelf` l'architecture pour laquelle le programme est compilé**

```bash 

```

🌞 **Afficher la liste des *sections* contenues dans le *programme***

```bash 

```

🌞 **Affichez le code *assembleur* de la section `.text` à l'aide d'`objdump`**

```bash 

```

## 2. Librairie et compilation dynamique

### A. Intro lib

### B. Intro compilation dynamique

### C. Tracer les appels à des librairies

🌞 **Tracez à l'aide de la commande `ldd` les *librairies* appelées par...**

```bash 

```

🌞 **Parmi les *librairies* appelées par *hello2*, déterminer le type du fichier nommé `libc.so.X`**

```bash 

```

## 3. Compilation statique

🌞 **Affichez le type des fichiers `hello2` et `hello3`**

```bash 

```

🌞 **Affichez leurs tailles**

```bash 

```

## 4. Compilation cross-platform

🌞 **Affichez l'*architecture* de votre *CPU***

```bash 

```

🌞 **Vérifiez que vous avez la commande `x86_64-linux-gnu-gcc`**

```bash 

```

🌞 **Compilez votre fichier `hello3.c` dans un fichier cible nommé `hello4` vers une autre *architecture* que la vôtre**

```bash 

```

🌞 **[Désassemblez](../../cours/memo/glossary.md#désassembler) `hello3` et `hello4` à l'aide d'`objdump`**

```bash 

```

🌞 **Essayez d'exécuter le *programme* `hello4`**

```bash 

```

# II. Ptits challenges de cracking

## 1. Install Ghidra

🌞 **Avec une commande `apt search`, déterminez si le paquet `ghidra` est disponible**

```bash 

```

🌞 **Ajouter l'URL des dépôts Kali à vos dépôts existants**

```bash 

```

🌞 **Ajoutez la clé publique des gars de chez Kali**

```bash 

```

🌞 **Mettez à jour la liste des dépôts que votre OS connaît actuellement**

```bash 

```

🌞 **Avec une commande `apt search`, déterminez si le paquet `ghidra` est disponible**

```bash 

```

🌞 **Installez le paquet `ghidra`**

```bash 

```

## 2. Patch manuel programme simple

🌞 **Récupérez le code de [`password_2.c`](../../cours/cracking/code_demo/password_2.c) sur la machine Linux et compilez-le**

```bash 

```

## 3. Root-me

## 4. Ptit chall maison

🌞 **Récupérer le flag du programme [`kaddate_challenge`](./kaddate_challenge)**

```bash 

```
