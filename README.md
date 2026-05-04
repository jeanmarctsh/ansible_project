# 🚀 Ansible Automation 

---

## 🎯 Objectif

Ce projet vise à automatiser la gestion d'une infrastructure Linux avec Ansible, notamment :

    - Création d'un utilisateur ansible (rua) dédié pour une gestion centralisée et sécurisée,
    - Organiser la configuration avec group_vars et host_vars pour une meilleure scalabilité
    - Installation et gestion de différents paquets via le module apt,
    - Simplifier la configuration des serveurs et réduire les interventions manuelles
    - etc...

---

## 📁 Structure du projet

la structure générale du projet se présente de la manière suivante:

```text
ansible-automation/
├── Images                  # Captures d'écran et schémas du projet
├── inventory/              
│   ├── group_vars
│   │   ├── all.yml         # Variables communes à tous les serveurs
│   │   └── workers.yml     # Variables spécifiques au groupe "workers"
│   ├── host_vars           
│   │   ├── worker1.yml     # Configuration propre au serveur worker1
│   │   └── worker2.yml     # Configuration propre au serveur worker2
│   └── hosts.yml           # Fichier d'inventaire pour les différents hôtes et groupes
├── playbook/               
│   ├── cleanup.yml         # Nettoyage des fichiers temporaires
│   ├── common.yml          # Configuration de base pour les groupes communs 
│   ├── create_user.yml     # Création automatique et gestion des utilisateurs SSH
│   ├── install.yml         # Playbook principal d'installation
│   ├── ping.yml            # Test de connectivité simple
│   └── uninstall.yml       # Désinstallation de différents paquets
├── .gitignore              # Fichiers à exclure de Git (logs, secrets)
├── ansible.cfg             # Configuration personnalisée d'Ansible
└── README.md               # Documentation du projet

```





---

## 🛠️ technologies utilisées

    - Linux (Ubuntu)
    - Ansible
    - Git
    - SSH
    - YAML

---
## ▶️ Exécution du Playbook.

Pour l'exécution d'un Playbook, voici quelques commandes à lancer:

> 1. Test de connectivité sur les deux serveurs (worker1 et worker2)

```bash
ansible all -i inventory/hosts.yml -m ping

```
---

> 2. Installation de difféents paquets au niveau du worker1 avec le tag : install_A

```bash
ansible-playbook -i inventory/hosts.yml playbook/install.yml --tags="install_A"

```

---

> 3. Installation de difféents paquets au niveau du worker2 avec le tag : install_B

```bash
ansible-playbook -i inventory/hosts.yml playbook/common.yml --tags="install_B"

```

---

## 📫 CONTACT

[![Email](https://img.shields.io/badge/Email-red?style=for-the-badge&logo=gmail)](mailto:jeanmarctshimbombo@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-blue?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/jean-marc-ngandu-b60796222)
[![GitHub](https://img.shields.io/badge/GitHub-black?style=for-the-badge&logo=github)](https://github.com/jeanmarctsh)
