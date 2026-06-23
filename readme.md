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
- Découpage temporel : 3 périodes (4, 5 et 9 semaines, soit 18 semaines au total)
- Évaluation orale : 1 soutenance à la fin de chaque période + 1 soutenance finale (soit 4 soutenances)

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
- DevOps : gestion de version, CI simple, documentation déploiement

Principes transverses inspirés du projet serre (à appliquer à tous les sujets) :
- Local-first : chaîne logicielle hébergée en local (acquisition, stockage, backend, interface), sans dépendance cloud obligatoire.
- Continuité de service : le système doit conserver ses fonctions critiques même si l'interface tombe ou si le réseau est indisponible.
- Sobriété mesurée : chaque groupe suit et justifie les ressources consommées (énergie, eau, matériaux, temps machine).
- UX utile : les interfaces privilégient des actions claires plutôt que des dashboards complexes.
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
- Période 1 (Semaines 1 à 4) : cadrage, état de l'art, architecture cible, preuve de faisabilité
- Période 2 (Semaines 5 à 9) : MVP logiciel + premier prototype électronique intégré + consolidation technique
- Période 3 (Semaines 10 à 18) : module IA opérationnel, intégration système, robustesse, tests en conditions réelles, finalisation des livrables

Soutenances :
- Soutenance 1 : fin Période 1 (semaine 4, revue de cadrage)
- Soutenance 2 : fin Période 2 (semaine 9, revue MVP)
- Soutenance 3 : fin Période 3 (semaine 18, revue d'intégration et validation technique)
- Soutenance finale : présentation finale complète (résultats, démo, retour critique)

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

### Définition of done (obligatoire)
Un projet est considéré valide uniquement si :
- le MVP est démontrable en conditions réelles,
- les exigences EF/ENF critiques sont vérifiées par des tests tracés,
- les modes de panne et le mode dégradé sont démontrés,
- un post-mortem technique est fourni en cas d'échec partiel.

### Livrables attendus à chaque soutenance
- Soutenance 1 (Semaine 4) : problème cible, EF/ENF v1, architecture v1, preuve de faisabilité.
- Soutenance 2 (Semaine 8) : MVP intégré (software + électronique), tests de base, premier retour utilisateur.
- Soutenance 3 (Semaine 12) : système consolidé, IA exploitable, tests d'intégration et robustesse.
- Soutenance 4 (Semaine 16) : validation terrain, corrections, dossier quasi final.
- Soutenance finale : bilan global, démo complète, mesures KPI, limites et feuille de route.

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
- **Actionneurs simples** : servo moteur 180° pour orientation tête, verin soude pour action palpable (ascenseur de carte, préhension lumière)

Détail fonctionnel attendu :
- **Parcours 1 - Enregistrement vocal** : l'utilisateur parle au robot, qui capture l'audio, l'envoie au backend NLP local, remet en forme la commande reconnue, l'affiche à l'écran en couleur et demande confirmation vocale ("Vous avez demandé ... c'est correct?"). Latence cible : <2s
- **Parcours 2 - Tâches et rappels** : le robot affiche un récapitulatif des 3 prochaines tâches sur l'écran avec leur priorité codée par couleur. L'utilisateur peut valider ou repousser l'ordre via les boutons. Actions l'e-mail sont synchronisées au backend
- **Parcours 3 - Confirmation tangible** : quand une tâche est validée, le robot tourne sa tête 90°, émet un signal sonore spécifique et lum ineux, puis revient à la position initiale. Cela rend l'IA tangible et intéractive
- **Parcours 4 - Tuteur observateur** : l'interface web (localhost:8080) affiche en direct l'historique des 20 derniers déverrouillages vocaux : texte reconnais, intention detectée, action exécutée, timestamp. Filtre par date ou type d'intention
- **Gestion d'erreurs** : si la reconnaissance vocale ne capture rien ou décide avec faible confiance (<60%), le robot propose 2-3 commandes similaires dont l'utilisateur peut choisir. Si toujours incertain, passage en manuel (boutons)
- **Mode dégradé** : fonctionnement complet sur réseau local sans Internet. Si NLP central indisponible, basculement automatique sur modèle léger embarqué (reconnaissance pattern simple)
- **Alimentation et veille** : en absence de parole pendant 10min, écran en veille de 30%, moteurs désactivés. Tap sur le bouton physique réveille

Fonctionnalités MVP :
- Commandes vocales basiques (reconnaissance intenté : 5-10 commandes majeures)
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
- NLP appliquée (tokenization, intent classification)
- Design d'interaction homme-machine et feedback utilisateur
- Intégration électronique visible et tangible
- Architecture event-driven avec message broker local (RabbitMQ ou Redis)
- Gestion état d'une application multi-composants
- Circuit breaker et résidence locale pour robustesse

---

### Projet B - Mini véhicule autonome indoor
Objectif :
Concevoir un petit véhicule autonome capable de suivre un circuit intérieur, détecter des obstacles et s'arrêter en sécurité.

Utilisateurs cibles :
- Opérateur de démonstration
- Évaluateur sécurité

Composants possibles :
- **Châssis** : plateforme robotique 20-30cm (DFRobot, SCUTTLE ou compatible), 500g max, roues tout-terrain
- **Moteurs** : deux moteurs DC 12V 100RPM avec encodeurs optiques (retour de position) + controles H-bridge L298N
- **Batterie** : Li-Po 7.4V (2S) 5000mAh minimum, chargeur USB-C integrate
- **Capteurs de perception**:
  - **Lidar** : YDLIDAR X4 (360°, 10m, peu di coteux) OU 5-6 capteurs ultrason (HC-SR04) pointés en éventail
  - **Encodeurs** : 2x encodeurs optiques sur les moteurs (résolution 20+ coups/tour)
  - **IMU** : capteur 9-DOF (accélero, gyro, magnéto : MPU6050 ou BNO055)
  - **Caméra** : webcam USB optionnelle pour détection de ligne au sol
- **Microcontrôleur** : Raspberry Pi 4 (4GB) avec GPIO PWM pour moteurs OU ESP32 pour architecture légère
- **Communication** : Wi-Fi pour dashboard temps réel + frequénce aréniøres 433MHz pour emergency stop radio
- **Système de sécurité** : bouton d'arrêt d'urgence mécanique, circuit de sécurité embarquée indépendante (Arduino nano redondant)

Détail fonctionnel attendu :
- **Parcours 1 - Mission autonome** : Opérateur définit un circuit via interface web (4-6 checkpoints GPS indoor alias + hauteur), véhicule se localise à l'init avec calibrage, exécute la mission en boucle avec suivi de position estimée, revient au point de départ avec précision <50cm
- **Parcours 2 - Détection obstacle** : capteurs continuellement actifs, fusion Lidar OU ultrason pour résolution 30cm. Si obstacle détecté à <1m, freinage d'urgence en <100ms, pause 1s. Tentative contournement simple (décal de 30cm latéral). Si contournement échoue 2x, signalement par LED rouge + appel radio emergency + alerte web
- **Parcours 3 - Mode manuel** : interface web avec joystick virtuel, l'opérateur reprend contrôle avec latence <500ms. Affichage télémétrie en temps réel : position estimée, vitesse, batterie, distance obstacle
- **Journal mission** : chaque sortie enregistrée localement (JSON) : timestamp, vitesse moyenne, distance parcourue, obstacles rencontrés, actions correctives, batterie à la fin. Export en CSV pour analyse post-mission
- **Sécurité de fonctionnement** : boucle d'arrêt embarquée indépendante qui coupe immédiatement les moteurs si : signal radio perdu >2s, tension batterie <10%, collision détectée. Cette boucle s'exécute à 50Hz sur microcontrôleur dédié
- **Calibrage terrain** : à chaque démarrage, véhicule effectue une ronde d'exploration pour mapper l'environnement (durée : <3min), stocke la carte en RAM

Fonctionnalités MVP :
- Déplacement autonome sur parcours prédéfini (3-4 waypoints)
- Détection d'obstacles et arret d'urgence
- Télémétrie en temps réel sur dashboard
- Mode manuel de secours avec joystick web
- Journalisation mission avec export CSV
- Système d'arrêt d'urgence redéterministe embarqué

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
- Disponibilité radio emergency stop (>99%)

Valeur pédagogique :
- Robotique mobile et cinématique (différentiel, odmétrie)
- Fusion capteurs (Kalman filter simplifié pour position)
- Contraintes temps réel et boucles de contrôle
- Sécurité de fonctionnement (fail-safe design)
- Architecture distribuée (contrôle embarqué + supervision cloud local)

---

### Projet C - Géolocalisation indoor en temps réel
Objectif :
Créer un système de localisation indoor (balises + algorithme) pour suivre un objet mobile, potentiellement le véhicule du Projet B.

Utilisateurs cibles :
- Opérateur de flotte indoor
- Équipe analyse des trajectoires

Composants possibles :
- **Infrastructure de localisation** :
  - **Option 1 : BLE Beacons** : 4-6 balises iBeacon TX @ -4dBm, fixées aux coins de la zone (10m x 15m ideal), calibrage distance d'reférence
  - **Option 2 : UWB (Ultra-Wideband)** : Qorvo ou Decawave (plus précis à 10-15cm mais coûteux)
  - **Option 3 : Wi-Fi triangulation** : utiliser les RSSI des APs campus + théorématique d'atténuation
- **Noeuds de mesure** : récepteurs ESP32 avec BLE ou UWB dispersés stratégiquement, filé en rséau local
- **Serveur de triangulation** : backend .NET 10 ASP.NET Core exposant algorithme Trilatération ou Kalman simplifié. API REST : POST /locate avec balises signalées, GET /history/{objet_id}
- **Interface cartographique** : SVG interactif avec plan du bâtiment, point position temps réel, trace historique dernier 1h coloriée par vitesse
- **Base données locale** : PostgreSQL ou SQLite pour historique avec index sur (timestamp, objet_id). Retention configurable (défaut : 1 semaine)
- **Communication** : Li-Fi ou 802.11ac pour bande passante temps réel, fallback sur 802.11b si surcharge

Détail fonctionnel attendu :
- **Parcours 1 - Initialisation zone** : admin web enregistre zone physique (dimensions, obstacles statiques), place 4-6 balises virtuelles dans plan. Système effectue calibrage de référence : parcours complet de la zone avec un objet de référence connu, enregistre RSSI par balise par position (grille 1m). Durée : 15-20min, résultats sauvegardés localement
- **Parcours 2 - Suivi temps réel** : objet mobile (véhicule, personne avec beacon) transmet signal périodiquement (toutes les 500ms). Noeuds récepteurs envoient au serveur leur signalé + timestamp. Serveur applique Trilatération, estime position, met à jour carte. Latence cible : <1s du signal à l'affichage. Affichage : position en cercle, vecteur vitesse, precision radius (cercle d'incertitude) en couleur (vert si <30cm, orange si <50cm, rouge si >50cm)
- **Parcours 3 - Export traces** : bouton "Export mission" charge dernier 1h d'historique, genere JSON + CSV avec colonnes : timestamp, X, Y, vitesse, objets proches, incidents. Fichier stocke localement
- **API inter-projet** : endpoint /locate/latest/{objet_id} retourne {x, y, precision, updated_at} en JSON. Projet B peut appeler cette API pour synchroniser sa carte interne. Latence max 100ms
- **Souverainété données** : aucun cloud. Base PostgreSQL locale obligatoire, chiffrée à repos (PgCrypto). Retention configurable par admin (par défaut 7 jours, purge auto). Droit à l'oubli : suppression manuelle ou par expiration
- **Continuité réseau** : si réseau central indisponible >30s, chaque noeud bascule sur cache local + sync différentielle une fois réseau rétabli

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
- Comparaison précision BLE vs Wi-Fi vs UWB (dashboard comparative)
- Détection anomalies (saut position anormal -> perte capteur)

