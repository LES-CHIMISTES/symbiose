# Maquette (faisabilité)

<!--
https://tim-montmorency.com/582523-gestion/#/contenus/3_planification/

# Maquette

## Importance de la maquette dans les projets multimédias
Une maquette permet de déterminer si un projet est réalisable sur les plans technique, économique et opérationnel. Elle aide à identifier les obstacles potentiels et à planifier les ressources nécessaires. Dans le contexte des technologies interactives, où les innovations sont rapides et les attentes des utilisateur·rice·s élevées, cette démarche devient encore plus critique.

## Étapes clés de la maquette

### 1. Aspect technique
- **Analyse des exigences techniques** : Définir les spécifications techniques du projet, y compris les logiciels, le matériel, les interfaces utilisateur et les protocoles de communication.  
- **Compatibilité du système** : Vérifier si les nouvelles technologies interactives sont compatibles avec les systèmes existants.  
- **Tests** : Effectuer des tests pour valider les fonctionnalités et l'interactivité.  

### 2. Aspect économique
- **Estimation des coûts** : Calculer les coûts associés à l'acquisition de matériel, de logiciels, au développement et à la maintenance.  
- **Analyse du retour sur investissement (ROI)** : Évaluer les bénéfices potentiels par rapport aux coûts engagés.  
- **Options de financement** : Explorer les subventions, les partenariats ou les modèles économiques alternatifs.  

### 3. LES RÈGLES ET LE SYSTÈME 

<!-- 1. **Les règles sont les briques de base.**  
2. **Le système applique les règles.**  
3. **L'expérience est la perspective du joueur.**  

### 4. Aspect temporelle
- **Planification du projet** : Établir un calendrier réaliste en tenant compte des délais de développement, de test et de déploiement.  
- **Gestion des risques** : Identifier les risques potentiels qui pourraient retarder le projet et prévoir des plans d'urgence.  

### 5. Aspect légal et éthique
- **Conformité réglementaire** : S'assurer que le projet respecte les lois en vigueur, notamment en matière de propriété intellectuelle et de protection des données.  
- **Accessibilité** : Garantir que l'installation interactive est accessible à tous les utilisateur·rice·s, y compris les personnes en situation de handicap.  

-->

## Scénarisation de l'interactivité
 
#### Phase 1 : Préparation (0-2 min)
| Verbe action | Condition de déclenchement | Effet visuel | Effet sonore | Effet interactif |
| ------- | ------- | ------- | ------- | ------- |
| **Appuyer**              | Une personne appuie sur le bouton central | Un bécher vide apparaît au centre de la projection du laboratoire | Son de démarrage, ambiance de laboratoire s'active | Le système initialise la session et active les quatre stations  |
| **Doser (Eau)** | L'erlenmeyer est agité (accéléromètre détecte le mouvement) | Une main virtuelle verse de l'eau dans le bécher, le niveau monte selon l'intensité de l'agitation | Son d'eau versée, proportionnel à l'intensité | Le système enregistre le niveau d'eau ajouté à la potion |
| **Doser (Feu)** | Le knob du brûleur est tourné | Le feu sous le bécher s'intensifie selon l'angle du knob, les LEDs physiques s'allument en conséquence | Son de flamme crépitante, intensité variable | Le système calcule l'impact thermique sur la potion |
| **Doser (Poudres)** | L'un des 3 knobs de poudre est tourné | Un flux continu de poudre colorée (bleue/verte/rose) tombe dans le bécher, intensité selon le knob | Son de poudre versée, tonalité différente par couleur | Le système enregistre le type et la quantité de poudre ajoutée |
| **Brasser** | Le joystick est manipulé | La potion tourbillonne dans le bécher selon la direction et l'intensité du joystick | Son de brassage liquide | Le système mélange virtuellement les ingrédients |
| **Expérimenter** | Les participants manipulent librement leurs stations | La potion change de couleur, de viscosité et d'apparence selon les combinaisons d'ingrédients | Harmonies sonores se superposent selon les dosages | Passage automatique à la Phase 2 après 2 minutes |

#### Phase 2 : Alchimie avec Défis (2-8 min)
 
