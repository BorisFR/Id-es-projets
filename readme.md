# Idées de projets de fin d'études

## 1) Contexte et objectif général
Ce document propose des sujets de projets pour des étudiants de dernière année en école d'ingénieur numérique.

Orientation pédagogique souhaitée :
- IA appliquée
- approche concrète et ludique
- intégration conjointe de développement logiciel et d'électronique

## 2) Contraintes de départ
- Charge projet : 180h par étudiant
- Effectif : 25 étudiants
- Organisation : 5 groupes de 5 étudiants
- Volume horaire cible par groupe : environ 900h
- Découpage temporel : 4 périodes (4, 5, 7 et 3 semaines, soit 19 semaines projet au total)
- Pauses projet : 4 semaines entre Période 1 et Période 2, puis 4 semaines entre Période 2 et Période 3 ; aucune pause entre Période 3 et Période 4
- Évaluation orale : 1 soutenance à la fin de chaque période ; la soutenance de fin de Période 4 constitue la soutenance finale (soit 4 soutenances)

## 3) Analyse rapide du besoin
Les idées initiales sont pertinentes car elles couvrent déjà :
- un usage visible et motivant (assistant, véhicule, serre)
- des dimensions IA appliquée (vision, NLP, prédiction, optimisation)
- des interfaces concrètes avec le monde physique (capteurs, actionneurs, embarqué)

Points à compléter pour un cadrage pédagogique robuste :
- définir des livrables clairs par projet
- imposer une architecture minimale (embarqué + backend + interface)
- prévoir un plan de tests et une validation terrain
- harmoniser la difficulté entre groupes
- fixer des critères d'évaluation communs

## 4) Socle technique recommandé (commun à tous les groupes)
Chaque projet devrait inclure au minimum :
- Électronique/embarqué : microcontrôleur (ESP32, Raspberry Pi Pico) ou SBC (Raspberry Pi)
- Logiciel : API/backend en .NET 10 (ASP.NET Core) avec interface Blazor
- Interface : application web ou mobile
- IA : au moins un module exploitable en démonstration (classification, détection, recommandation, prédiction)
- DevOps : gestion de version, CI (intégration continue) simple, documentation de déploiement
- Gestion de code source : utilisation de GitHub uniquement (pas GitLab, Bitbucket ou autre plateforme)
- Conteneurisation : non autorisée (Docker, Podman, Kubernetes, etc.)
- Hébergement : déploiement backend/site web possible sur VPS OVH type VPS-1 si nécessaire
- Wi-Fi (si nécessaire) : utiliser le SSID `JUNIA_LAB`
- Configuration réseau : prévoir un processus de provisioning (script, assistant de première configuration) ou un portail captif via point d'accès Wi-Fi
- Sécurité de configuration : ne jamais fixer en dur (hardcode) les paramètres Wi-Fi dans le code source

Principes transverses inspirés du projet serre (à appliquer à tous les sujets) :
- Approche local-first : chaîne logicielle hébergée en local (acquisition, stockage, backend, interface), sans dépendance cloud obligatoire.
- Continuité de service : le système doit conserver ses fonctions critiques même si l'interface tombe ou si le réseau est indisponible.
- Sobriété mesurée : chaque groupe suit et justifie les ressources consommées (énergie, eau, matériaux, temps machine).
- UX utile : les interfaces privilégient des actions claires plutôt que des tableaux de bord complexes.
- Droit au post-mortem : en cas d'échec terrain, le groupe doit produire une analyse technique argumentée basée sur les données.

## 5) Organisation du travail (180h par étudiant)
Proposition de découpage :
- Cadrage et état de l'art : 20h
- Conception système (architecture, choix matériel, schéma de données) : 25h
- Développement v1 (MVP) : 60h
- Intégration électronique + IA : 40h
- Tests, robustesse, optimisation : 20h
- Documentation, soutenance, démo finale : 15h

Cadence par périodes :
- Période 1 (4 semaines) : cadrage, état de l'art, architecture cible, preuve de faisabilité
- Pause projet (4 semaines)
- Période 2 (5 semaines) : MVP logiciel + premier prototype électronique intégré + consolidation technique
- Pause projet (4 semaines)
- Période 3 (7 semaines) : module IA opérationnel, intégration système, robustesse, tests en conditions réelles
- Période 4 (3 semaines) : finalisation des livrables, répétition générale, préparation et exécution de la soutenance finale