KPI de validation :
- Erreur moyenne de position (cible : <1m en 95% des cas)
- Taux de rafraîtchissement stable (constance <10% jitter)
- Disponibilité de l'API (>99%)
- Capacité à continuer localisation en cas de coupure réseau partielle (1-2 noeuds hors ligne : persist <20s)
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
  - Capteur humidité sol : two capacitance probe (DFRobot SEN0193 ou équivalent) avec dual points de mesure (haut/bas)
  - Capteur température/humidité air : DHT22 ou BME280 (baromètre bonus)
  - Capteur luminosité : LUX BH1750 (0-65536 lux)
  - Capteur débit d'eau : compteur turbine YF-S201 pour arrosage
  - Voltmètre batterie (ADC intégré)
- **Actionneurs** :
  - Pompe arrosage : 12V 1000mL/min avec tête spray ajustable
  - Ventilateur axial : 5V 50mm pour circulation air
  - LED horticole optionnelle : strip 18W LED rouges+bleues (ratio 3:1)
  - Solénoïde de drain (optionnel)
- **Électronique** : ESP32 Dev Board avec shield relay (4 canaux) + carte d'acquisition analogique
- **Stockage eau** : réservoir PVC transparent 10L avec flotteur magnétique (low battery alert)
- **Alimentation** : batterie Li-Po 5000mAh (min 5 jours autonomie) + panneau solaire 20W en option
- **Communication** : Wi-Fi 802.11ac + RTC embarqué (DS3231) pour persistance date
- **Base locale** : SQLite ou TimescaleDB (Postgres léger) pour séries temporelles

