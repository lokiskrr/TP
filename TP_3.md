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

```

🌞 **Afficher la ligne du fichier qui concerne votre utilisateur ET celle de `root` en même temps**

```bash

```

🌞 **Afficher la liste des groupes d'utilisateurs de la *machine***

```bash

```


🌞 **Afficher la ligne du fichier qui concerne votre utilisateur ET celle de `root` en même temps**

```bash

```

## 2. Hash des passwords

🌞 **Afficher la ligne qui contient le hash du mot de passe de votre utilisateur**

```bash

```

## 3. Sudo
### A. Intro

🌞 **Faites en sorte que votre utilisateur puisse taper n'importe quelle commande `sudo`**

```bash

```

### B. Practice

🌞 **Créer un groupe d'utilisateurs**

```bash

```

🌞 **Créer un utilisateur**

```bash

```

🌞 **Prouver que l'utilisateur `imbob` est créé**

```bash

```

🌞 **Prouver que l'utilisateur `imbob` a un password défini**

```bash

```

🌞 **Prouver que l'utilisateur `imbob` appartient au groupe `stronk_admins`**

```bash

```

🌞 **Créer un deuxième utilisateur**

```bash

```

🌞 **Modifier la configuration de `sudo` pour que**

```bash

```

🌞 **Créer le dossier `/home/goodguy`** (avec une commande)

```bash

```

🌞 **Changer le répertoire personnel de `imbob`**

```bash

```

🌞 **Créer le dossier `/home/badguy`**

```bash

```
🌞 **Changer le répertoire personnel de `imnotbobsorry`**

```bash

```

🌞 **Prouver que les permissions du dossier `/home/gooduy` sont incohérentes**

```bash

```

🌞 **Modifier les permissions de `/home/goodguy`**

```bash

```

🌞 **Modifier les permissions de `/home/badguy`**

```bash

```

🌞 **Connectez-vous sur l'utilisateur `imbob`**

```bash

```

🌞 **Connectez-vous sur l'utilisateur `imnotbobsorry`**

```bash

```

# II. Processes

## 1. Jouer avec la commande ps

🌞 **Affichez les processus `bash`**

```bash

```

🌞 **Affichez tous les processus lancés par votre utilisateur**

```bash

```

🌞 **Affichez le top 5 des processus qui utilisent le plus de RAM**

```bash

```

🌞 **Affichez le *PID* du processus du service SSH**

```bash

```

🌞 **Affichez le nom du processus avec l'identifiant le plus petit**

```bash

```

## 2. Parent, enfant, et meurtre

🌞 **Déterminer le *PID* de votre shell actuel**

```bash

```

🌞 **Déterminer le *PPID* de votre shell actuel**

```bash

```

🌞 **Déterminer le nom de ce *processus***

```bash

```

🌞 **Lancer un *processus* `sleep 9999` en tâche de fond**

```bash

```

🌞 **Fermez votre session SSH**

```bash

```

# III. Services

## 1. Intro

## 2. Analyser un service existant

🌞 **S'assurer que le service `ssh` est démarré**

```bash

```

🌞 **Isolez la ligne qui indique le nom du programme lancé**

```bash

```

🌞 **Déterminer le port sur lequel écoute le service SSH**

```bash

```

🌞 **Consulter les logs du service SSH**

```bash

```

### A. Configuration du service SSH

🌞 **Identifier le fichier de configuration du serveur SSH**

```bash

```

🌞 **Modifier le fichier de conf**

```bash

```

🌞 **Redémarrer le service**

```bash

```

🌞 **Effectuer une connexion SSH sur le nouveau port**

```bash

```

### B. Le service en lui-même

🌞 **Trouver le fichier `ssh.service`**

```bash

```

🌞 **Déterminer quel est le programme lancé**

```bash

```

## 4. Créez votre propre service

🌞 **Déterminer le dossier qui contient la commande `python3`**

```bash

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