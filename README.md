# lunqolabs.github.io

La racine du domaine `lunqolabs.github.io`.

Ce dépôt n'existe que pour servir **`app-ads.txt`** à cette racine. Les robots
qui le cherchent prennent le site déclaré dans la fiche Play Store —
`https://lunqolabs.github.io/backspace/` — puis remontent à la racine de
l'hôte. Un dépôt de projet ne sert que sous son propre chemin ; seul un dépôt
nommé d'après l'hôte sert la racine.

Les pages légales de Backspace vivent ailleurs, dans `lunqolabs/backspace`.

## app-ads.txt

Une ligne, au format de l'IAB : le domaine de la régie, l'identifiant
d'éditeur AdMob, la nature de la relation, et l'identifiant public de Google
comme autorité de certification. Rien n'y est secret — le fichier est fait
pour être lu par tout le monde.

Il ne sera vérifié qu'une fois l'application publiée : le robot part d'une
fiche de store en ligne. Tant que Backspace est en brouillon, AdMob
l'affichera comme introuvable, et ce n'est pas un échec.
