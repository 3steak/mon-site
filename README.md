# 📌 Projet Raspberry Pi 5 - Serveur Web PHP avec GitHub

## 🌟 Introduction

Ce projet transforme un Raspberry Pi 5 en un serveur web complet, permettant d'héberger des sites PHP et de gérer les fichiers via GitHub. Il inclut Apache, PHP, MariaDB (MySQL), PHPMyAdmin et un système de déploiement avec Git.

## 🛠️ Installation et Configuration

1️⃣ Préparer le Raspberry Pi

Installation de Raspberry Pi OS avec Raspberry Pi Imager

Configuration initiale (Wi-Fi, SSH, mises à jour) :

sudo apt update && sudo apt upgrade -y

2️⃣ Installation du serveur web

sudo apt install apache2 php libapache2-mod-php mariadb-server php-mysql -y

3️⃣ Installation de PHPMyAdmin

sudo apt install phpmyadmin -y

Accès : http://<IP_DU_RASPBERRY>/phpmyadmin

4️⃣ Configuration Git pour le déploiement

Installation de Git :

sudo apt install git -y

Génération et ajout de la clé SSH à GitHub :

ssh-keygen -t ed25519 -C "tonemail@example.com"
cat ~/.ssh/id_ed25519.pub

Copier la clé et l'ajouter dans GitHub (Settings → SSH Keys)

Initialisation du dépôt dans /var/www/html :

cd /var/www/html
git init
git remote add origin git@github.com:TonUser/mon-site.git

5️⃣ Push & Déploiement

git add .
git commit -m "Premier commit"
git push -u origin main

## 🚀 Accéder au site

En local : http://localhost

Depuis un autre appareil : http://<IP_DU_RASPBERRY>

## 📂 Gestion des fichiers via GitHub

Déploiement sur le serveur

Chaque modification doit être poussée via :

git add .
git commit -m "Mise à jour"
git push origin main

## 🔥 Fonctionnalités futures

✅ Hébergement de plusieurs sites (Virtual Hosts)
✅ Sécurisation avec HTTPS (Let's Encrypt)
✅ Automatisation du déploiement (GitHub Actions)
