# Idées de projets de fin d'etudes

## 1) Contexte et objectif general
Ce document propose des sujets de projets pour des etudiants de derniere annee en ecole d'ingenieur numerique.

Orientation pedagogique souhaitee :
- IA appliquee
- approche concrete et ludique
- integration conjointe de developpement logiciel et d'electronique

## 2) Contraintes de depart
- Charge projet: 180h par etudiant
- Effectif: 25 etudiants
- Organisation: 5 groupes de 5 etudiants
- Volume horaire cible par groupe: environ 900h
- Decoupage temporel: 3 periodes (4, 5 et 9 semaines, soit 18 semaines au total)
- Evaluation orale: 1 soutenance a la fin de chaque periode + 1 soutenance finale (soit 4 soutenances)

## 3) Analyse rapide du besoin
Les idees initiales sont pertinentes car elles couvrent deja:
- un usage visible et motivant (assistant, vehicule, serre)
- des dimensions IA appliquee (vision, NLP, prediction, optimisation)
- des interfaces concretes avec le monde physique (capteurs, actionneurs, embarque)

Points a completer pour un cadrage pedagogique robuste:
- definir des livrables clairs par projet
- imposer une architecture minimum (embarque + backend + interface)
- prevoir un plan de tests et une validation terrain
- harmoniser la difficulte entre groupes
- fixer des criteres d'evaluation communs

## 4) Socle technique recommande (commun a tous les groupes)
Chaque projet devrait inclure au minimum:
- Electronique/embarque: microcontroleur (ESP32, Raspberry Pi Pico) ou SBC (Raspberry Pi)
- Logiciel: API/backend en .NET 10 (ASP.NET Core) avec interface Blazor
- Interface: application web ou mobile
- IA: au moins un module exploitable en demonstration (classification, detection, recommandation, prediction)
- DevOps: gestion de version, CI simple, documentation deploiement

Principes transverses inspires du projet serre (a appliquer a tous les sujets):
- Local-first: chaine logicielle hebergee en local (acquisition, stockage, backend, interface), sans dependance cloud obligatoire.
- Continuite de service: le systeme doit conserver ses fonctions critiques meme si l'interface tombe ou si le reseau est indisponible.
- Sobriete mesuree: chaque groupe suit et justifie les ressources consommees (energie, eau, materiaux, temps machine).
- UX utile: les interfaces privilegient des actions claires plutot que des dashboards complexes.
- Droit au post-mortem: en cas d'echec terrain, le groupe doit produire une analyse technique argumentee basee sur les donnees.

## 5) Organisation du travail (180h par etudiant)
Proposition de decoupage:
- Cadrage et etat de l'art: 20h
- Conception systeme (architecture, choix materiel, schema de donnees): 25h
- Developpement v1 (MVP): 60h
- Integration electronique + IA: 40h
- Tests, robustesse, optimisation: 20h
- Documentation, soutenance, demo finale: 15h

Cadence par periodes:
- Periode 1 (Semaines 1 a 4): cadrage, etat de l'art, architecture cible, preuve de faisabilite
- Periode 2 (Semaines 5 a 9): MVP logiciel + premier prototype electronique integre + consolidation technique
- Periode 3 (Semaines 10 a 18): module IA operationnel, integration systeme, robustesse, tests en conditions reelles, finalisation des livrables

