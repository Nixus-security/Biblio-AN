# Circulation de l'information : groupe Biblio-AN

Complété en séance 1. Chaque section est rédigée et poussée depuis le compte de son auteur.

## 1. Rôles
Rédigé par : @Nixus-security

- **Auteur** : la personne qui produit une issue, du code ou de la documentation. Elle est responsable de la clarté : si quelqu'un doit lui poser une question, son travail n'est pas terminé.
- **Relecteur** : un autre membre du groupe, qui questionne, vérifie et demande des changements. Il n'est jamais l'auteur du changement qu'il relit.
- **Mainteneur** : trie les issues (labels, doublons), décide du merge et fait respecter les règles.

Dans le groupe, chacun est tour à tour auteur et relecteur. Les pull requests sont relues par au moins un autre membre, puis mergées par le mainteneur. L'auteur d'un changement ne le valide jamais seul.

## 2. Où circule chaque information
Rédigé par : @Nixus-security

| Information | Qui la produit | Qui la valide | Où elle est stockée | Durée de vie |
|---|---|---|---|---|
| Code source | L'auteur du changement, via une branche | Un relecteur (review), puis le mainteneur (merge) | Dépôt Git, historique des commits et pull requests | Toute la vie du projet |
| Bug signalé | Toute personne qui constate le bug | Le mainteneur (tri, labels, fermeture) | Issue GitHub (modèle Signaler un bug) | Jusqu'à sa correction, puis archivé dans l'historique |
| Décision technique | L'auteur, via une PR | Un autre membre, puis le mainteneur | ADR dans `docs/adr/` du dépôt | Tant que la décision reste valable |
| Documentation d'installation | L'auteur, via une PR | Un autre membre, qui la teste en suivant le texte | `README.md` du dépôt | Toute la vie du projet, mise à jour avec le code |
| Question rapide entre membres | Tout le monde | Personne | [Discord / WhatsApp : mettre l'outil réellement utilisé] | Quelques heures |
| Compte rendu de réunion | Le membre qui l'écrit | Les autres membres | [Wiki GitHub ou outil réel du groupe] | Jusqu'à la prochaine réunion |

Toute décision prise à l'oral ou dans le chat est recopiée dans l'issue ou la PR concernée, avec un lien. Aucun mot de passe ni clé d'API dans le dépôt, ni dans le chat.

## 3. Règles de l'équipe
Rédigé par : @Nixus-security

- **Titres d'issue** : ce qui se passe, et où (symptôme observable). L'urgence n'y figure pas, elle va dans un label. Pas de message recopié tel quel, pas de solution à la place du constat.
- **Contenu d'une issue** : contexte (commit, système, version de Python), étapes numérotées depuis `python biblio.py init`, comportement attendu, comportement observé copié. Un seul problème par issue.
- **Labels** : `bug`, `enhancement`, `question`, `securite` pour une faille. Une faille de sécurité est décrite sans mode d'emploi d'attaque.
- **Qui trie** : le mainteneur (labels, doublons). Les doublons sont cherchés avant d'écrire, puis fermés avec « Duplicate of #n ».
- **Qui assigne** : le mainteneur, une seule personne par issue, au moment où elle est prise en charge.
- **À partir de la séance 2 : aucun push direct sur `main`.** Tout passe par une pull request relue par au moins un autre membre, avec `Closes #n` dans la description.
- **Branches** : `fix/<n° issue>-mot-cle` pour les corrections, `docs/<n°>-mot-cle` pour la documentation.
- **Avant chaque commit** : Fetch origin puis Pull origin, car plusieurs personnes modifient les mêmes fichiers.
