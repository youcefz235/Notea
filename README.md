<<<<<<< HEAD
<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

<p align="center">
<a href="https://github.com/laravel/framework/actions"><img src="https://github.com/laravel/framework/workflows/tests/badge.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

## About Laravel

Laravel is a web application framework with expressive, elegant syntax. We believe development must be an enjoyable and creative experience to be truly fulfilling. Laravel takes the pain out of development by easing common tasks used in many web projects, such as:

- [Simple, fast routing engine](https://laravel.com/docs/routing).
- [Powerful dependency injection container](https://laravel.com/docs/container).
- Multiple back-ends for [session](https://laravel.com/docs/session) and [cache](https://laravel.com/docs/cache) storage.
- Expressive, intuitive [database ORM](https://laravel.com/docs/eloquent).
- Database agnostic [schema migrations](https://laravel.com/docs/migrations).
- [Robust background job processing](https://laravel.com/docs/queues).
- [Real-time event broadcasting](https://laravel.com/docs/broadcasting).

Laravel is accessible, powerful, and provides tools required for large, robust applications.

## Learning Laravel

Laravel has the most extensive and thorough [documentation](https://laravel.com/docs) and video tutorial library of all modern web application frameworks, making it a breeze to get started with the framework. You can also check out [Laravel Learn](https://laravel.com/learn), where you will be guided through building a modern Laravel application.

If you don't feel like reading, [Laracasts](https://laracasts.com) can help. Laracasts contains thousands of video tutorials on a range of topics including Laravel, modern PHP, unit testing, and JavaScript. Boost your skills by digging into our comprehensive video library.

## Laravel Sponsors

We would like to extend our thanks to the following sponsors for funding Laravel development. If you are interested in becoming a sponsor, please visit the [Laravel Partners program](https://partners.laravel.com).

### Premium Partners

- **[Vehikl](https://vehikl.com)**
- **[Tighten Co.](https://tighten.co)**
- **[Kirschbaum Development Group](https://kirschbaumdevelopment.com)**
- **[64 Robots](https://64robots.com)**
- **[Curotec](https://www.curotec.com/services/technologies/laravel)**
- **[DevSquad](https://devsquad.com/hire-laravel-developers)**
- **[Redberry](https://redberry.international/laravel-development)**
- **[Active Logic](https://activelogic.com)**

## Contributing

Thank you for considering contributing to the Laravel framework! The contribution guide can be found in the [Laravel documentation](https://laravel.com/docs/contributions).

## Code of Conduct

In order to ensure that the Laravel community is welcoming to all, please review and abide by the [Code of Conduct](https://laravel.com/docs/contributions#code-of-conduct).

## Security Vulnerabilities

If you discover a security vulnerability within Laravel, please send an e-mail to Taylor Otwell via [taylor@laravel.com](mailto:taylor@laravel.com). All security vulnerabilities will be promptly addressed.

## License

The Laravel framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
=======
Notea — Plateforme d’apprentissage légère (Laravel + HTML/CSS/JS)

Notea centralise le cycle d’apprentissage : cours → sources d’étude → prises de notes → projets → remises → feedback → amélioration.
Objectif : une interface sobre, fiable et facile à expliquer, pensée pour les étudiants et enseignants.

🎯 Description du projet

Problème : contenus d’étude éparpillés (PDF, liens, notes personnelles, consignes de projets) ⇒ perte de temps et suivi difficile.

Solution : une plateforme unique pour structurer les cours et sources, noter avec contexte (tags, PJ), remettre des projets et améliorer grâce au feedback enseignant, le tout avec une recherche + filtres rapides.

👥 Rôles

Étudiant : s’inscrit aux cours, consulte les sources, crée des notes (tags + pièces jointes), remet des projets, applique le feedback.

Enseignant : crée les cours, publie les sources, définit les projets, commente/évalue les remises, propose des pistes d’amélioration.

Invité (option) : lecture seule via lien signé et temporaire.

⚙️ Fonctionnalités principales (MVP)

Cours & Sources

Créer des cours et y associer des sources (PDF, vidéos, liens).

Lister/consulter les ressources d’un cours.

Notes & Tags

CRUD des notes reliées à un cours et/ou à une source.

Tags multiples par note, recherche (titre + contenu) et filtres par tags (logique ET).

Pièces jointes (image/PDF/audio) avec aperçu HTML.

Historique des versions d’une note + restauration.

Projets & Remises

Définir des projets (consignes, fichiers exemples).

Remettre un travail (fichier ou lien) avec statut Brouillon → Soumis → Révisé.

Feedback & Amélioration

Feedback enseignant (commentaire + score optionnel).

Items d’amélioration (to-dos cochables) pour guider la révision.

Partage sécurisé

Lien signé (lecture seule, expiration automatique) pour partager une note/remise.

💡 Valeur ajoutée

Contexte fort : notes reliées aux cours/sources → on retrouve mieux, plus vite.

Apprentissage itératif : versions + feedback + items d’amélioration → progression visible.

Simplicité pédagogique : parcours linéaires, choix techniques faciles à justifier.

🧰 Technologies utilisées

Back-end : PHP 8.2+, Laravel 11

Routing & Controllers (convention REST), Eloquent ORM (relations claires),

FormRequest (validations), Policies (RBAC simple),

Storage public (uploads + aperçus), URLs signées (partage sécurisé).

Base de données : SQLite (démo) ou MySQL/PostgreSQL (prod).

Front-end : Blade, HTML5, CSS3, JavaScript vanilla (interactions légères).

Outils : Git & GitHub (versions, issues), (option) Vite pour les assets.

🧠 Modèle conceptuel (vue d’ensemble)

User (rôle student / teacher)

Course, Enrollment (User↔Course)

Resource (PDF/vidéo/lien) liée à Course

Note (User, référence optionnelle → Course/Resource) + Tag (pivot note_tag)

Attachment (fichiers liés à Note), NoteVersion

Project (par Course) → Submission (par Student)

Feedback (par Teacher sur Submission) → ImprovementItem (to-dos)

✅ Qualités non fonctionnelles

Accessibilité : HTML sémantique, labels, focus visible, navigation clavier.

Sécurité : validations serveur, policies, CSRF, liens signés en lecture seule.

Performance : pagination, index DB, requêtes simples (LIKE/ILIKE).

Maintenabilité : structure MVC claire, relations Eloquent explicites.

🗺️ Roadmap (suggestion courte)

V1 : Cours & Sources, Notes & Tags (recherche/filtres, PJ, versions), Projets & Remises, Feedback & Items, Partage signé.

V1.1 : Corbeille (SoftDeletes), Export PDF/ZIP.

V2 : Recherche enrichie (pg_trgm / FULLTEXT), rubriques d’évaluation avancées, tableaux de bord.

🎤 Prompt (à mettre en bas du repo ou à réciter à l’oral)

Prompt / Pitch
« Notea est une plateforme d’apprentissage légère en Laravel + HTML/CSS/JS qui relie tout le cycle d’étude : cours, sources, notes (avec tags & pièces jointes), projets, remises, puis feedback enseignant avec items d’amélioration. Les notes sont reliées à leur contexte (cours/source) pour être retrouvées en secondes grâce à la recherche et aux filtres. On garde un historique des versions pour prouver la progression et on peut partager en lecture seule via un lien signé. Les choix techniques sont simples et pédagogiques (Eloquent, FormRequest, Policies, Storage) pour un produit sobre, fiable et présentable à un jury. »
>>>>>>> a9726bfb3a2bb029562158d6829fa2c2e7daab93
