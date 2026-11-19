Site du week-end WEP
====================

Appli autonome du WEP : un seul fichier `index.html`, aucune dependance, rien a installer.
Ouvrez-la avec un navigateur (telephone, ordinateur, ou videoprojecteur Android via Chrome plein ecran / kiosk).
Les donnees sont stockees localement (localStorage) sur chaque appareil.

Sections
--------
- **Scoreboard** : date/heure, total des points par equipe sur le week-end, matchs realises,
  match(s) en cours en grand (chrono de la duree + score, saisie +1/-1 possible),
  matchs a venir, classement provisoire, et **mode projecteur** plein ecran avec
  rotation automatique toutes les 8 s quand aucun match n'est en cours
  (classement / resultats et prochains matchs / total des points).
- **Accueil** : compte a rebours avant le prochain WEP, dernieres nouvelles, prochains rendez-vous, souvenirs.
- **Le fil WEP** : publications des organisateurs, commentaires et reactions pour tous.
- **Le live** : equipes (nom, couleur, composition propre a chaque edition),
  matchs (discipline, heure, equipes, joueurs par equipe, scores, statut a venir / en cours / termine),
  alerte quand un match se termine.
- **Les WEPiens** : fiches nom / prenom / alias / date de naissance, editions participees,
  stats personnelles non classantes (matchs joues, victoires).
- **Les archives** : une page par edition (dates, lieu, presents, composition conservee des equipes,
  resultats, photo de groupe).

Modes
-----
- **Mode organisateur** : publie, cree equipes et matchs, saisit les scores (telephone ou projecteur).
- **Mode spectateur** : consultation seule.

Prochaines etapes (vers la PWA)
-------------------------------
- manifest + service worker (installation sur ecran d'accueil),
- backend partage pour la synchronisation temps reel entre telephones et le videoprojecteur,
- notifications Web Push en cas de resultat,
- mode kiosk Android conseille sur le videoprojecteur (ex. Fully Kiosk Browser) pour un affichage autonome.
