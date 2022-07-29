# API Endpoints

Date : 15/07/2022

___

## /API/V1

### <u>User</u>

|Method| Route| Description| Returns |Page|
|---|---|---|---|---|
| GET | /users | Récupérer tous les utilisateurs | Tableau d'objets JSON | Dashboard Admin |
| GET | /users/:id | Récupérer un utilisateur par son id | Tableau d'objets JSON | profil utilisateur |
| POST | /signin | Connexion | Objet JSON avec les tokens | Modale de connexion |
| POST | /signup | Inscription | String de confirmation | Page inscription|
| GET | /signout | Déconnexion | String de confirmation | Modale de déconnexion |
| PATCH | /users/:id | Mise à jour des informations de profil | String de confirmation | Page profil de l'utilisateur|
| DELETE | /users/:id | Suppression d'un compte utilisateur | Objet JSON | Dashboard |
| PUT | /users/:id | Désactivation d'un utilisateur | Objet JSON | Dashboard |
| GET | /users/:id/panel | Récupérer tous le détail d'un utilisateur |Tableau d'objets JSON | Dashboard admin |
|POST|/refreshToken| Met à jour le token pour les autorisations| Objet JSON | Dashboard admin, utilisateur et auteur, page profil, page de creation de ticket d'erreur et d'article|

## <u>Articles</u>

|Method| Route| Description| Returns|Page|
|---|---|---|---|---|
| GET | /articles | Récupérer tous les articles | Tableau d'objets JSON | Page articles |
| GET | /articles/:id | Récupération d'un article par son id | Objet JSON | Page d'un article |
| POST | /articles | Soumettre l'article aux administrateurs| String de confirmation "en attente de validation" | Dashboard Auteur - Page de création d'article |
| PATCH | /articles/:id | Mise à jour d'un article |String "article mis à jour"| Dashboard Auteur - Page de création d'article |
| DELETE | /articles/:id | Suppression d'un article |  String "article supprimé"   | Page Dashboard auteur|
| GET | /categories/:id/articles | Récupérer tous les articles d'une catégorie | Tableau d'objets JSON | Page articles |
| GET | /users/:id/articles | Récupérer tous les articles d'un utilisateur | Tableau d'objets JSON | Profil auteur |
| POST | /articles/last | Récupérer les derniers articles publiés | Tableau d'objets JSON | Home / Page articles ? |
| POST | /articles/search | Récupérer les articles liés à la recherche | Tableau d'objets JSON | Toutes les pages |

### <u>Errors</u>

|Method| Route| Description| Returns|Page|
|---|---|---|---|---|
| GET | /errors | Récupérer tous les tickets d'erreur | Tableau d'objets JSON | Page tickets d'erreur |
| GET | /errors/:id | Récupération d'un ticket d'erreur par son id | Tableau d'objets JSON | Page d'un ticket d'erreur|
| POST | /errors | Soumettre le ticket d'erreur | String de confirmation "en attente de validation" |Création d'erreur|
| PATCH | /errors/:id | Mise à jour d'un ticket d'erreur | String "ticket d'erreur mise à jour" | Dashboard utilisateur - Page de création d'erreur |
| DELETE | /errors/:id | Suppression d'un ticket d'erreur | String "ticket d'erreur supprimé" | Dashboard utilisateur - Page de création d'erreur |
| GET | /categories/:id/errors | Récupérer tous les tickets d'erreur d'une catégorie | Tableau d'objets JSON | Page tickets d'erreur |
| GET | /users/:id/errors | Récupérer tous les tickets d'erreur d'un utilisateur | Tableau d'objets JSON | Profil utilisateur
| POST | /errors/last | Récupérer les derniers tickets d'erreur publiés | Tableau d'objets JSON | Home |
| POST | /errors/search | Récupérer les tickets d'erreur liés à la recherche | Tableau d'objets JSON | Toutes les pages |
| PATCH | /errors/:id/solution/:id | Valider un commentaire comme solution au ticket | String de confirmation | Page ticket d'erreur (auteur de l'erreur seulement) |

### <u>Article comments</u>

|Method| Route| Description| Returns|Page|
|---|---|---|---|---|
| GET | /articles/:id/comments | Récupérer tous les commentaires d'un article | Tableau d'objets JSON | Page article |
| POST | /articles/:id/comments | Publier un commentaire sur un article | String de confirmation | Page article |
| PATCH | /articles/:id/comments/:id | Mettre à jour un commentaire sur un article | String de confirmation | Page article |
| DELETE | /articles/:id/comments/:id | Suppression d'un commentaire sur un article | String de confirmation | Page article |
| GET | /users/:id/article_comments | Récupérer toutes les réponses d'un utilisateur à des articles | Tableau d'objets JSON | Page profil |

### <u>Error comments</u>

|Method| Route| Description| Returns|Page|
|---|---|---|---|---|
| GET | /errors/:id/comments | Récupérer tous les commentaires d'un ticket d'erreur | Tableau d'objets JSON | Page ticket d'erreur
| POST | /errors/:id/comments | Publier un commentaire sur un ticket d'erreur | String de confirmation | Page ticket d'erreur
| PATCH | /errors/:id/comments/:id | Mettre à jour un commentaire sur un ticket d'erreur | String de confirmation | Page ticket d'erreur
| DELETE | /errors/:id/comments/:id | Suppression d'un commentaire sur un ticket d'erreur | String de confirmation | Page ticket d'erreur
| GET | /users/:id/error_comments | Récupérer toutes les réponses d'un utilisateur à des tickets d'erreur | Tableau d'objets JSON | Page profil |

### <u>Categories</u>

|Method| Route| Description| Returns|Page|
|---|---|---|---|---|
| GET | /categories | Récupérer toutes les catégories | Tableau d'objets JSON | Home/Page articles/Page tickets d'erreurs/Création d'articles /Création d'erreur/ Profil utilisateur |
| GET | /articles/:id/categories | Récupérer toutes les catégories en fonction d'un article | Tableau d'objets JSON | Page article
| GET | /errors/:id/categories | Récupérer toutes les catégories en fonction d'un ticket d'erreur | Tableau d'objets JSON | Page ticket d'erreur
| POST | /categories | Créer une catégorie | String de confirmation | Dashboard Admin |
| DELETE | /categories/:id | Supprimer une catégorie | String de confirmation | Dashboard Admin |

___

[Page précédente](./05_MCD_MLD_MPD.md) | [Page suivante](./07_Dico_de_donnees.md) | [Accueil](../../README.md)