| Verbe action | Condition de déclenchement | Effet visuel | Effet sonore | Effet interactif |
| ------- | ------- | ------- | ------- | ------- |
| **Événement: Évaporation** | Déclenché aléatoirement après 1-2 min de calme | Le niveau du liquide dans le bécher diminue rapidement, vapeur s'élève | Son d'évaporation intense, sifflement | La personne à la station Eau doit agiter frénétiquement l'erlenmeyer pour compenser pendant 45 secondes |
| **Événement: Flamme instable**  | Déclenché aléatoirement après 1-2 min de calme | Le feu devient chaotique et irrégulier, flammes dansent de manière erratique | Son de flammes instables, crépitements agressifs | La personne au Feu doit ajuster le knob en rythme précis pour stabiliser pendant 45 secondes |
| **Événement: Flamme faible**  | Déclenché aléatoirement après 1-2 min de calme | Le feu diminue drastiquement, devient presque éteint, LEDs faiblissent | Son de flamme mourante, grave et inquiétant | La personne au Feu doit tourner le knob au maximum immédiatement pour maintenir pendant 25 secondes |
| **Événement: Gel** | Déclenché aléatoirement après 1-2 min de calme | Tous les ingrédients se figent dans le bécher, cristaux de glace apparaissent, tout devient bleu glacé | Son de gel, ambiance hivernale intense | TOUS les participants doivent manipuler frénétiquement leurs stations simultanément pour dégeler pendant 45 secondes |
| **Collaborer** | Les participants s'entraident pendant les événements | Les autres stations ralentissent ou accélèrent pour aider celui en difficulté | Encouragements sonores, harmonies se stabilisent | Le système favorise la survie de la potion si les participants coordonnent leurs actions |
| **Ajuster** | Entre les événements (1 min de calme) | Les participants peuvent réajuster leurs dosages librement | Retour à l'ambiance calme du laboratoire | Le système permet la correction de l'équilibre avant le prochain événement |
| **Échouer** | Déséquilibre critique (trop de liquide, trop de feu, etc.) | La potion explose violemment, éclairs, projection de liquide virtuel | Son d'explosion dramatique | Retour immédiat à la Phase 1, session réinitialisée |

 
#### Phase 3 : Résultat Final (après avoir survécu aux 4 événements)
 
| Verbe action | Condition de déclenchement | Effet visuel | Effet sonore | Effet interactif |
| ------- | ------- | ------- | ------- | ------- |
| **Stabiliser** | Les 4 événements sont passés, l'équilibre est maintenu pendant ~30 secondes | La potion brille intensément, stabilisée dans une couleur finale révélatrice | Crescendo musical, tension positive | Le système calcule le type de potion selon les proportions finales |
| **Révéler (Explosive)** | Proportions: Trop de feu + peu de liquide | Narration: "Votre collaboration a révélé un nouveau composé: [Nom], aux propriétés explosives." Fenêtre du labo: explosions dehors, ciel rouge, décor tremble | Son d'explosions lointaines, grondements | Les participants observent le résultat de leur collaboration chaotique |
| **Révéler (Curative)** | Proportions: Équilibre harmonieux liquide/poudres | Narration: "Votre collaboration a révélé un nouveau composé: [Nom], aux propriétés curatives." Fenêtre du labo: papillons, cœurs et fleurs apparaissent | Musique douce, sons de nature apaisants | Les participants observent le résultat de leur collaboration équilibrée |
| **Révéler (Toxique)** | Proportions: Excès de poudres + peu de liquide | Narration: "Votre collaboration a révélé un nouveau composé: [Nom], aux propriétés toxiques." Fenêtre du labo: gaz vert, têtes de mort apparaissent | Sons inquiétants, ambiance sombre | Les participants observent le résultat de leur collaboration déséquilibrée |
| **Révéler (Magique)** | Proportions: Beaucoup de liquide + peu de feu + brassage intense | Narration: "Votre collaboration a révélé un nouveau composé: [Nom], aux propriétés magiques." Fenêtre du labo: objets flottent, monde se retourne | Musique féerique, sons mystiques | Les participants observent le résultat de leur collaboration harmonieuse |

#### Phase 4 : Retour au Départ
 
| Verbe action | Condition de déclenchement | Effet visuel | Effet sonore | Effet interactif |
| ------- | ------- | ------- | ------- | ------- |
| **Dissiper** | Après ~15 secondes d'affichage du résultat | L'effet visuel par la fenêtre s'estompe progressivement, la potion dans le bécher se dissipe | Les sons s'éteignent doucement, retour au silence | Le système prépare la réinitialisation |
| **Réinitialiser** | La potion a complètement disparu | Le bécher disparaît, retour à la scène initiale du laboratoire vide avec le bouton central | Silence, attente d'une nouvelle session | Les stations se désactivent, prêtes pour un nouveau groupe de participants |


## Équipements requis
#### Audio
- 2 haut-parleurs actifs de 5"
- 2 fils XLR 3 conducteurs de 15'
- Carte de son multi-sorties + adaptateur powerCON
 
#### Vidéo
- 2 projecteurs Epson PowerLite 990U
- 1 câble HDMI
 
#### Lumière
- 4 lumières LED RGBAW DMX (une par station)
- 4 fils XLR 3 conducteurs de 20'
- 1 Interface DMX Via XLR
- LEDs programmables pour le brûleur (station Feu) // À_PRÉCISER

#### Électricité
- 4 extensions électriques
 
