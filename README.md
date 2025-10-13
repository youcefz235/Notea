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
