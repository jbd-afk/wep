
Gestion des donnees (v2)
------------------------
En mode organisateur, chaque donnee creee dans l'appli peut aussi etre **supprimee** :
- WEPien (retire aussi des equipes et des matchs),
- equipe (ses matchs sont supprimes),
- match,
- publication du fil.
- Le bouton **Reinit.** du header remet l'appareil aux donnees par defaut du code (utile pour partir sur de vraies donnees).
En mode spectateur, aucune suppression n'est possible.

Synchronisation multi-appareils (v4)
------------------------------------
Comme wep-primes : une ressource JSON unique (type JSONBin / Supabase Storage) partagee en GET+PUT.
- En mode organisateur, dans le **Fil WEP**, encart **SYNCHRONISATION** : saisir l'**URL de sync** et la **cle** (envoyee en en-tete `X-Master-Key`), puis *Enregistrer la config*.
- Automatique ensuite sur tous les appareils configures :
  - chaque modification (score, match, fiche, actu...) est renvoyee **4 s** apres la derniere action,
  - l'appli recupere les donnees **au demarrage puis toutes les 60 s** si la ressource est plus recente (dernier-writer-wins, horodatage `_sync`),
  - boutons manuels **Recuperer** / **Partager** dans le Fil WEP.
- Spectateurs et projecteur Android : configurer la sync une fois, l'appli suit scores et actus en quasi direct.
- Sans config de sync, l'appli reste 100% locale (localStorage), rien ne change.
- Configuration conservee par appareil (cles `wep-syncu` / `wep-synck`), non incluse dans les donnees partagees.

Edition complete des archives (v5)
----------------------------------
En mode organisateur, chaque edition archivee est desormais modifiable en place :
- annee (avec anti-doublon), dates, lieu,
- **presences** : boutons cliquables present/absent avec les **surnoms** affiches,
- **equipes conservees** : renommage, suppression, ajout, et composition (chips par equipe),
- **matchs joues** : discipline, equipes, scores, ajout/suppression de lignes (aussi archives automatiquement par le bouton "Archiver cette edition"),
- **classement** : nom d'equipe, victoires, defaites, points, ajout/suppression de lignes,
- **photo de groupe** : import depuis l'appareil (redimensionnee), affichage, retrait.
Les spectateurs voient l'edition en lecture seule, surnoms affiches.
