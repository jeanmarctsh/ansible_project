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

![Structure du projet](Images/structure_globale.PNG)

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

> 1. Test ping sur les deux serveurs (worker1 et worker2)

```bash
ansible all -i inventory/inventory.yml -m ping

```
---

> 2. Installation de difféents paquets au niveau du worker1 avec le tag : install_A

```bash
ansible-playbook -i inventory/inventory.yml playbook/install.yml --tags="install_A"

```

---

> 3. Installation de difféents paquets au niveau du worker2 avec le tag : install_B

```bash
ansible-playbook -i inventory/inventory.yml playbook/common.yml --tags="install_B"

```

---

## 📫 CONTACT

[![Email](https://img.shields.io/badge/Email-red?style=for-the-badge&logo=gmail)](mailto:jeanmarctshimbombo@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-blue?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/jean-marc-ngandu-b60796222)
[![GitHub](https://img.shields.io/badge/GitHub-black?style=for-the-badge&logo=github)](https://github.com/jeanmarctsh)
