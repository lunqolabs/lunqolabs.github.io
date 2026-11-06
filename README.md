# lunqolabs.github.io

La racine du domaine `lunqolabs.github.io`. Elle sert deux choses.

## `index.html` — la page d'accueil de Lunqo Labs

Elle présente **Undersnake** et **Backspace**, et donne pour chacun son lien Google Play. Pour
Undersnake elle propose aussi la version web, sur `undersnake.lunqolabs.com`.

Cette page n'est pas décorative, elle a trois emplois :

1. **Le site web déclaré dans la fiche Play Store d'Undersnake.** Un joueur qui clique sur « Site
   web » depuis le Play Store atterrit ici.
2. **La destination des publicités Meta.** Une campagne Trafic ne peut pas pointer vers une URL
   `play.google.com/store/apps/...` — Meta la réserve à l'objectif Installations et refuse la
   diffusion. Elle accepte en revanche un site ordinaire, d'où ce détour : la publicité mène ici,
   le bouton mène à Play.
3. **L'hôte d'`app-ads.txt`** (voir plus bas), parce que les robots remontent à la racine.

Les liens Play portent un paramètre `referrer` tracé (`utm_source=lunqolabs`, `utm_medium=site`),
distinct de celui des publicités : Play Console sépare ainsi les installations venues de cette page
de celles venues de Meta, dans *Acquisition d'utilisateurs*.

GitHub Pages sert `index.html` en priorité : ce README n'est plus rendu, il reste la documentation
du dépôt.

## `app-ads.txt`

Une ligne, au format de l'IAB : le domaine de la régie, l'identifiant d'éditeur AdMob, la nature de
la relation, et l'identifiant public de Google comme autorité de certification. Rien n'y est secret.

Les robots partent du site déclaré dans une fiche de store puis remontent à la racine de l'hôte. Un
dépôt de projet ne sert que sous son propre chemin ; seul un dépôt nommé d'après l'hôte sert la
racine. C'est pourquoi ce dépôt existe.

**Deux fiches Play pointent ici** : Backspace, et Undersnake depuis le 6 novembre 2026. Le même
identifiant éditeur couvre les deux, une seule ligne suffit donc.

Undersnake a d'abord déclaré son propre domaine, `undersnake.lunqolabs.com`. Le fichier y était
pourtant correct — servi en 200, bonne ligne, accessible à tous les agents Google testés — mais
AdMob n'a jamais réussi à le valider. La comparaison a disculpé le fichier : ORBGRID, qui passe,
a plus de commentaires et autant de caractères non-ASCII. La seule variable restante était
l'hébergeur, qui tourne derrière un proxy anti-robots. D'où le déplacement ici.

Les pages légales de Backspace vivent dans `lunqolabs/backspace`, celles d'Undersnake sur
`undersnake.lunqolabs.com`.
