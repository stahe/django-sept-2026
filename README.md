# Introduction étape par étape au framework web [Django]

**Le cours est en ligne ici : [https://stahe.github.io/django-sept-2026/](https://stahe.github.io/django-sept-2026/)**

## Auteur

Le cours et l'ensemble de ses codes ont été écrits par **Claude**, l'IA d'Anthropic, **unique auteur**, à la demande de Serge Tahé (septembre 2026).

## Présentation

Ce cours enseigne pas à pas la construction d'une application web MVC avec le framework **Django 6.1** et le langage **Python 3.13**. Les pages HTML y sont fabriquées par le serveur, avec les **gabarits de Django** (le langage DTL), sans framework JavaScript côté navigateur. L'accès aux données passe par l'**ORM de Django**.

Il transpose dans le monde Django le cours [Introduction étape par étape au framework web [Symfony]](https://stahe.github.io/symfony-sept-2026/), lui-même issu des cours [Laravel](https://stahe.github.io/laravel-sept-2026/), [Flask](https://stahe.github.io/flask-sept-2026/), [Spring MVC](https://stahe.github.io/springmvc-sept-2026/), [ASP.NET Core MVC](https://stahe.github.io/aspnetcoremvc-sept-2026/) et [NestJS](https://stahe.github.io/nestjs-html-sept-2026/). Les exemples portent les mêmes numéros et traitent les mêmes sujets : on peut comparer les frameworks exemple par exemple.

## Contenu

| Chapitre | Sujets | Exemples |
|---|---|---|
| Vues, routage, réponses | routes (`urls.py`, `path`, `include`), vues, réponses, redirections, middlewares, services partagés | 01 à 06 |
| Le modèle d'une vue | paramètres de la requête, classes de données, formulaires comme validateurs, décorateurs, requêtes POST et JSON | 07 à 12 |
| Les gabarits et les formulaires | DTL, gabarit parent, fragments nommés, processeurs de contexte, balises et filtres, formulaires Django, Post/Redirect/Get, messages, protection anti-CSRF | 13 à 21 |
| Internationalisation | une application en français et en anglais (gettext : fichiers `.po` et `.mo`, pluriels) | 22 |
| Portées des données | requête, session, cache, cookies signés | 23 |
| Le cycle de vie d'une requête | middlewares, signaux, pages d'erreur | 24 |
| Authentification et autorisation | jeton JWT dans un cookie, rôles, captcha, limitation des tentatives | 25 à 27 |
| Architecture en couches | web / métier / DAO avec l'ORM de Django et MySQL, transactions, verrou optimiste | 28 |
| Étude de cas | **RdvMedecins**, une application de prise de rendez-vous médicaux, commentée fichier par fichier | - |

L'étude de cas `rdvmedecins2-django` gère trois rôles (administrateur, médecins, patients) : agendas, réservations, gestion des médecins et des clients, création de compte protégée par captcha, interface FR / EN. Elle utilise la même base de données `dbrdvmedecins2` que les autres versions de l'application.

## Prérequis

- Python 3.12 ou plus récent (testé avec 3.13), avec `pip` et `venv` ;
- MySQL 8.4 ou plus récent, ou MariaDB 10.11 ou plus récent (Laragon sous Windows) ;
- Visual Studio Code avec les extensions Python, Pylance et Django ;
- curl.

Les codes sont téléchargeables depuis le site du cours. Les environnements virtuels (dossiers `.venv`) n'y figurent pas : `python -m venv .venv` puis `pip install -r requirements.txt` les fabriquent, une fois dans le dossier `exemples`, une fois dans le dossier `rdvmedecins2-django`.
