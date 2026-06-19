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
- Decoupage temporel: 4 periodes de 4 semaines (16 semaines au total)
- Evaluation orale: 1 soutenance a la fin de chaque periode + 1 soutenance finale (soit 5 soutenances)

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
- Electronique/embarque: microcontroleur (ESP32, STM32, Arduino) ou SBC (Raspberry Pi)
- Logiciel: API/backend (Python FastAPI, Node.js ou equivalent)
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

Cadence par periodes (4 x 4 semaines):
- Periode 1 (Semaines 1 a 4): cadrage, etat de l'art, architecture cible, preuve de faisabilite
- Periode 2 (Semaines 5 a 8): MVP logiciel + premier prototype electronique integre
- Periode 3 (Semaines 9 a 12): consolidation technique, module IA operationnel, integration systeme
- Periode 4 (Semaines 13 a 16): robustesse, tests en conditions reelles, finalisation des livrables

Soutenances:
- Soutenance 1: fin Periode 1 (revue de cadrage)
- Soutenance 2: fin Periode 2 (revue MVP)
- Soutenance 3: fin Periode 3 (revue d'integration)
- Soutenance 4: fin Periode 4 (pre-validation technique)
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

### Projet I - Jeu interactif de gestes et reflexes (Motion Arena)
Objectif:
Concevoir un jeu physique interactif ou les joueurs reproduisent des gestes, postures ou sequences motrices pour marquer des points en temps reel.

Utilisateurs cibles:
- Joueur (etudiant seul ou en duel)
- Animateur/enseignant qui parametre les niveaux

Composants possibles:
- Camera frontale
- Eclairage de poste
- Backend d'analyse de posture ou de sequence
- Ecran de score et de feedback visuel
- Signal lumineux/sonore pour rythmer les manches

Detail fonctionnel attendu:
- Parcours 1: le jeu affiche une consigne de geste a reproduire dans un temps limite.
- Parcours 2: le systeme valide le geste et attribue des points, bonus de vitesse et combo.
- Parcours 3: mode duel ou tournoi avec classement local.
- Parcours 4: mode entrainement avec conseils personnalises sur les erreurs recurrentes.

Fonctionnalites MVP:
- Capture video simple ou image fixe
- Classification de posture ou de geste
- Feedback visuel ou sonore
- Score en direct et classement local

Extensions possibles:
- Analyse de sequence complete
- Personnalisation des niveaux de jeu
- Mode cooperatif equipe contre chrono
- Defis hebdomadaires et progression joueur

KPI de validation:
- Precision de classification des gestes
- Temps de retour de feedback
- Satisfaction des joueurs et taux de rejouabilite

Valeur pedagogique:
- vision par ordinateur
- apprentissage supervise
- gamification de l'apprentissage

---

### Projet K - Challenge moteur: course, boost et efficacite
Objectif:
Concevoir un mini challenge competitif ou les equipes reglent un moteur pour relever des epreuves (vitesse, endurance, precision) avec un score final melant performance et efficacite.

Utilisateurs cibles:
- Equipes etudiantes en mode challenge
- Jury/animateur qui arbitre les manches

Composants possibles:
- Moteur electrique miniature avec charge variable
- Capteurs courant, tension, vitesse, temperature
- Controleur embarque et backend d'analyse
- Tableau de score temps reel

Detail fonctionnel attendu:
- Parcours 1: chaque equipe prepare un reglage pour une manche donnee (sprint, endurance, precision).
- Parcours 2: execution de la manche avec affichage du score en direct.
- Parcours 3: calcul du score final incluant performance, stabilite et sobriete energetique.
- Gestion incidents: si la temperature ou le courant depasse un seuil, penalite automatique et mode protection.

Fonctionnalites MVP:
- Visualisation des mesures clefs
- Enregistrement des profils d'equipe
- Calcul automatique du score
- Arret de securite sur depassement de seuil

Extensions possibles:
- IA coach pour suggerer des reglages
- Classement multi-manches
- Mode ligue inter-groupes

KPI de validation:
- Equilibre performance/consommation atteint
- Stabilite du moteur pendant les manches
- Lisibilite et acceptation des regles de score

Valeur pedagogique:
- optimisation sous contrainte
- instrumentation embarquee
- apprentissage par competition

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

### Projet M - Atelier d'assemblage assiste par vision et guidage lumineux
Objectif:
Concevoir un mini poste d'assemblage qui construit des modeles ludiques (personnages type briques et mini droide type R2D2 simplifie), en guidant l'utilisateur ou un bras simple piece par piece.

Utilisateurs cibles:
- Etudiant en phase d'assemblage
- Tuteur qui suit la qualite du processus

Composants possibles:
- Camera de poste
- Eclairage ou guidage lumineux par zones
- Bras robotique simple ou systeme de guidage mecanique
- Base de donnees de recettes de montage
- Interface web de suivi du poste

Detail fonctionnel attendu:
- Parcours 1: selection d'un modele a construire (personnage simplifie ou mini droide simplifie).
- Parcours 2: le systeme reconnait l'etape courante et indique la piece suivante.
- Parcours 3: si une mauvaise piece est detectee, il emet une alerte visuelle et sonore.
- Parcours 4: suivi du temps d'assemblage et des erreurs par sequence.
- Gestion incidents: si la camera perd le poste, le systeme se met en mode assistance manuelle.

Fonctionnalites MVP:
- Reconnaissance d'etapes de montage
- Assistance visuelle au poste
- Journal des erreurs d'assemblage
- Interface de suivi des temps
- Deux recettes completes minimum (personnage simplifie + mini droide simplifie)

Extensions possibles:
- Recommandation du meilleur ordre d'assemblage
- Detection automatique d'omissions
- Score de qualite du montage
- Mode chrono et classement entre equipes
- Bibliotheque de modeles ludiques supplementaires

KPI de validation:
- Reduction des erreurs d'assemblage
- Temps de completion d'une sequence
- Qualite de guidage percue par l'utilisateur
- Taux de modeles finalises sans reprise manuelle

Valeur pedagogique:
- vision appliquee
- aide a l'assemblage industriel
- interaction homme-machine contextualisee
- gamification de l'assemblage

## 9) Methode de choix et affectation des 5 groupes
Avec 9 idees disponibles (A a E, I, K, L, M), les etudiants disposent d'un vrai choix de sujet.

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
| I | Jeu interactif de gestes et reflexes (Motion Arena) | Moyenne | Moyen | Ludique, rejouable, ideal demo publique |
| A | Mini robot interactif de bureau | Moyenne | Moyen | Bon point d'entree pour embarque + UX |
| C | Geolocalisation indoor en temps reel | Moyenne a elevee | Moyen a eleve | Sensible a la calibration et aux mesures |
| K | Challenge moteur: course, boost et efficacite | Moyenne a elevee | Moyen | Performance + strategie + sobriete |
| D | Serre low-tech intelligente | Elevee | Moyen a eleve | Excellent sujet, mais fort risque terrain |
| B | Mini vehicule autonome indoor | Elevee | Eleve | Tres visible, integration mecanique exigeante |
| E | Plateau de jeu robotise strategique | Elevee | Eleve | Tres attractif, mecanique de precision et perception |
| M | Atelier d'assemblage ludique (personnages et mini droide) | Elevee | Eleve | Tres attractif pour demos et competitions |

Exemple de combinaison coherente sur 5 groupes:
- Groupe 1: Projet A (mini robot interactif)
- Groupe 2: Projet B (vehicule)
- Groupe 3: Projet C (geolocalisation)
- Groupe 4: Projet D (serre)
- Groupe 5: Projet M (assemblage ludique)

Couplage inter-projets recommande:
- Projet B (vehicule) <-> Projet C (geolocalisation) via API commune.

## 10) Risques principaux et plans de mitigation
- Risque: complexite materielle trop elevee
	Action: valider un MVP materiel avant la semaine 4
- Risque: module IA trop ambitieux
	Action: prevoir une version baseline non-IA
- Risque: integration tardive
	Action: imposer une demo d'integration intermediaire
- Risque: disparite de niveau entre groupes
	Action: definir un socle obligatoire et des options bonus

## 11) Jalons proposes
- Jalon 1 (Semaine 4): fin de Periode 1 + Soutenance 1 (cadrage et faisabilite)
- Jalon 2 (Semaine 8): fin de Periode 2 + Soutenance 2 (MVP fonctionnel)
- Jalon 3 (Semaine 12): fin de Periode 3 + Soutenance 3 (integration IA + electronique)
- Jalon 4 (Semaine 16): fin de Periode 4 + Soutenance 4 (systeme stabilise)
- Jalon 5 (Final): Soutenance finale transverse (bilan, demo, perspectives)

## 12) Conclusion
Le cadre propose permet de conserver l'esprit initial (IA appliquee, concret, ludique) tout en ajoutant un niveau de detail suffisant pour piloter 5 groupes de maniere homogene et evaluable.

Le catalogue retenu (9 sujets) augmente le choix et facilite l'alignement entre interets des etudiants, budget materiel et niveau de difficulte.
