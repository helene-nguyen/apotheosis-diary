# Dictionnaire de données

Date : 15/07/2022
___

## User

| Mot | Description|
|---|---|
|user | utilisateur |
| id| identification de l'utilisateur|
|username| nom d'utilisateur|
|email | adresse e-mail|
|password| mot de passe|
|status| statut actif ou inactif|
|title| métier, fonction ou spécialité de l'utilisateur|
|presentation| biographie de l'utilisateur|
|linkedin_url| lien vers le profil Linked In|
|github_url| lien vers le profil Github|
|instagram_url| lien vers le profil Instagram|
|twitter_url| lien vers le profil Twitter|
|portfolio_url| lien vers son site personnel|
|created_at| date de création du compte|
|updated_at| date de la mise à jour du profil|
|role_id| identification du role|

## Category

| Mot | Description|
|---|---|
|category| catégorie de l'article ou du ticket d'erreur|
|id| identification de la catégorie|
|name| nom de la catégorie|

## Article

| Mot | Description|
|---|---|
|article| un article|
|id| identification de l'article|
|title| titre de l'article|
|abstract| résumé de l'article|
|content|contenu de l'article|
|created_at| date de création de l'article|
|updated_at| date de la mise à jour de l'article|
|status_id|identification du statut de l'article|
|user_id|identification de l'auteur d'un article|

## Error

| Mot | Description|
|---|---|
|error| un ticket d'erreur|
|id| identification du ticket d'erreur|
|title| titre du ticket d'erreur|
|abstract| résumé du ticket d'erreur|
|content|contenu du ticket d'erreur|
|created_at| date de création du ticket d'erreur|
|updated_at| date de la mise à jour du ticket d'erreur|
|status_id|identification du statut du ticket d'erreur|
|user_id|identification de l'auteur d'un ticket d'erreur|
|error_comment_id|identification du commentaire - solution au ticket d'erreur|

## Article comment

| Mot | Description|
|---|---|
|article_comment| un commentaire d'un article|
|id| identification d'un commentaire|
|content|contenu du commentaire|
|created_at| date de création du commentaire|
|updated_at| date de la mise à jour du commentaire|
|article_id|identification de l'article auquel est rattaché le commentaire|
|user_id|identification de l'auteur du commentaire|

## Error comment

| Mot | Description|
|---|---|
|error_comment| un commentaire d'un ticket d'erreur|
|id| identification d'un commentaire|
|content|contenu du commentaire|
|created_at| date de création du commentaire|
|updated_at| date de la mise à jour du commentaire|
|error_id|identification du ticket d'erreur auquel est rattaché le commentaire|
|user_id|identification de l'auteur du commentaire|

## Bad word

| Mot | Description|
|---|---|
|bad_word|mot interdit / mot vulgaire|
|id| identification du mot interdit|
|word| le mot|

## Role

| Mot | Description|
|---|---|
|role| rôle d'un utilisateur (utilisateur enregistré, auteur ou admin)|
|id|identification du rôle|
|name| intitulé du rôle|

## Status

| Mot | Description|
|---|---|
|status| statut d'un article ou d'un ticket d'erreur|
|id| identification du statut|
|name| intitulé du statut|

___

[Page précédente](./06_Endpoints.md) | [Page suivante](./08_Design.md) | [Accueil](../../README.md)