Soutenances :
- Soutenance 1 : fin Période 1 (revue de cadrage)
- Soutenance 2 : fin Période 2 (revue MVP)
- Soutenance 3 : fin Période 3 (revue d'intégration et validation technique)
- Soutenance 4 (finale) : fin Période 4, présentation finale complète (résultats, démo, retour critique)

## 6) Livrables attendus
Pour chaque groupe :
- Cahier des besoins et cas d'usage
- Dossier architecture (matériel + logiciel)
- Dépôt code versionné propre
- Prototype fonctionnel démontrable
- Rapport technique (résultats, limites, pistes d'amélioration)
- Présentation finale avec démonstration en conditions réelles

### Trame obligatoire du cahier des charges (fonctionnel)
Chaque groupe doit produire un cahier des charges avec, au minimum, les rubriques suivantes :
- Contexte et problème cible : qui est l'utilisateur, quel besoin concret est résolu.
- Périmètre : ce qui est inclus, ce qui est explicitement hors périmètre.
- Parties prenantes : utilisateur final, exploitant, mainteneur, évaluateur.
- Parcours utilisateur cibles : 3 à 5 scénarios nominaux + 2 scénarios d'erreur.
- Exigences fonctionnelles (EF) : liste numérotée EF-01, EF-02, ... testables.
- Exigences non fonctionnelles (ENF) : latence, disponibilité, sécurité, local-first, sobriété.
- Contraintes matérielles : capteurs/actionneurs imposés ou optionnels, budget cible, encombrement.
- Données et traçabilité : quelles données sont stockées, durée de rétention, format d'export.
- Stratégie de validation : tests unitaires, tests intégration, tests terrain, critères d'acceptation.
- Gestion des risques : top 5 risques + plan de mitigation.

### Format recommandé des exigences
- EF-xx (fonctionnelle) : "Le système doit ..." + mesure de succès + méthode de test.
- ENF-xx (non fonctionnelle) : "Le système doit ..." + seuil chiffré.

Exemples :
- EF-03 : Le système doit détecter un événement critique et notifier l'utilisateur en moins de 3 secondes.
- ENF-02 : Le système doit continuer ses fonctions vitales pendant au moins 30 minutes sans interface graphique.
- ENF-05 : Le système doit fonctionner sans dépendance cloud obligatoire sur le réseau local.

### Glossaire des acronymes (utilisés dans ce document)
- EF : Exigence Fonctionnelle.
- ENF : Exigence Non Fonctionnelle.
- KPI : Key Performance Indicator (indicateur clé de performance).
- UX : User eXperience (expérience utilisateur).
- MVP : Minimum Viable Product (produit minimum viable).
- CI : Continuous Integration (intégration continue).
- API : Application Programming Interface (interface de programmation applicative).
- NLP : Natural Language Processing (traitement automatique du langage naturel).
- IoT : Internet of Things (Internet des objets).
- JSON : JavaScript Object Notation (format texte d'échange de données).
- CSV : Comma-Separated Values (format tabulaire texte séparé par des virgules).
- QR : Quick Response (code 2D à lecture rapide).
- RSSI : Received Signal Strength Indicator (indicateur de puissance de signal reçue).
- UWB : Ultra-Wideband (ultra large bande).

### Définition de terminé (Definition of Done, obligatoire)
Un projet est considéré valide uniquement si :
- le MVP est démontrable en conditions réelles,
- les exigences EF/ENF critiques sont vérifiées par des tests tracés,
- les modes de panne et le mode dégradé sont démontrés,
- un post-mortem technique est fourni en cas d'échec partiel.

### Livrables attendus à chaque soutenance
- Soutenance 1 (Semaine 4) : problème cible, EF/ENF v1, architecture v1, preuve de faisabilité.
- Soutenance 2 (fin Période 2) : MVP intégré (logiciel + électronique), tests de base, premier retour utilisateur.
- Soutenance 3 (fin Période 3) : système consolidé, IA exploitable, tests d'intégration et robustesse.
- Soutenance 4 (fin Période 4, finale) : validation terrain, corrections, bilan global, démo complète, mesures KPI, limites et feuille de route.

## 7) Grille d'évaluation (exemple)
- Qualité de la solution technique : 30%
- Intégration électronique + logiciel : 20%
- Pertinence et maîtrise du module IA : 20%
- Qualité logicielle (tests, propreté, documentation) : 15%
- Gestion de projet et travail d'équipe : 10%
- Qualité de la démonstration finale : 5%

Suggestion de répartition des notes par soutenance :
- Soutenance 1 : 10%
- Soutenance 2 : 15%
- Soutenance 3 : 20%
- Soutenance 4 : 20%
- Soutenance finale : 35%

## 8) Idées de projets détaillées

### Projet A - Mini robot interactif de bureau
Objectif :
Construire un mini robot interactif de bureau capable de capter des demandes vocales, d'afficher des informations sur son écran et d'agir physiquement de manière simple.

Utilisateurs cibles :
- Étudiant utilisateur final
- Tuteur qui consulte la progression des tâches

Composants possibles :
- **Structure mécanique** : base mobile compacte (dimensions : 20-30cm) avec châssis stable, ou configuration de bureau fixe avec tête mobile articulée
- **Système de mobilité** : deux moteurs pas-à-pas 28BYJ ou moteurs CC avec réducteur, résistant à 10+ heures d'utilisation quotidienne
- **Interfaces de saisie** : microphone directif intégré (MÓ5 ou équivalent) + 3-4 boutons physiques silencieux + capteur tactile de présence (PIR ou capacitif)
- **Système d'affichage** : écran tactile 3-4" (480x320px minimum, IPS de préférence) ou e-ink pour sobriété énergétique
- **Audio** : haut-parleur 2W minimum + amplificateur audio intégré, capables de synthétiser la parole clairement
- **Calcul embarqué** : Raspberry Pi 4 (4GB RAM) ou Pi Pico RP2040 + co-processeur SBC limité
- **Connectivité** : Wi-Fi 802.11ac pour backend en réseau local, Bluetooth 5.0 optionnel pour mobile
- **Alimentation** : batterie Li-Po 5000mAh (min 8h autonomie) + charge rapide USB-C, mode hibernation programmable
- **Actionneurs simples** : servo moteur 180° pour orientation tête, vérin pour action palpable (ascenseur de carte, préhension lumière)

Détail fonctionnel attendu :
- **Parcours 1 - Enregistrement vocal** : l'utilisateur parle au robot, qui capture l'audio, l'envoie au backend NLP local, remet en forme la commande reconnue, l'affiche à l'écran en couleur et demande confirmation vocale ("Vous avez demandé ... c'est correct?"). Latence cible : <2s
- **Parcours 2 - Tâches et rappels** : le robot affiche un récapitulatif des 3 prochaines tâches sur l'écran avec leur priorité codée par couleur. L'utilisateur peut valider ou repousser l'ordre via les boutons. Les actions et e-mails sont synchronisés au backend
- **Parcours 3 - Confirmation tangible** : quand une tâche est validée, le robot tourne sa tête à 90°, émet un signal sonore spécifique et lumineux, puis revient à la position initiale. Cela rend l'IA tangible et interactive
- **Parcours 4 - Tuteur observateur** : l'interface web (localhost:8080) affiche en direct l'historique des 20 derniers déverrouillages vocaux : texte reconnu, intention détectée, action exécutée, timestamp. Filtre par date ou type d'intention
- **Gestion d'erreurs** : si la reconnaissance vocale ne capture rien ou décide avec faible confiance (<60%), le robot propose 2-3 commandes similaires dont l'utilisateur peut choisir. Si toujours incertain, passage en manuel (boutons)
- **Mode dégradé** : fonctionnement complet sur réseau local sans Internet. Si NLP central indisponible, basculement automatique sur modèle léger embarqué (reconnaissance pattern simple)
- **Alimentation et veille** : en absence de parole pendant 10min, écran en veille de 30%, moteurs désactivés. Un appui sur le bouton physique réveille le système

Fonctionnalités MVP :
- Commandes vocales basiques (reconnaissance d'intents : 5-10 commandes majeures)
- Création de tâches/rappels avec priorité (API REST)
- Suggestion automatique de priorités basée sur historique
- Journal d'activité consultable en temps réel
- Affichage d'état sur écran embarqué
- Une action physique simple commandable par l'utilisateur (servo ou vérin)
- Authentification utilisateur simple (badge ou code 4 chiffres)

Extensions possibles :
- Synchronisation agenda (Google Calendar en API locale)
- Mode hors ligne dégradé avec persistance locale
- Profil utilisateur personnalisé avec reconnaissance vocale du locuteur
- Apprentissage des préférences temps de traitement
- Intégration avec systèmes domotiques (allumage lumières)
- Support multilingue (basique)

KPI de validation :
- Taux de reconnaissance correcte des intentions (>80% cible)
- Temps moyen entre commande et action exécutée (<3s)
- Taux d'erreurs non récupérées (<5%)
- Consommation moyenne CPU/RAM du service local (<20% CPU, <300MB RAM)
- Disponibilité du système en mode dégradé (>98%)
- Satisfaction utilisateur (score de facilité d'usage >7/10)

Valeur pédagogique :
- NLP appliquée (tokenisation, classification d'intentions)
- Design d'interaction homme-machine et feedback utilisateur
- Intégration électronique visible et tangible
- Architecture pilotée par événements avec message broker local (RabbitMQ ou Redis)
- Gestion état d'une application multi-composants
- Circuit breaker et résilience locale pour robustesse

---

### Projet B - Mini véhicule autonome indoor
Objectif :
Concevoir un petit véhicule autonome capable de suivre un circuit intérieur, détecter des obstacles et s'arrêter en sécurité.

Utilisateurs cibles :
- Opérateur de démonstration
- Évaluateur sécurité

Composants possibles :
- **Châssis** : plateforme robotique 20-30cm (DFRobot, SCUTTLE ou compatible), 500g max, roues tout-terrain
- **Moteurs** : deux moteurs DC 12V 100RPM avec encodeurs optiques (retour de position) + contrôles H-bridge L298N
- **Batterie** : Li-Po 7.4V (2S) 5000mAh minimum, chargeur USB-C intégré
- **Capteurs de perception**:
  - **Lidar** : YDLIDAR X4 (360°, 10m, peu coûteux) OU 5-6 capteurs ultrason (HC-SR04) pointés en éventail
  - **Encodeurs** : 2x encodeurs optiques sur les moteurs (résolution 20+ coups/tour)
  - **IMU** : capteur 9-DOF (accélero, gyro, magnéto : MPU6050 ou BNO055)
  - **Caméra** : webcam USB optionnelle pour détection de ligne au sol
- **Microcontrôleur** : Raspberry Pi 4 (4GB) avec GPIO PWM pour moteurs OU ESP32 pour architecture légère
- **Communication** : Wi-Fi pour tableau de bord temps réel + fréquence radio 433MHz pour arrêt d'urgence
- **Système de sécurité** : bouton d'arrêt d'urgence mécanique, circuit de sécurité embarquée indépendante (Arduino nano redondant)

Détail fonctionnel attendu :
- **Parcours 1 - Mission autonome** : l'opérateur définit un circuit via interface web (4-6 points de passage indoor + hauteur). Le véhicule se localise à l'initialisation avec calibrage, exécute la mission en boucle avec suivi de position estimée, puis revient au point de départ avec précision <50cm
- **Parcours 2 - Détection obstacle** : capteurs continuellement actifs, fusion Lidar OU ultrason pour résolution 30cm. Si obstacle détecté à <1m, freinage d'urgence en <100ms, pause 1s. Tentative de contournement simple (décalage latéral de 30cm). Si le contournement échoue 2 fois, signalement par LED rouge + appel radio d'urgence + alerte web
- **Parcours 3 - Mode manuel** : interface web avec joystick virtuel, l'opérateur reprend contrôle avec latence <500ms. Affichage télémétrie en temps réel : position estimée, vitesse, batterie, distance obstacle
- **Journal mission** : chaque sortie enregistrée localement (JSON) : timestamp, vitesse moyenne, distance parcourue, obstacles rencontrés, actions correctives, batterie à la fin. Export en CSV pour analyse post-mission
- **Sécurité de fonctionnement** : boucle d'arrêt embarquée indépendante qui coupe immédiatement les moteurs si : signal radio perdu >2s, tension batterie <10%, collision détectée. Cette boucle s'exécute à 50Hz sur microcontrôleur dédié
- **Calibrage terrain** : à chaque démarrage, véhicule effectue une ronde d'exploration pour mapper l'environnement (durée : <3min), stocke la carte en RAM

Fonctionnalités MVP :
- Déplacement autonome sur parcours prédéfini (3-4 waypoints)
- Détection d'obstacles et arrêt d'urgence
- Télémétrie en temps réel sur tableau de bord
- Mode manuel de secours avec joystick web
- Journalisation mission avec export CSV
- Système d'arrêt d'urgence déterministe embarqué

Extensions possibles :
- Planification de trajectoire dynamique avec A* (obstacle avoidance en t.r.)
- Prédiction de batterie avec retour automatique de "rentre charger"
- Multi-véhicules synchronisés sur un même circuit (anti-collision inter-véhicules)
- SLAM simplifié (localisation relative)
- Suivi de lignes au sol avec caméra pour précision

KPI de validation :
- Taux de tours complets sans intervention (>80% des missions réussies)
- Nombre de collisions/contacts (<2 par 10 missions)
- Latence de réaction obstacle (<150ms)
- Taux de fonctionnement en mode dégradé sans interface (>95%)
- Précision position finale vs point de départ (<1m)
- Disponibilité radio d'arrêt d'urgence (>99%)

Valeur pédagogique :
- Robotique mobile et cinématique (différentiel, odométrie)
- Fusion capteurs (filtre de Kalman simplifié pour la position)
- Contraintes temps réel et boucles de contrôle
- Sécurité de fonctionnement (conception fail-safe)
- Architecture distribuée (contrôle embarqué + supervision locale)

---

### Projet C - Géolocalisation indoor en temps réel
Objectif :
Créer un système de localisation indoor (balises + algorithme) pour suivre un objet mobile, potentiellement le véhicule du Projet B.

Utilisateurs cibles :
- Opérateur de flotte indoor
- Équipe analyse des trajectoires

Composants possibles :
- **Infrastructure de localisation** :
  - **Option 1 : BLE Beacons** : 4-6 balises iBeacon TX @ -4dBm, fixées aux coins de la zone (10m x 15m idéal), calibrage de distance de référence
  - **Option 2 : UWB (Ultra-Wideband)** : Qorvo ou Decawave (plus précis à 10-15cm mais coûteux)
  - **Option 3 : Wi-Fi triangulation** : utiliser les RSSI des APs campus + théorie d'atténuation
- **Nœuds de mesure** : récepteurs ESP32 avec BLE ou UWB dispersés stratégiquement, reliés en réseau local
- **Serveur de triangulation** : backend .NET 10 ASP.NET Core exposant algorithme Trilatération ou Kalman simplifié. API REST : POST /locate avec balises signalées, GET /history/{objet_id}
- **Interface cartographique** : SVG interactif avec plan du bâtiment, point position temps réel, trace historique dernier 1h coloriée par vitesse
- **Base de données locale** : PostgreSQL ou SQLite pour historique avec index sur (timestamp, objet_id). Rétention configurable (défaut : 1 semaine)
- **Communication** : Li-Fi ou 802.11ac pour bande passante temps réel, avec repli sur 802.11b si surcharge

Détail fonctionnel attendu :
- **Parcours 1 - Initialisation zone** : admin web enregistre zone physique (dimensions, obstacles statiques), place 4-6 balises virtuelles dans plan. Système effectue calibrage de référence : parcours complet de la zone avec un objet de référence connu, enregistre RSSI par balise par position (grille 1m). Durée : 15-20min, résultats sauvegardés localement
- **Parcours 2 - Suivi temps réel** : objet mobile (véhicule, personne avec beacon) transmet un signal périodiquement (toutes les 500ms). Noeuds récepteurs envoient au serveur leur signal + timestamp. Serveur applique la trilatération, estime la position et met à jour la carte. Latence cible : <1s du signal à l'affichage. Affichage : position en cercle, vecteur vitesse, rayon de précision (cercle d'incertitude) en couleur (vert si <30cm, orange si <50cm, rouge si >50cm)
- **Parcours 3 - Export traces** : bouton "Export mission" charge la dernière heure d'historique, génère JSON + CSV avec colonnes : timestamp, X, Y, vitesse, objets proches, incidents. Fichier stocké localement
- **API inter-projet** : point d'accès /locate/latest/{objet_id} retournant {x, y, precision, updated_at} en JSON. Le Projet B peut appeler cette API pour synchroniser sa carte interne. Latence max : 100ms
- **Souveraineté des données** : aucun cloud. Base PostgreSQL locale obligatoire, chiffrée au repos (PgCrypto). Rétention configurable par admin (par défaut 7 jours, purge auto). Droit à l'oubli : suppression manuelle ou par expiration
- **Continuité réseau** : si le réseau central est indisponible >30s, chaque nœud bascule sur cache local + synchronisation différentielle une fois le réseau rétabli

Fonctionnalités MVP :
- Position estimée en direct (à >80% de confiance)
- Historique de trajectoire avec affichage graphique
- Affichage précision moyenne et latence système
- API réutilisable par d'autres projets
- Interface admin pour calibrage de zone
- Export données en CSV

Extensions possibles :
- Géofencing avec alertes automatiques (ex: véhicule sort de la zone -> SMS/Slack)
- Filtrage avancé Kalman (convergence rapide)
- Estimation orientation de l'objet (si 2+ capteurs par objet)
- Comparaison de précision BLE vs Wi-Fi vs UWB (tableau de bord comparatif)
- Détection anomalies (saut position anormal -> perte capteur)

KPI de validation :
- Erreur moyenne de position (cible : <1m en 95% des cas)
- Taux de rafraîchissement stable (constance <10% jitter)
- Disponibilité de l'API (>99%)
- Capacité à continuer la localisation en cas de coupure réseau partielle (1-2 noeuds hors ligne : persistance <20 s)
- Latence E2E signal à affichage (<1.5s)
- Consommation batterie balise mobile (<48h sur 500mAh coin cell)

Valeur pédagogique :
- Traitement du signal (RSSI, filtrage bruit)
- Estimation de position (Trilatération, Kalman)
- Interconnexion inter-projets et API standards
- Architecture distribuée capteurs + serveur
- Persistance locale et continue de service
- Calibrage de systèmes physiques

---

### Projet D - Serre low-tech intelligente
Objectif :
Développer une mini-serre instrumentée, intelligente et autonome, capable de maintenir une plante en vie sur un cycle réel de culture, tout en sollicitant l'utilisateur uniquement quand c'est nécessaire.

Contexte d'usage :
Beaucoup d'utilisateurs oublient d'arroser, ne savent pas interpréter l'état d'une plante, ou s'absentent plusieurs jours. La solution doit simplifier la vie du jardinier urbain, pas la complexifier.

Utilisateurs cibles :
- Gestionnaire de serre
- Enseignant pour audit de données

Contraintes spécifiques (issues du brief serre) :
- Souveraineté des données : acquisition, base de données, backend et application hébergés localement.
- Cycle réel : fonctionnement continu sur octobre -> février, avec choix de variété justifié par faisabilité (luminosité, température).
- Continuité de service : les fonctions vitales (arrosage, ventilation) restent actives même en cas de panne d'interface.
- Sobriété : suivi quantifié de l'eau, de l'énergie et des matériaux engagés.

Composants possibles :
- **Capteurs environnement** :
  - Capteur humidité sol : sonde capacitive double (DFRobot SEN0193 ou équivalent) avec deux points de mesure (haut/bas)
  - Capteur température/humidité air : DHT22 ou BME280 (baromètre bonus)
  - Capteur luminosité : LUX BH1750 (0-65536 lux)
  - Capteur débit d'eau : compteur turbine YF-S201 pour arrosage
  - Voltmètre batterie (ADC intégré)
- **Actionneurs** :
  - Pompe arrosage : 12V 1000mL/min avec tête spray ajustable
  - Ventilateur axial : 5V 50mm pour circulation air
  - LED horticole optionnelle : strip 18W LED rouges+bleues (ratio 3:1)
  - Solénoïde de drain (optionnel)
- **Électronique** : carte ESP32 de développement avec shield relais (4 canaux) + carte d'acquisition analogique
- **Stockage eau** : réservoir PVC transparent 10L avec flotteur magnétique (low battery alert)
- **Alimentation** : batterie Li-Po 5000mAh (min 5 jours autonomie) + panneau solaire 20W en option
- **Communication** : Wi-Fi 802.11ac + RTC embarqué (DS3231) pour la persistance de la date
- **Base locale** : SQLite ou TimescaleDB (Postgres léger) pour séries temporelles

Détail fonctionnel attendu :
- **Parcours 1 - Acquisition continue** : chaque capteur est lu toutes les 5min, données envoyées au backend local, stockées avec timestamp. Le tableau de bord affiche des courbes temps réel sur 24h glissantes : temp, humidité sol, humidité air, luminosité. Moyennes horaires calculées et archivées
- **Parcours 2 - Recommandations explicables** : modèle de décision local (arbres de décision ou moteur de règles simple) évaluant l'état de la serre vs contraintes plante. Ex. :
  - SI humidité_sol < 30% ALORS "Arroser maintenant (raison : sol sec depuis 2h, événements : aucun)"
  - SI temp > 28°C ET humidité < 40% ALORS "Ventiler immédiatement (raison : climat trop chaud et sec)"
  - SI soleil < 2h AUJOURD'HUI ET LED disponible ALORS "Lumière insuffisante, allumer LED 4h ce soir?"
  - Chaque action est justifiée par critères mesurables
- **Parcours 3 - Pilotage manuel** : l'utilisateur peut forcer l'arrosage, la ventilation ou les LED depuis l'application mobile (locale). Pendant 5s après action manuelle, l'IA se met en pause. Résultats immédiatement visibles sur capteurs (pour confirmer que l'action a fonctionné)
- **Parcours 4 - Journal agronomique** : chaque action (arrosage, ventilation, LED) est journalisée avec raison, durée, volume d'eau consommé, énergie utilisée. L'interface affiche une chronologie : "09:30 - Arrosage (30s, 150mL eau) - Raison : humidité sol en baisse"
- **Parcours 5 - Application smartphone locale** : accessible sur réseau local via QR-code (http://serre.local:8000). Interface minimale : état serre (feu tricolore), recommandation en gros texte, historique 3 dernières actions. Pas de notifications push (sobriété), consultation manuelle
- **Parcours 6 - UX d'action** : recommandations formatées comme des questions simples :
  - "Arroser maintenant? (oui/non)"
  - "Ventiler? (non/rapide/long)"
  - "LED ce soir? (non/4h/8h)"
  - Pas d'affichage de valeurs brutes à l'utilisateur non-technicien
- **Mode autonome** : en absence d'interface pendant 24h, serre continue fonctionnement sur règles déterministes locales (seuils fixes sauvegardés)

Architecture de sûreté recommandée :
- **Niveau 1 (embarqué prioritaire)** : règles vitales locales exécutées à 50Hz sur ESP32 (timer d'interruption) : 
  - SI humidité_sol < 15% ALORS pompe=ON pendant max 30s (sauvegarde plante)
  - SI temp > 35°C ALORS ventilo=ON continu (prévention coup de chaleur)
- **Niveau 2 (supervision)** : si backend indisponible, ces règles continuent à fonctionner
- **Stratégie de secours** : si IA indisponible, retour à seuils déterministes sécurisés (conservateurs)

Critères de succès du projet :
- Serre demandant peu d'entretien humain
- Autonomie sur les fonctions critiques (eau, climat)
- Récolte exploitable en fin de période OU explication scientifique argumentée en cas d'échec
- Application smartphone locale opérationnelle
- Conseils utiles et actionnables pour l'utilisateur

Fonctionnalités MVP :
- Tableau de bord des mesures (courbes 24h)
- Alertes seuils critiques (SMS ou LED, sans cloud)
- Recommandations automatiques explicables
- Historique et tendances avec export JSON
- Pilotage manuel des actionneurs
- Journal d'actions avec horodatage

Extensions possibles :
- Prédiction 24h des besoins en eau (régression simple)
- Scénarios saisonniers paramétrables
- Détection anomalies capteurs (plateau RSSI suspect)
- Calibrage automatique humidité sol (courbe 0%-100% par plant variant)
- Intégration données météo extérieures par Web public (cible : prédiction soleil pour LED)
- Support de multiples serres en parallèle

KPI de validation :
- Réduction dépassements seuil critique (humidité sol <15% : <3 occurrences sur cycle de 3 mois)
- Stabilité conditions de culture (temp ±3°C, humidité ±10%)
- Précision recommandations vs décisions expertes (>80% accord)
- Temps cumulé service en mode autonome sans intervention humaine (>95%)
- Rendement final (récolte viable OU analyse causale qualifiée en cas d'échec)
- Consommation d'eau totale vs témoin non-instrumenté
- Énergie utilisée vs autonomie batterie prédite

Valeur pédagogique :
- Chaîne IoT complète capteur -> backend -> interface web/mobile
- Modélisation de données temporelles et séries
- IA interprétable pour prise de décision (vs boîte noire)
- Sûreté de fonctionnement et priorité des fonctions vitales
- Eco-conception et mesure d'impact technique
- Post-mortem scientifique en cas d'échec biologique
- Edge computing (informatique en périphérie) et hébergement souverain
- Gestion énergie et autonomie système embarqué

---

### Projet E - Plateau de jeu robotisé stratégique
Objectif :
Concevoir un plateau de jeu physique capable de déplacer automatiquement des pièces selon les décisions d'une IA, avec perception visuelle de l'état de la partie et action mécanique précise.

Utilisateurs cibles :
- Joueur humain
- Observateur pédagogique qui suit la logique de décision de l'IA

Composants possibles :
- **Système de mouvement** :
  - Plateau motorisé (pivot ±90° via servo 200° 80kg/cm) OU système cartésien XY gantry (moteurs pas-à-pas NEMA17)
  - Encodeurs optiques sur moteurs pour retour de position
  - Système de coordonnées absolues (endstop magnétiques)
- **Perception** :
  - Caméra USB 1080p montée en zénith avec calibrage géométrique
  - Éclairage LED RVB ambigu (minimiser ombres)
  - Détection de pièces par couleur + appariement de motifs (OpenCV)
- **Préhension/Action** :
  - Électro-aimant 24V 50N pour pièces ferrées OU servo pour poussée douce
  - Bras léger (effecteur piloté par Arduino) si manipulation
  - Mécanisme de blocage pièces sur trajet (roulements)
- **Intelligence** :
  - Moteur de règles pour échiquier (openChess ou compatible)
  - IA stratégie simplifiée (Minimax avec α-β, profondeur 3-4)
  - Backend .NET pour orchestration
- **Communication** : Wi-Fi local pour superviseur web

Détail fonctionnel attendu :
- **Parcours 1 - Coup autonome** : la caméra capture le plateau, détecte les positions des pièces (état du plateau), l'IA calcule le meilleur coup en <5s, puis le système déplace la pièce source vers la destination via moteurs + effecteur. Mouvement exécuté en boucle fermée avec correction si variation ±1cm
- **Parcours 2 - Vérification cohérence** : après chaque coup, rescane du plateau entier, validation état réel vs état attendu. Si pièce mal positionnée, signal LED rouge + demande de confirmation humaine ("Correction pièce détectée, valider ?")
- **Parcours 3 - Traçabilité décision** : l'interface web affiche pour chaque coup : pièce déplacée, destination, coups alternatifs envisagés (top 3), justification IA ("Protège cavalier, contrôle centre"), score de position post-coup. L'utilisateur peut "rejouer" les coups passés en mode visualisation
- **Parcours 4 - Gestion incidents** :
  - Pièce bloquée <5cm de destination : essai tassement x3, sinon alerte 
  - Pièce mal reconnue après coup : mode manuel 30s pour correction utilisateur
  - Batterie <15% : signalement + arrêt gracieux
- **Parcours 5 - Mode spectateur** : affichage temps réel plateau via projecteur ou tablette, annotations mouvements en couleur (pièce en vert, destination en jaune)

Fonctionnalités MVP :
- Reconnaissance des pièces et position (précision >95%)
- Exécution coups automatiques (latence <10s)
- Historique coups avec justification IA minimale
- Mode pause/reprise avec validation humaine
- Échiquier uniquement (règles complètes)

Extensions possibles :
- Support de multiples jeux (dames, Othello, jeu chinois)
- Stratégie IA avancée (réseau de neurones convolutif pour évaluation position)
- Mode "puzzles" pédagogique (IA donne indices)
- Reconnaissance adversaire par webcam (position joueur utilisée pour adaptation de la difficulté)
- Partage partie via réseau (IA vs IA)

KPI de validation :
- Reconnaissance correcte des pièces : >95% en première tentative
- Taux coups exécutés sans intervention : >90%
- Précision placement ±2cm en destination
- Temps par coup (calcul + exécution) : <15s
- Disponibilité système : >98% sur 1h partie

Valeur pédagogique :
- Vision par ordinateur (détection, calibrage caméra, perspective)
- Prise de décision IA avec temps limité (minimax avec pruning)
- Robotique de manipulation de précision
- Orchestration temps réel d'états complexes
- Validation avec humain dans la boucle

Fonctionnalités MVP:
- Reconnaissance des pièces et de leur position
- Exécution automatique de déplacements simples
- Historique des coups
- Mode pause/reprise avec validation humaine

Extensions possibles:
- Stratégie IA plus avancée
- Support de plusieurs jeux (échecs, dames, othello simplifié)
- Mode spectateur avec explication des coups

KPI de validation:
- Taux de reconnaissance correcte des pièces
- Taux de coups exécutés sans intervention
- Précision du placement mécanique

Valeur pédagogique:
- Vision par ordinateur
- Prise de décision par IA
- Robotique de manipulation de précision

---

### Projet F - Casier intelligent de prêt de matériel
Objectif :
Gérer un casier connecté permettant de prêter du matériel aux étudiants avec traçabilité, autorisation et suivi des retours.

Utilisateurs cibles :
- Responsable de laboratoire
- Étudiant emprunteur
- Technicien qui gère les états de maintenance

Composants possibles :
- **Serrurerie** :
  - Serrures électroniques intelligentes (ASSA ABLOY ou équivalent) ou électrovannes 12V pour portes casiers
  - Microcontrôleur ESP32 pour orchestration (5-10 casiers max)
  - Clavier 4x4 OU lecteur RFID/NFC pour authentification
  - Affichage LCD/OLED petit écran par casier (numéro casier, état, instruction)
- **Backend de gestion** :
  - API REST .NET ASP.NET Core: POST /reserve, POST /return, GET /inventory, PATCH /maintenance
  - Base PostgreSQL : user (ID_badge, nom, droit), inventory (casier, objet, état), audit (action, who, when, proof_hash)
- **Application web** :
  - Interface React/Vue.js : réservation objet par catégorie, historique emprunts, panneau admin pour gestion d'état
  - Export rapports : utilisation par étudiant, taux de retour, objets manquants, temps moyen de prêt
- **Sécurité et traçabilité** :
  - Photo locale (Pi Camera) au moment retour (preuve dépôt, état objet)
  - Hash versioning des photos pour intégrité
  - Signature numérique de chaque transaction
- **Communication** : Wi-Fi 802.11ac pour réseau lab local

Détail fonctionnel attendu :
- **Parcours 1 - Réservation et prêt** : l'étudiant s'authentifie via badge (scan RFID), sélectionne l'objet désiré. Si disponible et autorisé, la réservation est confirmée avec heure d'ouverture. À l'heure prévue : le casier correspondant s'ouvre (LED verte + bip), objet prélevé. Retrait confirmé par capteur de contact ou capteur image
- **Parcours 2 - Retour matériel** : l'étudiant place l'objet retour dans le casier prévu. Photo automatique prise. L'admin accède au web pour valider le retour :
  - Complet ? -> Libre (vert)
  - Abîmé ? -> Maintenance nécessaire (orange, blocage 1 semaine)
  - Manquant ? -> Alerte (rouge, facturation étudiant si applicable)
- **Parcours 3 - Alertes et gestion retards** : si matériel non retourné 24h après échéance : email auto + SMS si num tel connu. Après 48h : casier automatiquement bloqué pour l'utilisateur
- **Parcours 4 - Checklist état** : lors de chaque retour, images compressées + calcul de hash MD5. L'admin vérifie visuellement vs checklist pré-définie ("4 vis présents ? Batterie dedans ? Aucune rayure ?"). Retour automatisé pour l'étudiant
- **Parcours 5 - Passage maintenance** : objet endommagé -> flux de maintenance : le technicien accède au panneau "à réparer", journal des actions, date estimée de retour en service, reclassification
- **Parcours 6 - Rapports fiabilité** : graphe matériel vs taux de perte/avarie/retard. Top 5 emprunteurs fiables. Recommandation de dépréciation objet (ex. : 6 avaries -> retrait du catalogue)

Fonctionnalités MVP :
- Authentification utilisateur (RFID/badge)
- Réservation et prêt simple (2 clics)
- Journal d'historique consultable
- État des casiers en direct (web + LED)
- Gestion états matériel (OK, à vérifier, indisponible)
- Export CSV basique utilisation
- Photo automatique retour

Extensions possibles :
- Réservation par créneau horaire
- Notification retard (SMS/Slack)
- Inventaire intelligent par catégorie
- Score de fiabilité des emprunteurs (accès tarif réduit si bon score)
- Flux de maintenance intégré
- Rapport mensuel d'usage et pertes
- Intégration avec SAP/ERP pour amortissement
- Code-barres ou QR sur objets pour traçabilité fine

KPI de validation :
- Taux de retour à l'heure (cible >90%)
- Disponibilité casiers (<5 min downtime/semaine)
- Traçabilité objets (100% d'actions loggées)
- Taux d'objets retournés en bon état (cible >95%)
- Diminution pertes vs système manuel (cible -70%)
- Temps consultation disponibilité (<3s)
- Faux positifs détection retour <2%

Valeur pédagogique :
- Système d'information complet (API, interface web, BD)
- Sécurisation accès physique + audit
- UX opérationnelle pour usage quotidien massif
- Gestion d'actifs et maintenance
- Intégration caméra et vision pour preuve
- Autorisation et rôles (user/admin/tech)
- Design scalable pour 100+ étudiants
- Parcours 3: alerte si retard, matériel absent ou ouverture anormale.
- Parcours 4 : checklist d'état au retour (complet, endommagé, batterie faible, accessoire manquant).
- Parcours 5: passage automatique en maintenance ou quarantaine si anomalie détectée.
- Parcours 6: tableau de fiabilité par type de matériel (taux de perte, pannes, retards).

---

### Projet G - Jeu de fléchettes avec reconnaissance par caméra
Objectif :
Concevoir un système de jeu de fléchettes numérique qui détecte automatiquement la position des fléchettes sur la cible par vision par ordinateur, gère les règles du jeu (301, Cricket, etc.) et affiche les scores en direct.

Utilisateurs cibles :
- Joueur en compétition ou loisir
- Animateur/arbitre qui gère les parties
- Spectateur qui visualise les scores et l'historique

Composants possibles :
- **Système d'imagerie** :
  - 3 caméras RGB 4K disposées autour de la cible (ou multi-vue calibrée à 120° d'écart) montées sur rail fixe
  - Résolution 2160x4320 minimum pour détection centimétrique
  - Synchronisation temporelle des 3 flux (déclenchement GPIO ou NTP)
  - Calibrage géométrique 3D (reprojection de positions 2D en 3D)
- **Cible physique** :
  - Cible standard professionnel (68cm) ou améliorée avec marqueurs visuels (LED infra si sobriété)
  - Surface texturée contrastée pour robustesse détection
  - Rechange pointe fléchette recommandée après 500 lancers
- **Éclairage** :
  - Éclairage LED RVB ambigu calibré : 2 spots 50W blancs chaud OU adaptateur Daylight 5500K
  - Réduction des ombres via diffusion, angle 45°
  - Capteur LUX pour normalisation automatique
- **Backend** :
  - Service .NET Core de traitement image (liaison OpenCV ou EmguCV)
  - Moteur de règles (301, Cricket, Around the World, Shanghai) avec logging complet
  - API REST : POST /throw, GET /scores, GET /stats/{joueur}
  - Base PostgreSQL pour historique parties (1000+ parties/saison)
- **Affichage** :
  - Écran tactile 24\" OU projection murale 200\" avec Apple TV
  - Interface temps réel des scores + visualisation fléchettes détectées
  - Leaderboard persistant stocké localement
- **Communication** : Wi-Fi 802.11ac (latence critique), basculement Ethernet filaire

Détail fonctionnel attendu :
- **Parcours 1 - Initialisation partie** : admin crée partie sur tablette :
  - Nom du mode : 301, Cricket, Around the world, Shanghai
  - Nombre de joueurs : 1-8 (validé)
  - Affichage scores cible : réfléchi en fonction du mode (501, 301, etc.)
  - Création de session avec UUID (id partie) stockée immédiatement
- **Parcours 2 - Détection fléchettes** : dès arrivée d'une fléchette dans le FOV (variation d'image >2%), 3 caméras capturent simultanément. Pipeline :
  1. Détection zone sombre (fléchette, tige)
  2. Extraction centroïde 2D par caméra
  3. Triangulation 3D via matrices de calibration
  4. Projection sur plan cible + table de correspondance (x,y) -> (zone cible : simple/double/triple/bullseye)
  - Latence totale : <500ms entre image et résultat points
- **Parcours 3 - Calcul des points** : selon zone + mode de jeu :
  - Mode 301 : si triple 20, 60 points = débuter de 301, descendre à 0 avec finish double
  - Mode Cricket : marqueur de zones (15-20, bullseye), scorer si 3x touches, le meilleur gagne
  - Validation : affichage immédiat "Triple 20 = 60 pts!" + son feedback
- **Parcours 4 - Gestion séquence joueurs** : tour par tour automatique :
  - "Tour 1 - Jean: (affichage score)"
  - Détection de 3 fléchettes (ou saisie utilisateur si timeout 30s)
  - Calcul cumulatif, passage joueur suivant
  - Pause graphique 2s entre joueurs
- **Parcours 5 - Affichage temps réel** :
  - Tableau scores : colonne joueur, score cumulatif, reste à faire (301 - cumul), statut (in/out/bust)
  - Visualisation 2D cible actualisée : points rouges positions derniers coups, zones colorées par joueur
  - Barre progression (pour 301 : graphe cible=100, cumul=80, reste=20)
- **Parcours 6 - Historique et replay** :
  - Bouton "Derniers 3 coups [Jean]" → affichage graphique trajet fléchettes + points
  - Export match JSON : ID partie, joueurs, coups, timestamps
  - Statistiques joueur : taux précision par zone (triple=best, bull=second)
- **Gestion incidents** :
  - Fléchette non détectée ou ambiguë (<60% confiance) : LED jaune + invite joueur/arbitre "Confirmer zone? [Selector]"
  - Fléchette tombée entre caméras : zone par défaut "miss"
  - Joueur conteste : arbitre ajuste le score manuellement en 5s (journal d'audit : "Admin correction Jean -20 pts")
  - Mode dégradé : saisie manuelle zone fléchette via boutons physiques (5 zones = 5 boutons)

Fonctionnalités MVP :
- Détection et localisation fléchettes (>95% reconnaissance 1ère tentative)
- Calcul automatique points (zones cible : simple, double, triple, bullseye)
- Gestion 2 modes de jeu minimum (301, Cricket)
- Interface configuration partie (nombre joueurs, choix mode)
- Affichage scores temps réel avec joueur en cours
- Historique 3 derniers coups par joueur
- Mode manuel de correction et secours

Extensions possibles :
- Support multiples modes de jeu (Around the world, Shanghai, 501)
- Statistiques joueur avancées (taux précision par zone, évolution série)
- Classement multi-parties et ligue locale (table ELO?)
- Notifications vocales des scores
- Reconnaissance des joueurs par visage ou badge (intégration caméra détection)
- Couplage projecteur pour affichage compétition (leaderboard public)
- Analyse IA trajectoires et prédictions
- Synchronisation cloud optionnelle (ligue centralisée, si choix utilisateur)

KPI de validation :
- Précision détection fléchettes (>95% de reconnaissance en 1ère tentative)
- Latence arrivée fléchette → affichage score (<2s cible, <3s acceptable)
- Taux erreurs non récupérées (<2% par partie)
- Disponibilité système lors partie complète (>98% uptime)
- Satisfaction joueurs et arbitres (score >8/10)
- Durée match standard 501 vs temps horloge (objectif : <20min vs 20min manuel)

Valeur pédagogique :
- Vision par ordinateur multi-caméra (calibrage géométrique, triangulation)
- Traitement d'image temps réel (détection objet, contraste robustesse)
- Gestion règles métier complexes et états de jeu
- Interface utilisateur pour compétition (UX temps réel, feedback immédiat)
- Interaction homme-machine et arbitrage
- Synchronisation multi-source et latence critique
- Audit et intégrité données (fairplay)

---

### Projet H - Bataille navale électronique modulaire
Objectif :
Concevoir un jeu de bataille navale physique-numérique avec deux plateaux par joueur, un affichage lumineux de l'état des navires, un écran de supervision, et une communication radio entre modules indépendants.

Utilisateurs cibles :
- Joueur en duel local (2 modules)
- Joueur solo contre IA (1 module)
- Observateur pédagogique qui suit les états de jeu en temps réel

Composants possibles :
- **Module joueur (x1 ou x2)** :
  - 1 plateau vertical lumineux (état flotte du joueur)
  - 1 plateau horizontal lumineux (zone de tir sur l'adversaire)
  - 1 écran (LCD/TFT) pour l'état de partie, les étapes et le choix du mode
  - 1 microcontrôleur ESP32 (ou équivalent) avec radio embarquée
- **Détection de position des bateaux** :
  - Grille instrumentée (contacts magnétiques/reed, Hall, ou autre détection de présence)
  - Calibration automatique de la grille au démarrage
  - Validation anti-erreur (navires hors grille, chevauchement interdit)
- **Affichage lumineux** :
  - Matrice LED RGB (WS2812B ou équivalent) sur chaque plateau
  - Codification d'état claire :
    - navire non touché
    - navire touché
    - navire coulé
    - tir ennemi dans l'eau
    - eau libre
- **Communication radio** :
  - Lien sans fil entre deux modules (ESP-NOW, mesh léger, ou protocole équivalent)
  - Synchronisation d'état de tour, tirs, accusés de réception et fin de partie
  - Fonctionnement sans liaison physique filaire entre joueurs
- **Backend local optionnel** :
  - Service .NET 10 pour journaux, analyses de partie, replay, et supervision web locale

Détail fonctionnel attendu :
- **Parcours 1 - Placement des navires** : le joueur place virtuellement ses bateaux sur le plateau vertical. Le système détecte automatiquement les positions et vérifie la validité de la configuration. L'écran guide étape par étape ("placer porte-avions", "placer destroyer", etc.).
- **Parcours 2 - Vue flotte (plateau vertical)** : le plateau vertical affiche en continu l'état de la flotte du joueur : navires intacts, touchés, coulés, et impacts ennemis dans l'eau.
- **Parcours 3 - Vue attaque (plateau horizontal)** : le joueur sélectionne ses tirs sur le plateau horizontal. L'interface lumineuse et l'écran indiquent les cases déjà jouées, les touches, les ratés et l'avancement global.
- **Parcours 4 - Communication inter-modules** : chaque tir est transmis par radio à l'autre module, puis validé (touché/coulé/raté). Les deux écrans restent synchronisés sur la phase de jeu en cours.
- **Parcours 5 - Mode IA** : avec un seul module, le joueur affronte une IA locale. L'IA propose plusieurs niveaux (aléatoire, chasse ciblée, stratégie probabiliste simple).
- **Parcours 6 - Choix du type de jeu** : l'écran permet de choisir le mode (solo IA, duel 2 modules), la taille de grille (si extensible), et éventuellement des variantes de règles.
- **Mode dégradé** : si radio indisponible temporairement, mise en file locale des actions et reprise automatique à la reconnexion avec résolution de cohérence.

Fonctionnalités MVP :
- Détection automatique du placement des navires
- Affichage lumineux des états navire/eau sur le plateau vertical
- Sélection des tirs sur le plateau horizontal
- Synchronisation radio de base entre 2 modules
- Mode solo contre IA locale
- Écran d'état de partie avec guidage des étapes

Extensions possibles :
- Modes de jeu avancés (salves, brouillard de guerre, grilles variables)
- IA améliorée (chasse probabiliste + apprentissage des patterns)
- Journal et replay local des parties
- Tableau de statistiques (précision, durée, nombre de coups)
- Effets visuels/sonores renforcés pour feedback pédagogique
- Tournois multi-modules sur réseau maillé

KPI de validation :
- Taux de détection correcte du placement des navires (>98%)
- Latence tir -> retour d'état (touché/raté) en duel (<500 ms)
- Taux de désynchronisation inter-modules (<1% par partie)
- Stabilité mode IA sur partie complète (>99% sans blocage)
- Compréhension utilisateur de l'état lumineux (>8/10 en test utilisateur)

Valeur pédagogique :
- Systèmes embarqués interactifs (détection + action + rendu)
- Conception d'un protocole radio fiable et tolérant aux pertes
- Gestion d'état distribué et synchronisation temps réel
- UX de jeu tangible (plateaux lumineux + écran de guidage)
- IA de stratégie discrète et évaluation de performance

---

### Projet I - Machine solveur de Rubik's Cube
Objectif :
Concevoir une machine capable d'analyser un Rubik's Cube mélangé, vérifier la cohérence de reconnaissance des couleurs, calculer une solution valide puis exécuter automatiquement les rotations jusqu'à résolution complète, avec un suivi visuel clair pour l'utilisateur.

Utilisateurs cibles :
- Utilisateur grand public qui lance une résolution en un bouton
- Observateur pédagogique qui suit les étapes (vision, calcul, action)

Composants possibles :
- **Mécanique de manipulation** :
  - Berceau de maintien du cube avec pinces souples anti-glissement
  - 4 à 6 actionneurs (servos couple élevé ou moteurs pas-à-pas) pour effectuer les rotations des faces
  - Fins de course ou encodeurs pour vérifier l'angle réel de rotation (90°/180°)
- **Perception visuelle** :
  - Caméra RGB fixe ou module multi-vues (1-2 caméras) avec éclairage LED uniforme
  - Fond et gabarit de prise de vue pour réduire les erreurs de segmentation
  - Pipeline OpenCV pour détection des 54 stickers et classification couleur
- **Calcul de solution** :
  - Backend .NET 10 (ASP.NET Core) ou service embarqué pour orchestration
  - Solveur algorithmique (Kociemba 2-phase ou équivalent) pour générer la séquence de mouvements
  - Validation de l'état du cube (parités, nombre de couleurs, configuration solvable)
- **Interface utilisateur** :
  - Écran tactile 3-5" ou interface web locale
  - Bouton physique "Lancer" + voyant d'état (analyse, calcul, exécution, terminé)
  - Barre de progression globale + compteur de mouvements restants
- **Communication et données** :
  - Wi-Fi local pour supervision optionnelle
  - Journal local des sessions (temps analyse, temps calcul, temps exécution, erreurs)

Détail fonctionnel attendu :
- **Parcours 1 - Lancement simple** : l'utilisateur mélange son Rubik's Cube, le place dans la machine, puis appuie sur l'écran ou le bouton physique pour démarrer. L'interface passe immédiatement en mode "Analyse en cours".
- **Parcours 2 - Analyse des faces** : la machine capture les 6 faces, détecte les facettes une à une et affiche une vue synthétique du cube reconstruit. Chaque couleur reconnue est visualisée sur un mini-cube 3D/2D.
- **Parcours 3 - Vérification de cohérence** : avant tout mouvement, le système vérifie qu'il n'y a pas d'erreur de reconnaissance :
  - 9 stickers par couleur
  - centres cohérents
  - état mathématiquement solvable
  - en cas d'erreur, message explicite et reprise de capture automatique ou assistance manuelle
- **Parcours 4 - Calcul de la solution** : le solveur calcule la séquence optimale ou quasi-optimale, puis affiche : nombre total de mouvements, estimation du temps, et premières étapes prévues.
- **Parcours 5 - Exécution mécanique** : la machine enchaîne les mouvements du cube en boucle contrôlée. Chaque rotation est confirmée par capteur/encodeur et l'interface met à jour la progression globale (ex : 23/48 mouvements).
- **Parcours 6 - Fin de cycle** : lorsque le cube est résolu, l'écran affiche une confirmation visuelle (état final résolu), émet un signal sonore court, puis l'utilisateur récupère le cube.
- **Mode de sécurité** : arrêt immédiat possible via bouton stop. En cas de blocage mécanique, la machine s'interrompt, journalise l'incident et propose reprise ou annulation.

Fonctionnalités MVP :
- Lancement de la résolution par bouton/écran
- Reconnaissance automatique des 6 faces
- Vérification de validité de l'état du cube
- Calcul de solution avec séquence de mouvements
- Exécution mécanique complète de la séquence
- Affichage de progression globale et étape courante
- Journal de session local

Extensions possibles :
- Optimisation du temps total (vitesse moteur + séquence minimisée)
- Mode "explication" (afficher la logique de résolution par blocs/étapes)
- Statistiques comparatives par cube (moyenne, meilleur temps, taux d'erreur vision)
- Support de variantes (2x2, 4x4 avec contraintes supplémentaires)
- Détection d'usure mécanique prédictive (maintenance)

KPI de validation :
- Taux de reconnaissance correcte des facettes (>98% cible)
- Taux de détection d'états invalides (100% des cas de test préparés)
- Taux de résolution complète sans intervention (>90% en MVP)
- Temps moyen total d'un cycle (analyse + calcul + exécution)
- Écart entre mouvements planifiés et exécutés (0 mouvement perdu)
- Taux d'arrêts d'urgence ou blocages mécaniques (<5% des cycles)

Valeur pédagogique :
- Vision par ordinateur appliquée à un objet structuré (détection couleur, robustesse éclairage)
- Algorithmique de recherche/optimisation (solveur de cube)
- Robotique mécanique de précision (actionneurs, asservissement, anti-blocage)
- UX temps réel avec transparence des étapes et progression
- Sécurité opérationnelle (stop, reprise, gestion d'anomalies)
- Intégration système complète capteur -> calcul -> action


## 9) Méthode de choix et affectation des 5 groupes
Avec 9 idées disponibles (A à I), les étudiants disposent d'un vrai choix de sujet.

Processus recommandé :
- Étape 1 : chaque groupe soumet un top 3 de projets (ordre de préférence).
- Étape 2 : arbitrage enseignant selon faisabilité technique et équilibre de charge.
- Étape 3 : validation officielle des 5 sujets retenus (1 sujet par groupe).

Règles d'arbitrage suggérées :
- Priorité aux sujets couvrant bien le socle complet (embarqué + backend + IA + interface).
- Éviter que plusieurs groupes prennent des sujets trop similaires.
- Garantir au moins 1 sujet orienté mobilité/robotique et 1 sujet orienté IoT environnement.

Classement recommandé par difficulté et budget :

| Projet | Intitulé | Difficulté | Budget matériel | Commentaire |
| --- | --- | --- | --- | --- |
| F | Casier intelligent de prêt de matériel | Faible à moyenne | Faible à moyen | Solide pour gestion d'accès et traçabilité |
| A | Mini robot interactif de bureau | Moyenne | Moyen | Bon point d'entrée pour embarqué + UX |
| G | Jeu de fléchettes avec reconnaissance par caméra | Moyenne à élevée | Moyen | Vision applicative, ludique, bon potentiel démo |
| H | Bataille navale électronique modulaire | Moyenne à élevée | Moyen | Jeu physique connecté, synchronisation radio et UX lumineuse |
| I | Machine solveur de Rubik's Cube | Moyenne à élevée | Moyen à élevé | Excellente synthèse vision + algorithmique + mécanique |
| C | Géolocalisation indoor en temps réel | Moyenne à élevée | Moyen à élevé | Sensible à la calibration et aux mesures |
| D | Serre low-tech intelligente | Élevée | Moyen à élevé | Excellent sujet, mais fort risque terrain |
| B | Mini véhicule autonome indoor | Élevée | Élevé | Très visible, intégration mécanique exigeante |
| E | Plateau de jeu robotisé stratégique | Élevée | Élevé | Très attractif, mécanique de précision et perception |

Exemple de combinaison cohérente sur 5 groupes :
- Groupe 1 : Projet A (mini robot interactif)
- Groupe 2 : Projet B (véhicule)
- Groupe 3 : Projet C (géolocalisation)
- Groupe 4 : Projet D (serre)
- Groupe 5 : Projet E (plateau de jeu robotisé)

Couplage inter-projets recommandé :
- Projet B (véhicule) <-> Projet C (géolocalisation) via API commune.

## 10) Jalons proposés
- Jalon 1 (Semaine 4) : fin de Période 1 + Soutenance 1 (cadrage et faisabilité)
- Jalon 2 (Semaine 9) : fin de Période 2 + Soutenance 2 (MVP fonctionnel)
- Jalon 3 (Semaine 18) : fin de Période 3 + Soutenance 3 (intégration IA + électronique et système stabilisé)
- Jalon 4 (Final) : Soutenance finale transverse (bilan, démo, perspectives)

## 11) Conclusion
Le cadre proposé permet de conserver l'esprit initial (IA appliquée, concret, ludique) tout en ajoutant un niveau de détail suffisant pour piloter 5 groupes de manière homogène et évaluable.

Le catalogue retenu (9 sujets) augmente le choix et facilite l'alignement entre intérêts des étudiants, budget matériel et niveau de difficulté.