Détail fonctionnel attendu :
- **Parcours 1 - Acquisition continue** : chaque capteur lu toutes les 5min, données envoyées au backend local, stockées avec timestamp. Dashboard affiche courbes temps réel pour 24h glissantes : temp, humidité sol, humidité air, luminosité. Moyennes horaires calculées et archivées
- **Parcours 2 - Recommandations explicables** : modèle de décision local (arbres de décision ou rules engine simple) évalue état serre vs contraintes plante. Ex:
  - SI humidité_sol < 30% ALORS "Arroser maintenant (raison : sol sec depuis 2h, événements : aucun)"
  - SI temp > 28°C ET humidité < 40% ALORS "Ventiler immédiatement (raison : climat trop chaud et sec)"
  - SI soleil < 2h AUJOURD'HUI ET LED disponible ALORS "Lumière insuffisante, allumer LED 4h ce soir?"
  - Chaque action est justifiée par critères mesurables
- **Parcours 3 - Pilotage manuel** : l'utilisateur peut forcer l'arrosage, ventilation ou LED depuis l'app mobile (locale). Pendant 5s après action manuelle, l'IA se met en pause. Résultats immédiatement visibles sur capteurs (pour confirmer l'action a fonctionné)
- **Parcours 4 - Journal agronomique** : chaque action (arrosage, ventilation, LED) loggée avec raison, durée, volume d'eau consommé, énergie utilisée. Interface affiche timeline : "09:30 - Arrosage (30s, 150mL eau) - Raison : humidité sol en baisse"
- **Parcours 5 - Application smartphone locale** : accessible sur réseau local via QR-code (http://serre.local:8000). Interface minimale : état serre (feu tricolore), recommandation en gros texte, historique 3 dernières actions. Pas de notifications push (sobriété), consultation manuelle
- **Parcours 6 - UX d'action** : recommandations formatées comme des questions simples :
  - "Arroser maintenant? (oui/non)"
  - "Ventiler? (non/rapide/long)"
  - "LED ce soir? (non/4h/8h)"
  - Pas d'affichage de valeurs brutes à l'utilisateur non-technicien
- **Mode autonome** : en absence d'interface pendant 24h, serre continue fonctionnement sur règles déterministes locales (seuils fixes sauvegardés)

Architecture de sûreté recommandée :
- **Niveau 1 (embarqué prioritaire)** : règles vitales locales exécutées à 50Hz sur ESP32 (interrupt timer) : 
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
- IoT complet capteur->backend->interface web+mobile
- Modélisation de données temporelles et séries
- IA interprétable pour prise de décision (vs boîte noire)
- Suretté de fonctionnement et priorité fonctions vitales
- Eco-conception et mesure d'impact technique
- Post-mortem scientifique en cas d'échec biologique
- Edge computing et hébergement souverain
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
  - Système de coordonnées absolu (endstop magnétiques)
- **Perception** :
  - Caméra USB 1080p montée en zénith avec calibrage géométrique
  - Éclairage LED RVB ambigu (minimiser ombres)
  - Détection pièces par couleur + template matching (OpenCV)
- **Préhension/Action** :
  - Électro-aimant 24V 50N pour pièces ferrées OU servo pour poussée douce
  - Bras léger (Arduino-controlled end-effector) si manipulation
  - Mécanisme de blocage pièces sur trajet (roulements)
- **Intelligence** :
  - Moteur de règles pour échiquier (openChess ou compatible)
  - IA stratégie simplifiée (Minimax avec α-β, profondeur 3-4)
  - Backend .NET pour orchestration
- **Communication** : Wi-Fi local pour superviseur web

Détail fonctionnel attendu :
- **Parcours 1 - Coup autonome** : caméra capture plateau, détecte positions pièces (board state), IA calcule meilleur coup en <5s, système déplace pièce source vers destination via moteurs+end-effector. Mouvement exécuté en boucle fermée avec correction si variation ±1cm
- **Parcours 2 - Vérification cohérence** : après chaque coup, re-scan plateau entier, valide état réel vs état attendu. Si pièce mal positionnée, signal LED rouge + demande confirmation humaine ("Correction pièce détectée, valider?")
- **Parcours 3 - Traçabilité décision** : interface web affiche pour chaque coup : pièce déplacée, destination, coups alternatifs envisagés (top-3), justification IA ("Protège cavalier, contrôle centre"), score position post-coup. Utilisateur peut "rejouer" coups passés en mode visualisation
- **Parcours 4 - Gestion incidents** :
  - Pièce bloquée <5cm de destination : essai tassement x3, sinon alerte 
  - Pièce mal reconnue après coup : mode manuel 30s pour correction utilisateur
  - Batterie <15% : signalement + arrêt gracieux
- **Parcours 5 - Mode spectateur** : affichage temps réel plateau via projecteur ou tablette, annotations mouvements en couleur (pièce en vert, destination en jaune)

Fonctionnalités MVP :
- Reconnaissance des pièces et position (accuracy >95%)
- Exécution coups automatiques (latence <10s)
- Historique coups avec justification IA minimale
- Mode pause/reprise avec validation humaine
- Échiquier uniquement (règles complètes)

Extensions possibles :
- Support multiple jeux (dames, Othello, jeu chinois)
- Stratégie IA avancée (réseau de neurones convolutif pour évaluation position)
- Mode "puzzles" pédagogique (IA donne indices)
- Reconnaissance adversaire par webcam (position joueur utilisé pour adaptation difficulté)
- Partage partie via réseau (IA vs IA)

KPI de validation :
- Reconnaissance correcte pièces : >95% en première tentative
- Taux coups exécutés sans intervention : >90%
- Précision placement ±2cm en destination
- Temps coup (calcul + exécution) : <15s
- Disponibilité système : >98% sur 1h partie

Valeur pédagogique :
- Vision par ordinateur (détection, calibrage caméra, perspective)
- Prise de décision IA avec temps limité (minimax avec pruning)
- Robotique de manipulation de précision
- Orchestration temps réel d'états complexes
- Human-in-the-loop validation

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

### Projet L - Casier intelligent de prêt de matériel
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
  - Frontend React/Vue.js : réservation objet par catégorie, historique emprunts, admin panel pour gestion état
  - Export rapports : utilisation par étudiant, taux de retour, objets manquants, temps moyen de prêt
- **Sécurité et traçabilité** :
  - Photo locale (Pi Camera) au moment retour (preuve dépôt, état objet)
  - Hash versioning des photos pour intégrité
  - Signature numérique de chaque transaction
- **Communication** : Wi-Fi 802.11ac pour réseau lab local

Détail fonctionnel attendu :
- **Parcours 1 - Réservation et prêt** : étudiant authenticate via badge (scan RFID), sélectionne objet désiré. Si disponible et autorisé, réservation confirmée avec heure d'ouverture. À l'heure : casier correspondant s'ouvre (LED verte + bip), objet prélevé. Retrait confirmé par capteur contact ou image capteur
- **Parcours 2 - Retour matériel** : étudiant place objet retour dans casier prévu. Photo automatique prise. Admin accède au web pour valider retour :
  - Complète? → Libre (vert)
  - Abîmée? → Maintenance nécessaire (orange, blockade 1 semaine)
  - Manquant? → Alerte (rouge, facturation étudiant si applicable)
- **Parcours 3 - Alertes et gestion retards** : si matériel non retourné 24h après échéance : email auto + SMS si num tel connu. Après 48h : casier automatiquement bloqué pour l'utilisateur
- **Parcours 4 - Checklist état** : lors de chaque retour, images compressées + calcul hash MD5. Admin vérifie visuellement vs checklist pré-définie ("4 vis présents? Batterie dedans? Aucune rayure?"). Feedback automatisé pour étudiant
- **Parcours 5 - Passage maintenance** : objet endommagé -> workflow maintenance workflow : technicien accède panel "à réparer", log actions, date estimée retour à service, reclassification
- **Parcours 6 - Rapports fiabilité** : graphe matériel vs taux de perte/avarie/retard. Top 5 emprunteurs fiables. Recommandation dépréciation objet (ex: 6 avaries -> retrait du catalogue)

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
- Workflow de maintenance intégré
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
- Système d'information complet (API, frontend, BD)
- Sécurisation accès physique + audit
- UX opérationnelle pour usage quotidien massif
- Gestion d'actifs et maintenance
- Intégration caméra et vision pour preuve
- Autorisation et roles (user/admin/tech)
- Design scalable pour 100+ étudiants
- Parcours 3: alerte si retard, matériel absent ou ouverture anormale.
- Parcours 4: checklist d'état au retour (complet, endommagé, batterie faible, accessoire manquant).
- Parcours 5: passage automatique en maintenance ou quarantaine si anomalie détectée.
- Parcours 6: tableau de fiabilité par type de matériel (taux de perte, pannes, retards).

---

### Projet N - Jeu de fléchettes avec reconnaissance par caméra
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
  - Synchronisation temporelle des 3 flux (trigger GPIO ou NTP)
  - Calibrage géométrique 3D (reproject positions 2D en 3D)
- **Cible physique** :
  - Cible standard professionnel (68cm) ou améliorée avec marqueurs visuels (LED infra si sobriété)
  - Surface texturée contrastée pour robustesse détection
  - Rechange pointe fléchette recommandée après 500 lancers
- **Éclairage** :
  - Éclairage LED RVB ambigu calibré : 2 spots 50W blancs chaud OU adaptateur Daylight 5500K
  - Réduction des ombres via diffusion, angle 45°
  - Capteur LUX pour normalisation automatique
- **Backend** :
  - Service .NET Core de traitement image (OpenCV binding ou EmguCV)
  - Moteur de règles (301, Cricket, Around the World, Shanghai) avec logging complet
  - API REST : POST /throw, GET /scores, GET /stats/{joueur}
  - Base PostgreSQL pour historique parties (1000+ parties/saison)
- **Affichage** :
  - Écran tactile 24\" OU projection murale 200\" avec Apple TV
  - Interface temps réel des scores + visualisation fléchettes détectées
  - Leaderboard persistant stocké localement
- **Communication** : Wi-Fi 802.11ac (latence critique), failover Ethernet filé

Détail fonctionnel attendu :
- **Parcours 1 - Initialisation partie** : admin crée partie sur tablette :
  - Nom du mode : 301, Cricket, Around the world, Shanghai
  - Nombre de joueurs : 1-8 (validé)
  - Affichage scores cible : réfléchi en fonction du mode (501, 301, etc.)
  - Création session avec UUID (id partie) stockée immédiatement
- **Parcours 2 - Détection fléchettes** : dès arrivée fléchette dans FOV (frame >2% change), 3 caméras capturent simultanément. Pipeline :
  1. Détection zone sombre (fléchette, tige)
  2. Extraction centroïde 2D par caméra
  3. Triangulation 3D via matrices de calibration
  4. Projection sur plan cible + lookup table (x,y) → (zone cible : simple/double/triple/bullseye)
  - Latence total : <500ms du frame au résultat points
- **Parcours 3 - Calcul points** : selon zone + mode de jeu :
  - Mode 301 : si triple 20, 60 points = débuter de 301, descendre à 0 avec finish double
  - Mode Cricket : marqueur de zones (15-20, bullseye), scorer si 3x touches, le meilleur gagne
  - Validation : affichage immédiat "Triple 20 = 60 pts!" + son feedback
- **Parcours 4 - Gestion séquence joueurs** : tour par tour automatique :
  - "Tour 1 - Jean: (affichage score)"
  - Détection 3 fléchettes (ou user input si timeout 30s)
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
  - Fléchette tombée entre caméras : default zone "miss"
  - Joueur conteste : arbitre ajuste score manuel en 5s (log audit : "Admin correction Jean -20 pts")
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
- Reconnaissance joueurs par visage ou badge (intégration caméra détection)
- Couplage projecteur pour affichage compétition (leaderboard public)
- Analyse IA trajectoires et prédictions
- Sync cloud optionnelle (ligue centralisée, si choix utilisateur)

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


## 9) Méthode de choix et affectation des 5 groupes
Avec 7 idées disponibles (A à E, L, N), les étudiants disposent d'un vrai choix de sujet.

Processus recommandé :
- Étape 1 : chaque groupe soumet un Top 3 de projets (ordre de préférence).
- Étape 2 : arbitrage enseignant selon faisabilité technique et équilibre de charge.
- Étape 3 : validation officielle des 5 sujets retenus (1 sujet par groupe).

Règles d'arbitrage suggérées :
- Priorité aux sujets couvrant bien le socle complet (embarqué + backend + IA + interface).
- Éviter que plusieurs groupes prennent des sujets trop similaires.
- Garantir au moins 1 sujet orientée mobilité/robotique et 1 sujet orientée IoT environnement.

Classement recommandé par difficulté et budget :

| Projet | Intitulé | Difficulté | Budget matériel | Commentaire |
| --- | --- | --- | --- | --- |
| L | Casier intelligent de prêt de matériel | Faible à moyenne | Faible à moyen | Solide pour gestion d'accés et traçabilité |
| A | Mini robot interactif de bureau | Moyenne | Moyen | Bon point d'entrée pour embarqué + UX |
| N | Jeu de fléchettes avec reconnaissance caméra | Moyenne à élevée | Moyen | Vision applicative, ludique, bon potentiel démo |
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
Le cadre proposé permet de conserver l'esprit initial (IA appliquée, concrét, ludique) tout en ajoutant un niveau de détail suffisant pour piloter 5 groupes de manière homogéne et évaluable.

Le catalogue retenu (7 sujets) augmente le choix et facilite l'alignement entre interets des etudiants, budget materiel et niveau de difficulte.
