# Scénarisation de l'interactivité
 
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


