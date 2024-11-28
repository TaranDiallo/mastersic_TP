# Déploiement et Sécurisation d'un Site WordPress dans le Cloud

Ce projet a pour objectif de déployer et sécuriser un site WordPress hébergé dans un environnement cloud. Il inclut la configuration initiale du serveur, l'installation de WordPress, ainsi que la mise en œuvre de plusieurs couches de sécurité pour protéger le site et les données qu'il traite.

## Fonctionnalités principales

- **Installation et configuration de WordPress** : Déploiement d'un site WordPress sur un serveur VPS avec Nginx et MariaDB.
- **Sécurisation du site** :
  - Activation du HTTPS avec **Certbot** et Let's Encrypt pour le chiffrement des communications.
  - Gestion des DNS et sécurisation des requêtes HTTP via **Cloudflare**.
  - Authentification avec `htpasswd` pour protéger l'accès au site lors de la phase de développement.
  - Mise en place de règles de pare-feu avec **ModSecurity**.
  - Analyse du code source avec **SonarCloud** pour détecter les vulnérabilités.
  - Configuration de scans réguliers pour maintenir un niveau élevé de sécurité.
- **Surveillance et gestion de la sécurité** : Utilisation d'outils comme **Wazuh** pour la détection des intrusions et le suivi des vulnérabilités.

## Prérequis

- Serveur VPS avec un système d'exploitation Linux (Ubuntu recommandé).
- Accès root pour la configuration initiale, puis utilisation d'un utilisateur non-root pour des raisons de sécurité.
- DNS configuré pour pointer vers le serveur (géré via Cloudflare).

## Technologies utilisées

- **Serveur Web** : Nginx
- **Base de Données** : MariaDB
- **Langages** : PHP, Bash
- **Outils de Sécurité** : Certbot, Cloudflare, ModSecurity, SonarCloud, Wazuh
- **Gestion des accès** : htpasswd

## Sécurisation HTTPS et DNS

1. **Certbot** :
   - Utilisé pour générer et renouveler automatiquement les certificats SSL/TLS via Let's Encrypt.
   - Permet d'assurer une connexion sécurisée entre les utilisateurs et le serveur.

2. **Cloudflare** :
   - Gère les enregistrements DNS pour simplifier la configuration.
   - Fournit une protection automatique contre les attaques DDoS et sécurise les requêtes HTTP avec son mode "Full SSL (Strict)".
   - Redirige automatiquement les requêtes HTTP vers HTTPS pour garantir que tout le trafic est chiffré.

## Instructions d'installation

1. Configurer le serveur avec Nginx, MariaDB et PHP.
2. Télécharger et installer WordPress dans un répertoire sécurisé.
3. Activer HTTPS avec Certbot.
4. Configurer Cloudflare pour gérer les DNS et activer ses options de sécurité (comme Always Use HTTPS et SSL/TLS).
5. Configurer le fichier `.htaccess` pour renforcer la protection.
6. Mettre en œuvre les règles de pare-feu et configurer ModSecurity.
7. Configurer SonarCloud pour l'analyse du code source.
8. Installer et configurer Wazuh pour la surveillance.

## Objectifs

Ce projet vise à fournir un environnement sécurisé et optimisé pour l'hébergement de sites WordPress, en adoptant les meilleures pratiques pour la protection des données et la détection proactive des vulnérabilités.

Pour plus de détails techniques sur la mise en œuvre, consultez notre [Documentation technique](https://nomande-consulting.notion.site/D-ploiement-et-s-curisation-d-un-site-WordPress-1130f38684d6808c94ffe8c9f9b23130?pvs=4).

## Contributeurs

- [Ousmane Diallo](https://www.linkedin.com/in/diallousmane/)
- [Hélène Moulet](https://www.linkedin.com/in/h%C3%A9l%C3%A8ne-moulet/)
- [Bailo Diallo](https://www.linkedin.com/in/bailosank/)
- [Matteo LE PERA](https://www.linkedin.com/in/matteo-le-pera-45ab89227/)


## Licence

Ce projet est sous licence [MIT](LICENSE). Vous êtes libre de le modifier et de le redistribuer, sous réserve de respecter les termes de la licence.

---

*Développé par un groupe d'étudiant du [Master SIC -Cybersécurité de l'Université Paris Panthéon Sorbonne](https://formations.pantheonsorbonne.fr/fr/catalogue-des-formations/master-M/master-management-des-systemes-d-information-KBUV9JGI/master-parcours-systemes-d-information-et-de-connaissance-sous-parcours-cybersecurite-apprentissage-KD8MHGXN.html)*