#### Réseau
- 3 câbles ethernet
- 2 transmetteurs et 2 récepteurs (pour projection)

#### Ordinateurs
- 1 ordinateur portable (avec cable alimentation)

#### Matériaux de fabrication
- Bois (pour structure de table et supports)
- Peinture noire mate
- Visserie et quincaillerie
- Tissus bleu pour erlenmeyer
- Matériaux pour boîtiers (stations Feu et Poudres) 

#### Capteurs et contrôleurs
- 1 accéléromètre (station Eau)
- 4 potentiomètres rotatifs (knobs)
- 1 joystick analogique (station Tourbillon)
- 1 M5Stack Atom pour transmission de données
- 1 bouton central lumineux
- Câblage et connecteurs // À_PRÉCISER

#### Objets physiques
- 1 erlenmeyer vide
- 1 agitateur magnétique réel
- Réceptacle fermé pour eau (agitateur)

## Logiciels Requis
#### Environnement de programmation
- Visual Studio Code / PlatformIO / Arduino IDE (Programmation des capteurs: accéléromètre, knobs, joystick)
- Unity 3D (Scène globale, réception données)
#### Design graphique / Effets visuels
- After Effects (Effets de particules pré-rendus au besoin)
- Photoshop (Textures pour le laboratoire 3D)
- Blender/Maya (Modélisation 3D)
#### Gestion de l'éclairage
- QLC+ (Éclairage)
#### Audio
- Reaper / FL Studio (Composition et design sonore)
- Synthétiseurs VST (Sons de laboratoire, événements)

## Synoptique // À_FAIRE
![Plan de branchements // À_FAIRE](_synoptique.svg)

## Plan d'implémentation // À_FAIRE
![Planification de l'espace - perspective 2D // À_FAIRE](_2d_plan.webp)
![Planification de l'espace - perspective 3D // À_FAIRE](_3d_plan1.webp)
![Planification de l'espace - perspective 3D (vue table) // À_FAIRE](_3d_plan2.webp)
![Planification de l'espace - perspective 3D (vue projection) // À_FAIRE](_3d_plan3.webp)

## Budget estimé // À_PRÉCISER

| Objet| Description | Prix | URL/Provenance |
| ------ | ------ | ------ | ------ |
| Erlenmeyer (250ml) | Récipient en verre pour station Eau | 15$ | [Amazon](https://www.amazon.ca/dp/B01N5R7SKK) |
| Accéléromètre MPU6050 | Capteur de mouvement pour détecter l'agitation de l'erlenmeyer | 8$ | [Amazon](https://www.amazon.ca/dp/B08T1WZNT2) |
| Tissus bleu (1m) | Tissu pour simuler l'eau dans l'erlenmeyer et cacher l'accéléromètre | 10$ | [Fabricville](https://www.fabricville.com/) |
| Potentiomètres rotatifs (x5) | Knobs pour contrôle du feu et des poudres | 25$ (5$/unité) | [Amazon](https://www.amazon.ca/dp/B07S1JWG5P) |
| LEDs programmables RGB (bande 1m) | Pour simuler le feu réel dans le brûleur | 20$ | [Amazon](https://www.amazon.ca/dp/B01LSF4Q0A) |
| Joystick analogique | Contrôleur pour le brassage/tourbillon | 12$ | [Amazon](https://www.amazon.ca/dp/B07CKVD4R5) |
| M5Stack Atom | Microcontrôleur pour transmission de données des capteurs | 35$ | [RobotShop](https://www.robotshop.com/ca/fr/) |
| Agitateur magnétique | Vrai agitateur pour effet visuel physique | 40$ | [Amazon](https://www.amazon.ca/dp/B07FKTZC1F) |
| Bouton central lumineux | Bouton de démarrage de l'expérience | 15$ | [Amazon](https://www.amazon.ca/dp/B07R2S77M9) |
| Bois MDF / Contreplaqué | Pour construire les boîtiers des stations et la table | 80$ (~20$/panneau) | [Rona](https://www.rona.ca/) |
| Peinture noire mate | Pour peinturer les structures et le joystick | 35$/950ml | [HomeDepot](https://www.homedepot.ca/produit/rust-oleum-painter-s-touch-peinture-multi-usages-en-noir-mat-946-ml/1000155179) |
| Pinceaux et outils | Pour assemblage et peinture | 20$ | [HomeDepot](https://www.homedepot.ca/) |
| Visserie et quincaillerie | Vis, écrous, supports pour assemblage | 25$ | [Rona](https://www.rona.ca/) |
| Câblage électronique | Fils, connecteurs, breadboards | 30$ | [Amazon](https://www.amazon.ca/) |
| Réceptacle hermétique | Contenant pour l'eau de l'agitateur magnétique | 10$ | [Dollarama](https://www.dollarama.com/) |
|  |  |  | |
| **Total estimé** | | **~380$** | |