# ⚽ StageHub

**StageHub** est une application web de gestion complète des rassemblements sportifs (stages, compétitions, matchs préparatoires), conçue pour les sélections nationales, clubs ou académies. Elle permet aux Team Managers et membres du staff de planifier, coordonner et superviser efficacement tous les aspects logistiques, techniques et médicaux d’un regroupement.

---

## 🧩 Fonctionnalités principales

- 🗓️ **Création et gestion de rassemblements** (stage, compétition, mixte)
- 👥 **Convocation des joueurs** avec historique et statut (présent, blessé, absent)
- 🧑‍💼 **Ajout des membres du staff** (coach, médecin, officier...) avec ou sans accès système
- 🛏️ **Affectation des chambres** dans un ou plusieurs hébergements successifs
- 📆 **Programme journalier dynamique** (entraînement, repas, matchs, repos...)
- 📱 **Suivi de la remise et restitution des téléphones**, horodaté avec système de QR code
- 🩺 **Suivi médical des joueurs** (consultations, traitements, jours de repos)
- 🖼️ **Gestion des médias** (photos, vidéos, documents) avec contrôle de la visibilité
- 📊 **Rapports automatiques** (journaliers, par joueur, fin de stage)

---

## 👤 Rôles & accès

- **Super Admin** : gestion complète du système
- **Admin** : gestion des utilisateurs, validations
- **Team Manager** : point focal de l’équipe (crée staff, rassemblements, programme...)
- **Team Staff** : coachs, médecins, officiers (accès personnalisés)
- *(optionnel)* **Joueur** : accès restreint à ses propres infos

---

## 🚀 Technologies utilisées

- **Laravel 10+** (PHP 8.2)
- **MySQL 8+**
- **Docker & Docker Compose**
- **Nginx (serveur web)**
- **MailDev (test d’envoi d’emails)**
- **phpMyAdmin (interface SQL)**

---

## ⚙️ Installation rapide (en local avec Docker)

```bash
git clone https://github.com/ton-org/stagehub.git
cd stagehub
cp .env.example .env
docker-compose up -d --build
docker exec -it stagehub_app composer install
docker exec -it stagehub_app php artisan key:generate
docker exec -it stagehub_app php artisan migrate
