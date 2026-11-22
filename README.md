
Gestion des donnees (v2)
------------------------
En mode organisateur, chaque donnee creee dans l'appli peut aussi etre **supprimee** :
- WEPien (retire aussi des equipes et des matchs),
- equipe (ses matchs sont supprimes),
- match,
- publication du fil.
- Le bouton **Reinit.** du header remet l'appareil aux donnees par defaut du code (utile pour partir sur de vraies donnees).
En mode spectateur, aucune suppression n'est possible.

Consultation et organisation (v3)
---------------------------------
Deux liens, deux roles :
- **Lien consultation** (a partager avec tous les WEPiens) : `https://<adresse-de-l-appli>/` -- spectateur.
- **Lien organisateur** (a garder prive, quelques personnes seulement) : ajoute `?orga=wep2026` a l'adresse.
Le code organisateur est defini dans le code (`ORGA_CODE='wep2026'`), modifiable dans `index.html`.
Ces deux liens s'affichent dans l'encart jaune "LIENS A PARTAGER" du Fil WEP (visible uniquement en mode organisateur).

En mode organisateur :
- **WEPiens** : ajout, modification et suppression d'un WEPien, avec photo (choisie sur l'appareil, redimensionnee et stockee localement).
- **Logo** : bouton "Logo" dans le header pour remplacer le logo affiche en haut a gauche.
- **Matchs** : modification/suppression des resultats ; le bouton "Supprimer" d'un match reste reserve aux organisateurs.
- **Archives** : ajout d'une nouvelle edition (annee, dates, lieu), modification ou suppression d'une edition archivee, et bouton "Archiver cette edition" qui enregistre les equipes et le classement du moment dans les archives.

Ouvert a tous (consultation ET organisation) :
- Demarrer un match, marquer les points (+/-), designer les joueurs presents, terminer un match.

Limitation connue : les donnees restent stockees dans l'appareil (localStorage) tant qu'il n'y a pas de backend ; la synchronisation temps reel entre telephones est la prochaine etape.
