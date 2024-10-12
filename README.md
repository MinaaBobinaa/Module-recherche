# Repertoire des Cours de Finance

## Description
Ce projet implémente un module de recherche d'informations sur un répertoire de cours de finance en ligne. Le programme utilise les **streams** et les **expressions lambda** en Java pour effectuer diverses opérations de recherche et de filtrage sur les cours présents dans un fichier CSV.

Le fichier CSV contient des informations sur chaque cours telles que le titre, le prix, le nombre d'étudiants, l'évaluation moyenne, le niveau d'expérience requis, et la date de publication.

## Fonctionnalités
- Charger un répertoire de cours de finance depuis un fichier CSV.
- Rechercher des cours par titre, évaluation, niveau d'expérience, prix, nombre d'étudiants, période de publication, etc.
- Retourner des statistiques et des listes de cours basées sur des critères donnés.
- Utiliser des **expressions lambda** et des **streams** pour traiter les données de manière efficace.

## Fichiers fournis
- `CoursFinance.java` : Classe modélisant un cours de finance.
- `CoursFinanceInvalideException.java` : Exception lancée lors de la création d'un cours avec des données invalides.
- `repertoireCoursFinances.csv` : Fichier CSV contenant les cours de finance.

## Méthodes Principales
- **obtenirNbCours()** : Retourne le nombre total de cours dans le répertoire.
- **rechercherParTitre(String chaineCaracteres)** : Retourne la liste des cours dont le titre contient la chaîne de caractères spécifiée.
- **rechercherParEvaluation(float eval, boolean plusPetite)** : Retourne les cours ayant une évaluation plus petite ou supérieure/égale à `eval`.
- **rechercherParNiveauExperience(List<String> niveauxExperience)** : Retourne les cours dont le niveau d’expérience correspond aux niveaux donnés.
- **rechercherParPeriode(LocalDateTime dateHeureDebut, LocalDateTime dateHeureFin)** : Retourne les cours publiés dans la période spécifiée.
- **rechercherParNbEtudiants(int n)** : Retourne les `n` cours ayant le plus ou le moins d’étudiants inscrits.
- **rechercherParPourcentageEvaluation(int n)** : Retourne les cours ayant les meilleurs ou les moins bons pourcentages d’évaluations.
- **rechercherParPrix(float prix, boolean estPlusGrand)** : Retourne les cours dont le prix est plus grand ou plus petit que celui spécifié.

## Format du fichier CSV
Le fichier CSV contient les colonnes suivantes :
- **ID** : Numéro d'identification unique du cours
- **Titre** : Titre du cours
- **Prix** : Prix du cours (0 si gratuit)
- **Nb d'étudiants** : Nombre d'étudiants inscrits
- **Nb d'évaluations** : Nombre d'évaluations pour le cours
- **Évaluation** : Note moyenne (sur 10) du cours
- **Niveau d'expérience** : Niveau d'expérience requis (Junior, Intermédiaire, Senior, Tous)
- **Durée** : Durée du cours en minutes
- **Date de publication** : Date et heure de publication (format `aaaa-mm-jj HH:mm`)