Soutenances:
- Soutenance 1: fin Periode 1 (semaine 4, revue de cadrage)
- Soutenance 2: fin Periode 2 (semaine 9, revue MVP)
- Soutenance 3: fin Periode 3 (semaine 18, revue d'integration et validation technique)
- Soutenance finale: presentation finale complete (resultats, demo, retour critique)

## 6) Livrables attendus
Pour chaque groupe:
- Cahier des besoins et cas d'usage
- Dossier architecture (materiel + logiciel)
- Depot code versionne propre
- Prototype fonctionnel demonstrable
- Rapport technique (resultats, limites, pistes d'amelioration)
- Presentation finale avec demonstration en conditions reelles

### Trame obligatoire du cahier des charges (fonctionnel)
Chaque groupe doit produire un cahier des charges avec, au minimum, les rubriques suivantes:
- Contexte et probleme cible: qui est l'utilisateur, quel besoin concret est resolu.
- Perimetre: ce qui est inclus, ce qui est explicitement hors perimetre.
- Parties prenantes: utilisateur final, exploitant, mainteneur, evaluateur.
- Parcours utilisateur cibles: 3 a 5 scenarios nominaux + 2 scenarios d'erreur.
- Exigences fonctionnelles (EF): liste numerotee EF-01, EF-02, ... testables.
- Exigences non fonctionnelles (ENF): latence, disponibilite, securite, local-first, sobriete.
- Contraintes materielles: capteurs/actionneurs imposes ou optionnels, budget cible, encombrement.
- Donnees et traceabilite: quelles donnees sont stockees, duree de retention, format d'export.
- Strategie de validation: tests unitaires, tests integration, tests terrain, criteres d'acceptation.
- Gestion des risques: top 5 risques + plan de mitigation.

### Format recommande des exigences
- EF-xx (fonctionnelle): "Le systeme doit ..." + mesure de succes + methode de test.
- ENF-xx (non fonctionnelle): "Le systeme doit ..." + seuil chiffre.

Exemples:
- EF-03: Le systeme doit detecter un evenement critique et notifier l'utilisateur en moins de 3 secondes.
- ENF-02: Le systeme doit continuer ses fonctions vitales pendant au moins 30 minutes sans interface graphique.
- ENF-05: Le systeme doit fonctionner sans dependance cloud obligatoire sur le reseau local.

### Definition of done (obligatoire)
Un projet est considere valide uniquement si:
- le MVP est demonstrable en conditions reelles,
- les exigences EF/ENF critiques sont verifiees par des tests traces,
- les modes de panne et le mode degrade sont demontres,
- un post-mortem technique est fourni en cas d'echec partiel.

### Livrables attendus a chaque soutenance
- Soutenance 1 (Semaine 4): probleme cible, EF/ENF v1, architecture v1, preuve de faisabilite.
- Soutenance 2 (Semaine 8): MVP integre (software + electronique), tests de base, premier retour utilisateur.
- Soutenance 3 (Semaine 12): systeme consolide, IA exploitable, tests d'integration et robustesse.
- Soutenance 4 (Semaine 16): validation terrain, corrections, dossier quasi final.
- Soutenance finale: bilan global, demo complete, mesures KPI, limites et feuille de route.

## 7) Grille d'evaluation (exemple)
- Qualite de la solution technique: 30%
- Integration electronique + logiciel: 20%
- Pertinence et maitrise du module IA: 20%
- Qualite logicielle (tests, proprete, documentation): 15%
- Gestion de projet et travail d'equipe: 10%
- Qualite de la demonstration finale: 5%

Suggestion de repartition des notes par soutenance:
- Soutenance 1: 10%
- Soutenance 2: 15%
- Soutenance 3: 20%
- Soutenance 4: 20%
- Soutenance finale: 35%

## 8) Idees de projets detaillees

### Projet A - Mini robot interactif de bureau
Objectif:
Construire un mini robot interactif de bureau capable de capter des demandes vocales, d'afficher des informations sur son ecran et d'agir physiquement de maniere simple.

Utilisateurs cibles:
- Etudiant utilisateur final
- Tuteur qui consulte la progression des taches

Composants possibles:
- Base mobile compacte ou châssis de bureau
- Ecran embarque pour afficher et confirmer les actions
- Microphone + haut-parleur + boutons physiques
- Raspberry Pi ou mini-PC local
- Backend IA (reconnaissance vocale, classification d'intention, synthese vocale)
- Capteurs simples de presence ou d'interaction

Detail fonctionnel attendu:
- Parcours 1: l'utilisateur parle au robot, qui reformule la demande, l'affiche a l'ecran puis confirme l'action.
- Parcours 2: le robot affiche des rappels, une to-do list ou un etat simple sur son ecran.
- Parcours 3: le robot effectue une action physique simple (tourner, se positionner, presenter une carte, allumer un signal) pour rendre l'IA tangible.
- Parcours 4: le tuteur visualise les interactions (historique, taux de succes des commandes).
- Gestion d'erreurs: en cas de commande non comprise, l'assistant propose 2 ou 3 intents proches.
- Contraintes d'exploitation: fonctionnement sur reseau local du campus et mode degrade disponible sans acces Internet.

Fonctionnalites MVP:
- Commandes vocales basiques
- Creation de taches/rappels
- Suggestion automatique de priorites
- Journal d'activite consultable
- Affichage d'etat sur ecran embarque
- Une action physique simple commandable par l'utilisateur

Extensions possibles:
- Synchronisation agenda (Google/Outlook)
- Mode hors ligne degrade
- Profil utilisateur personnalise

KPI de validation:
- Taux de reconnaissance correcte des intentions
- Temps moyen entre commande et action executee
- Taux d'erreurs non recuperees
- Consommation moyenne CPU/RAM du service local

Valeur pedagogique:
- NLP applique
- design d'interaction homme-machine
- integration electronique visible
- architecture event-driven

---

### Projet B - Mini vehicule autonome indoor
Objectif:
Concevoir un petit vehicule autonome capable de suivre un circuit interieur, detecter des obstacles et s'arreter en securite.

Utilisateurs cibles:
- Operateur de demonstration
- Evaluateur securite

Composants possibles:
- Chassis mobile + moteurs + controle moteur
- Capteurs ultrason/ToF + IMU + camera
- ESP32 ou Raspberry Pi selon niveau de complexite
- Module IA de perception (ligne, obstacle, segmentation simple)

Detail fonctionnel attendu:
- Parcours 1: lancement d'une mission sur circuit predefini, suivi des checkpoints et retour au point de depart.
- Parcours 2: detection d'obstacle, freinage, contournement si possible, sinon alerte et arret securise.
- Parcours 3: reprise manuelle via interface en cas de panne capteur.
- Journal mission: vitesse, position estimee, incidents, action corrective.
- Securite de fonctionnement: une boucle de securite embarquee doit prioriser l'arret d'urgence independamment du dashboard.

Fonctionnalites MVP:
- Deplacement autonome sur parcours defini
- Detection d'obstacles et evitement simple
- Telemetrie en temps reel sur dashboard
- Mode manuel de secours

Extensions possibles:
- Planification de trajectoire dynamique
- Detection d'etat batterie avec retour automatique
- Multi-vehicules sur un meme circuit

KPI de validation:
- Taux de tours complets sans intervention
- Nombre de collisions/contacts
- Latence de reaction obstacle
- Taux de fonctionnement en mode degrade (sans interface)

Valeur pedagogique:
- robotique mobile
- fusion capteurs
- contraintes temps reel

---

### Projet C - Geolocalisation indoor en temps reel
Objectif:
Creer un systeme de localisation indoor (balises + algorithme) pour suivre un objet mobile, potentiellement le vehicule du Projet B.

Utilisateurs cibles:
- Operateur de flotte indoor
- Equipe analyse des trajectoires

Composants possibles:
- Balises BLE/UWB/Wi-Fi selon budget
- Noeuds de mesure fixes
- Serveur de triangulation/filtrage
- Interface cartographique en temps reel

Detail fonctionnel attendu:
- Parcours 1: initialisation d'une zone, calibration des balises, verification de couverture.
- Parcours 2: suivi temps reel d'un objet avec affichage position, vitesse et trace.
- Parcours 3: export des traces pour analyse (CSV/JSON).
- API inter-projet: endpoint standard pour recuperer la position courante et l'historique recent.
- Souverainete des donnees: base locale obligatoire et retention des traces configurable.

Fonctionnalites MVP:
- Position estimee en direct
- Historique de trajectoire
- Affichage precision moyenne et latence
- API reutilisable par d'autres projets

Extensions possibles:
- Geofencing avec alertes automatiques
- Filtrage avance (Kalman/particle)
- Estimation orientation de l'objet

KPI de validation:
- Erreur moyenne de position (en metres)
- Taux de rafraichissement stable
- Disponibilite de l'API
- Capacite a continuer la localisation en cas de coupure reseau locale partielle

Valeur pedagogique:
- traitement du signal
- estimation de position (filtrage Kalman simplifie possible)
- interconnexion inter-projets

---

### Projet D - Serre low-tech intelligente
Objectif:
Developper une mini-serre instrumentee, intelligente et autonome, capable de maintenir une plante en vie sur un cycle reel de culture, tout en sollicitant l'utilisateur uniquement quand c'est necessaire.

Contexte d'usage:
Beaucoup d'utilisateurs oublient d'arroser, ne savent pas interpreter l'etat d'une plante, ou s'absentent plusieurs jours. La solution doit simplifier la vie du jardinier urbain, pas la complexifier.

Utilisateurs cibles:
- Gestionnaire de serre
- Enseignant pour audit de donnees

Contraintes specifiques (issues du brief serre):
- Souverainete des donnees: acquisition, base de donnees, backend et application heberges localement.
- Cycle reel: fonctionnement continu sur octobre -> fevrier, avec choix de variete justifie par faisabilite (luminosite, temperature).
- Continuite de service: les fonctions vitales (arrosage, ventilation) restent actives meme en cas de panne d'interface.
- Sobriete: suivi quantifie de l'eau, de l'energie et des materiaux engages.

Composants possibles:
- Capteurs humidite sol, temperature, humidite air, luminosite
- Actionneurs: pompe d'arrosage, ventilation, LED horticole
- ESP32 + backend de collecte
- Module IA de recommandation ou prediction simple

Detail fonctionnel attendu:
- Parcours 1: acquisition continue des mesures et visualisation en dashboard.
- Parcours 2: declenchement d'une recommandation explicable (ex: arroser dans 2h, cause: humidite sol faible).
- Parcours 3: pilotage manuel des actionneurs et comparaison avec mode auto.
- Journal agronomique: actions appliquees, evolution des mesures, effets observes.
- Application mobile locale: consultation et alertes sur smartphone connecte au meme Wi-Fi.
- UX orientee action: recommandations claires ("Arroser maintenant") plutot que donnees brutes non interpretees.

Architecture de surete recommandee:
- Niveau 1 (embarque prioritaire): regles vitales locales pour arroser/ventiler meme sans UI.
- Niveau 2 (supervision): API + application mobile + recommandations IA + historique.
- Strategie de secours: si l'IA est indisponible, retour a des seuils deterministes securises.

Criteres de succes du projet:
- Serre demandant peu d'entretien humain
- Autonomie sur les fonctions critiques (eau, climat)
- Recolte exploitable en fin de periode ou explication scientifique argumentee en cas d'echec
- Application smartphone locale operationnelle
- Conseils utiles et actionnables pour l'utilisateur

Fonctionnalites MVP:
- Tableau de bord des mesures
- Alertes (seuils critiques)
- Recommandations automatiques explicables
- Historique et tendances

Extensions possibles:
- Prediction a 24h des besoins en eau
- Scenarios saisonniers parametrables
- Detection d'anomalies capteurs

KPI de validation:
- Reduction des depassements de seuil
- Stabilite des conditions de culture
- Precision des recommandations par rapport aux decisions expertes
- Temps cumule de service en mode autonome sans intervention
- Rendement final (recolte ou analyse causale qualifiee en cas d'echec)

Valeur pedagogique:
- IoT complet capteur->backend->interface
- modelisation de donnees temporelles
- IA interpretable pour la prise de decision

Apprentissages vises:
- Ingenierie hardware + software dans un environnement reel contraint
- Architecture edge computing et hebergement local souverain
- Securite de fonctionnement et priorisation des fonctions vitales
- Eco-conception avec mesure de l'impact technique
- Post-mortem scientifique en cas d'echec biologique

---

### Projet E - Plateau de jeu robotise strategique
Objectif:
Concevoir un plateau de jeu physique capable de deplacer automatiquement des pieces selon les decisions d'une IA, avec perception visuelle de l'etat de la partie et action mecanique precise.

Utilisateurs cibles:
- Joueur humain
- Observateur pedagogique qui suit la logique de decision de l'IA

Composants possibles:
- Plateau motorise ou systeme cartesien XY
- Camera de dessus pour detection des pieces
- Mecanisme de prehension ou de poussée des pieces
- Moteur de regles + IA de strategie
- Interface de suivi de partie sur web ou tablette

Detail fonctionnel attendu:
- Parcours 1: l'IA observe le plateau, calcule son coup et deplace automatiquement sa piece.
- Parcours 2: le systeme detecte l'etat reel du plateau apres chaque action et verifie la coherence.
- Parcours 3: l'utilisateur peut consulter l'explication du choix de coup ou l'historique de la partie.
- Gestion incidents: si une piece est mal percue ou mal deplacee, le systeme se met en pause et demande confirmation.

Fonctionnalites MVP:
- Reconnaissance des pieces et de leur position
- Execution automatique de deplacements simples
- Historique des coups
- Mode pause/reprise avec validation humaine

Extensions possibles:
- Stratégie IA plus avancée
- Support de plusieurs jeux (echecs, dames, othello simplifie)
- Mode spectateur avec explication des coups

KPI de validation:
- Taux de reconnaissance correcte des pieces
- Taux de coups executés sans intervention
- Precision du placement mecanique

Valeur pedagogique:
- vision par ordinateur
- prise de decision par IA
- robotique de manipulation de precision

---

### Projet L - Casier intelligent de pret de materiel
Objectif:
Gerer un casier connecte permettant de prêter du materiel aux etudiants avec traçabilite, autorisation et suivi des retours.

Utilisateurs cibles:
- Responsable de laboratoire
- Etudiant emprunteur
- Technicien qui gere les etats de maintenance

Composants possibles:
- Serrures ou electrovannes de casiers
- Lecteur badge ou code personnel
- Backend de gestion d'inventaire local
- Application web d'administration et de reservation
- Module de preuve de depot/retrait (photo locale)

Detail fonctionnel attendu:
- Parcours 1: reserve un objet, le casier s'ouvre a l'heure autorisee.
- Parcours 2: retour du materiel avec verification du casier associe.
- Parcours 3: alerte si retard, materiel absent ou ouverture anormale.
- Parcours 4: checklist d'etat au retour (complet, endommage, batterie faible, accessoire manquant).
- Parcours 5: passage automatique en maintenance ou quarantaine si anomalie detectee.
- Parcours 6: tableau de fiabilite par type de materiel (taux de perte, pannes, retards).

Fonctionnalites MVP:
- Authentification usager
- Reserve/pret/retour
- Journal d'historique
- Etat des casiers en direct
- Gestion des etats materiel (OK, a verifier, indisponible)

Extensions possibles:
- Reservation par créneau
- Notification de retard
- Inventaire intelligent par categorie
- Score de fiabilite des emprunteurs
- Workflow de maintenance integre
- Rapport mensuel d'usage et de pertes

KPI de validation:
- Taux de retour a l'heure
- Disponibilite des casiers
- Traçabilite des objets pretes
- Taux d'objets retournes en bon etat
- Diminution des pertes et litiges

Valeur pedagogique:
- systeme d'information local
- securisation d'acces physique
- UX operationnelle pour un usage quotidien
- gestion d'actifs et maintenance

---

### Projet N - Jeu de flechettes avec reconnaissance par camera
Objectif:
Concevoir un systeme de jeu de flechettes digital qui detecte automatiquement la position des flechettes sur la cible par vision par ordinateur, gere les regles du jeu (301, Cricket, etc.) et affiche les scores en direct.

Utilisateurs cibles:
- Joueur en competition ou loisir
- Animateur/arbitre qui gere les parties
- Spectateur qui visualise les scores et l'historique

Composants possibles:
- 3 cameras RGB disposees autour de la cible (ou multi-vue calibree)
- Cible physique standard ou amelioree avec marqueurs visuels
- Eclairage optimise pour la detection de contraste
- Backend de traitement d'image et de reconnaissance de position
- Serveur d'API local pour la gestion des regles et des scores
- Interface web/tablette pour affichage des scores, gestion des joueurs et des modes de jeu
- Affichage ecran ou projection pour spectateurs

Detail fonctionnel attendu:
- Parcours 1: initialisation d'une partie (nombre de joueurs, choix du mode de jeu: 301, Cricket, etc.).
- Parcours 2: detecter automatiquement l'arrivee d'une nouvelle flechette et localiser sa position sur la cible.
- Parcours 3: calculer automatiquement les points selon la zone touchee et les regles du jeu en cours.
- Parcours 4: gerer la sequence des joueurs, afficher le joueur en cours et son tour.
- Parcours 5: affichage temps reel des scores cumulatifs et de l'etat de chaque joueur (reste a compter, deja out, etc.).
- Parcours 6: historique des coups et replay visuel des flechettes detaillees.
- Gestion incidents: si une flechette n'est pas detectee ou ambigue, demander confirmation manuelle au joueur/arbitre.
- Mode degrade: possibilite d'entrer les scores manuellement en cas de defaillance camera.

Fonctionnalites MVP:
- Detection et localisation des flechettes par camera
- Calcul automatique des points (zones cible: simple, double, triple, bullseye)
- Gestion de minimum 2 modes de jeu (301, Cricket)
- Interface de configuration de partie (nombre joueurs, choix mode)
- Affichage des scores temps reel avec joueur en cours
- Historique des 3 derniers coups par joueur
- Mode manuel de correction et de secours

Extensions possibles:
- Support de multiples modes de jeu (Around the world, Shanghai, etc.)
- Statistiques joueur (taux de precision par zone, historique)
- Classement multi-parties et ligue locale
- Notifications vocales des scores
- Reconnaissance des joueurs par visage ou badge
- Couplage avec projecteur pour affichage en direct
- Analyse IA des trajectoires et predictions

KPI de validation:
- Precision de detection des flechettes (>95% de precision)
- Latence entre arrivee de la flechette et affichage du score (<2 secondes)
- Taux d'erreurs non recuperees
- Disponibilite du systeme lors d'une partie complete
- Satisfaction des joueurs et arbitres

Valeur pedagogique:
- vision par ordinateur multi-camera
- traitement d'image et calibration
- gestion de regles complexes et etats de jeu
- interface utilisateur pour gestion de competition
- interaction homme-machine temps reel


## 9) Methode de choix et affectation des 5 groupes
Avec 7 idees disponibles (A a E, L, N), les etudiants disposent d'un vrai choix de sujet.

Processus recommande:
- Etape 1: chaque groupe soumet un Top 3 de projets (ordre de preference).
- Etape 2: arbitrage enseignant selon faisabilite technique et equilibre de charge.
- Etape 3: validation officielle des 5 sujets retenus (1 sujet par groupe).

Regles d'arbitrage suggerees:
- Priorite aux sujets couvrant bien le socle complet (embarque + backend + IA + interface).
- Eviter que plusieurs groupes prennent des sujets trop similaires.
- Garantir au moins 1 sujet orientee mobilite/robotique et 1 sujet orientee IoT environnement.

Classement recommande par difficulte et budget:

| Projet | Intitule | Difficulté | Budget materiel | Commentaire |
| --- | --- | --- | --- | --- |
| L | Casier intelligent de pret de materiel | Faible a moyenne | Faible a moyen | Solide pour gestion d'acces et traçabilite |
| A | Mini robot interactif de bureau | Moyenne | Moyen | Bon point d'entree pour embarque + UX |
| N | Jeu de flechettes avec reconnaissance camera | Moyenne a elevee | Moyen | Vision applicative, ludique, bon potentiel demo |
| C | Geolocalisation indoor en temps reel | Moyenne a elevee | Moyen a eleve | Sensible a la calibration et aux mesures |
| D | Serre low-tech intelligente | Elevee | Moyen a eleve | Excellent sujet, mais fort risque terrain |
| B | Mini vehicule autonome indoor | Elevee | Eleve | Tres visible, integration mecanique exigeante |
| E | Plateau de jeu robotise strategique | Elevee | Eleve | Tres attractif, mecanique de precision et perception |

Exemple de combinaison coherente sur 5 groupes:
- Groupe 1: Projet A (mini robot interactif)
- Groupe 2: Projet B (vehicule)
- Groupe 3: Projet C (geolocalisation)
- Groupe 4: Projet D (serre)
- Groupe 5: Projet E (plateau de jeu robotise)

Couplage inter-projets recommande:
- Projet B (vehicule) <-> Projet C (geolocalisation) via API commune.

## 10) Jalons proposes
- Jalon 1 (Semaine 4): fin de Periode 1 + Soutenance 1 (cadrage et faisabilite)
- Jalon 2 (Semaine 9): fin de Periode 2 + Soutenance 2 (MVP fonctionnel)
- Jalon 3 (Semaine 18): fin de Periode 3 + Soutenance 3 (integration IA + electronique et systeme stabilise)
- Jalon 4 (Final): Soutenance finale transverse (bilan, demo, perspectives)

## 11) Conclusion
Le cadre propose permet de conserver l'esprit initial (IA appliquee, concret, ludique) tout en ajoutant un niveau de detail suffisant pour piloter 5 groupes de maniere homogene et evaluable.

Le catalogue retenu (7 sujets) augmente le choix et facilite l'alignement entre interets des etudiants, budget materiel et niveau de difficulte.
