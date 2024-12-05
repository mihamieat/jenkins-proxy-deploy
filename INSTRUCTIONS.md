# The bill, please!

## Instructions

### L’ADDITION, S’IL VOUS PLAÎT ? 🧮

Bienvenue à l'hackathon dédié à l’automatisation de déploiement avec `Jenkins` 🛠️ et les outils d’IaC (Infrastructure as Code). Pendant cette journée, vous travaillerez en équipe pour créer une infrastructure professionnelle qui intègre `Jenkins`, un reverse proxy `Nginx`. L’objectif est de rendre cette infrastructure entièrement automatisée et sécurisée.

Ce hackathon est une opportunité d’appliquer vos compétences en Terraform et Ansible dans un environnement collaboratif et structuré.

Vous devrez configurer votre `Jenkins` en tant que service afin qu’il n’occupe pas votre terminal. Pour que votre instance de `Jenkins` soit accessible de manière sécurisée, vous utiliserez un serveur `Nginx` (configuré en <ins>reverse proxy</ins>). Vous compléterez votre installation en associant un nom de domaine ainsi que des certificats SSL à votre instance.

Vous travaillerez chacun sur votre machine, mais vous avancerez en groupe et au même rythme afin d’avoir le même résultat à la fin de la journée.

👉 Avant de vous lancer, prenez le temps d’analyser le sujet et la documentation de `Jenkins` et de `Nginx` avec votre groupe pour comprendre son fonctionnement. Vous devrez déployer manuellement la version `Debian`, sans passer par Docker ou Snap.

👉 Afin de comprendre le fonctionnement de cette configuration, vous allez d’abord la réaliser <ins>en local sur votre VM</ins>. Cela vous permettra d’avoir les fichiers de configuration sous la main pour l’automatisation de votre infrastructure.

👉 Créez ensuite un dossier "`Jenkins`" qui contiendra toutes les ressources du projet, telles que vos fichiers de configuration Terraform et Ansible.

### CRÉATION DE L’INFRASTRUCTURE

👉 En utilisant Terraform, préparez le déploiement sur AWS ainsi que la configuration réseau adéquate (pare-feu).

👉 Validez l’étape précédente en déployant l’infrastructure via la commande terraform apply.

### DÉPLOIEMENT DE LA PLATEFORME

👉 En utilisant Ansible, préparez le déploiement de `Jenkins` et de `Nginx` ainsi que leurs dépendances sur la machine `Debian`.

Le service `Jenkins` devra être accessible depuis l’extérieur en https sur le sous-domaine de votre choix et se lancer automatiquement au démarrage du système.

👉 Validez l’étape précédente en démarrant le <ins>playbook Ansible</ins>.

Ce processus montre l’intégration de Terraform pour la gestion de l’infrastructure et Ansible pour la configuration des services. Vous pouvez reproduire cette infrastructure en un clic, garantissant ainsi la rapidité et la fiabilité du déploiement. Bonne chance ! 🎉

## My notes

- For the first login, `Jenkins` asks for the password located at `/var/lib/`Jenkins`/secrets/initialAdminPassword`
- In Jenkins UI, Required plugins are chosen for install
-
