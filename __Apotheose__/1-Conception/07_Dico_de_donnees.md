# Dictionnaire de données

Date : 15/07/2022
___

## User

| Mot | Description|Type | Spécificités |
|---|---|---|---|
|user | utilisateur |table||
| id| identification de l'utilisateur| integer|primary key / not null|
|username| nom d'utilisateur|text| not null|
|email | adresse e-mail|text| not null|
|password| mot de passe|text| not null|
|isActive| statut actif ou inactif|boolean| not null|
|title| métier, fonction ou spécialité de l'utilisateur|text|null|
|presentation| biographie de l'utilisateur|text|null|
|profile_pic_url| lien vers la photo de profil|text|null|
|linkedin_url| lien vers le profil Linked In|text|null|
|github_url| lien vers le profil Github|text|null|
|instagram_url| lien vers le profil Instagram|text|null|
|twitter_url| lien vers le profil Twitter|text|null|
|portfolio_url| lien vers son site personnel|text|null|
|created_at| date de création du compte|timestamp with timezone|not null, default now()|
|updated_at| date de la mise à jour du profil|timestamp with timezone||
|role_id| identification du role|integer| not null, references role(id)|

## Category

| Mot | Description|Type | Spécificités |
|---|---|---|---|
|category| catégorie de l'article ou du ticket d'erreur|table||
|id| identification de la catégorie|integer|primary key / not null|
|name| nom de la catégorie|text|not null|

## Article

| Mot | Description|Type | Spécificités |
|---|---|---|---|
|article| un article|table||
|id| identification de l'article|integer|primary key / not null|
|title| titre de l'article|text|null|
|abstract| résumé de l'article|text|null|
|content|contenu de l'article|text|null|
|created_at| date de création de l'article|timestamp with timezone|not null, default now()|
|updated_at| date de la mise à jour de l'article|timestamp with timezone||
|status_id|identification du statut de l'article|integer|not null / reference status (id)|
|user_id|identification de l'auteur d'un article|integer|not null / reference user (id)|

## Error

| Mot | Description|Type | Spécificités |
|---|---|---|---|
|error| un ticket d'erreur|table||
|id| identification du ticket d'erreur|integer|primary key / not null|
|title| titre du ticket d'erreur|text|null|
|abstract| résumé du ticket d'erreur|text|null|
|content|contenu du ticket d'erreur|text|null|
|created_at| date de création du ticket d'erreur|timestamp with timezone|not null, default now()|
|updated_at| date de la mise à jour du ticket d'erreur|timestamp with timezone||
|status_id|identification du statut du ticket d'erreur|integer|not null / reference status (id)|
|user_id|identification de l'auteur d'un ticket d'erreur|integer|not null / reference user (id)|
|error_comment_id|identification du commentaire - solution au ticket d'erreur|integer|not null / reference error_comment (id)|

## Article comment

| Mot | Description|Type | Spécificités |
|---|---|---|---|
|article_comment| un commentaire d'un article|table||
|id| identification d'un commentaire|integer|primary key / not null|
|content|contenu du commentaire|text|not null|
|created_at| date de création du commentaire|timestamp with timezone|not null, default now()|
|updated_at| date de la mise à jour du commentaire|timestamp with timezone||
|article_id|identification de l'article auquel est rattaché le commentaire|integer|not null / reference article (id)|
|user_id|identification de l'auteur du commentaire|integer|not null / reference user (id)|

## Error comment

| Mot | Description|Type | Spécificités |
|---|---|---|---|
|error_comment| un commentaire d'un ticket d'erreur|table||
|id| identification d'un commentaire|integer|primary key / not null|
|content|contenu du commentaire|text|not null|
|created_at| date de création du commentaire|timestamp with timezone|not null, default now()|
|updated_at| date de la mise à jour du commentaire|timestamp with timezone||
|error_id|identification du ticket d'erreur auquel est rattaché le commentaire|integer|not null / reference error (id)|
|user_id|identification de l'auteur du commentaire|integer|not null / reference user (id)|

## Bad word

| Mot | Description|Type | Spécificités |
|---|---|---|---|
|bad_word|mot interdit / mot vulgaire|table||
|id| identification du mot interdit|integer|primary key / not null|
|word| le mot|text| not null|

## Role

| Mot | Description|Type | Spécificités |
|---|---|---|---|
|role| rôle d'un utilisateur (utilisateur enregistré, auteur ou admin)|table||
|id|identification du rôle|integer|primary key / not null|
|name| intitulé du rôle|text|not null|

## Status

| Mot | Description|Type | Spécificités |
|---|---|---|---|
|status| statut d'un article ou d'un ticket d'erreur|table||
|id| identification du statut|integer|primary key / not null|
|name| intitulé du statut|text |not null|

___

[Page précédente](./06_Endpoints.md) | [Page suivante](./08_Design.md) | [Accueil](../../README.md)
