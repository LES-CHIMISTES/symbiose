# Scénarisation de l'interactivité
 
#### Phase 0 : État initial
| Verbe action | Condition de déclenchement | Effet visuel | Effet sonore | Effet interactif |
| ------- | ------- | ------- | ------- | ------- |
| **Observer**              | Les participants arrivent devant l'installation | Un faisceau lumineux illumine la station Eau, liste de checkboxes sur la projection : "☐ 1. Verser de l'eau" | Ambiance de laboratoire calme, attente | Le système attend l'interaction avec la première station |

#### Phase 1 : Tutoriel progressif (0-2 min)
| Verbe action | Condition de déclenchement | Effet visuel | Effet sonore | Effet interactif |
| ------- | ------- | ------- | ------- | ------- |
| **Verser** | L'erlenmeyer de la station Eau est agité (accéléromètre détecte le mouvement) | Une main virtuelle verse de l'eau dans le bécher, le niveau monte. Checkbox "✓ Verser de l'eau" se coche. Nouveau faisceau illumine la station Feu. Nouvelle checkbox apparaît : "☐ Allumer le feu" | Son d'eau versée, note de validation | Le système débloque la station Feu et enregistre le niveau d'eau |
| **Tourner (Feu)** | Le knob du brûleur est tourné | Le feu s'allume sous le bécher, s'intensifie selon l'angle. Checkbox "✓ Allumer le feu" se coche. Faisceau illumine la station Poudres. Nouvelle checkbox : "☐ Ajouter des poudres" | Son de flamme crépitante, note de validation | Le système débloque la station Poudres et calcule l'impact thermique |
| **Tourner (Poudres)** | L'un des 3 knobs de poudre est tourné | Flux de poudre colorée tombe dans le bécher. Checkbox "✓ Ajouter des poudres" se coche. Faisceau illumine la station Tourbillon. Nouvelle checkbox : "☐ Brasser la potion" | Son de poudre versée, note de validation | Le système débloque la station Tourbillon et enregistre le type/quantité de poudre |
| **Basculer** | Le joystick est manipulé | La potion tourbillonne dans le bécher. Checkbox "✓ Brasser la potion" se coche. Tous les faisceaux s'éteignent. Message : "Tutoriel terminé - Expérimentez librement !" | Son de brassage liquide, accord de succès | Les quatre stations sont maintenant actives simultanément |
<!-- | **Expérimenter** | Les participants manipulent librement toutes leurs stations | La potion change de couleur, viscosité et apparence selon les combinaisons. Les checkboxes disparaissent | Harmonies sonores se superposent selon les dosages | Passage automatique à la Phase 2 après 2 minutes d'expérimentation libre | -->

<!-- #### Phase 2 : Alchimie avec Défis (2-8 min)
 
| Verbe action | Condition de déclenchement | Effet visuel | Effet sonore | Effet interactif |
| ------- | ------- | ------- | ------- | ------- |
| **Réagir** | Un événement aléatoire se déclenche toutes les 1-2 min (Évaporation/Flamme instable/Flamme faible/Gel) | Visuel spécifique selon l'événement : vapeur qui s'élève, flammes erratiques, feu mourant, ou cristaux de glace. Dure 45 secondes | Sons spécifiques : sifflement, crépitements, grondement grave, ou ambiance hivernale | Les participants doivent réagir selon l'événement : agiter frénétiquement (Évaporation), ajuster en rythme (Flamme instable), tourner au max (Flamme faible), ou tous manipuler ensemble (Gel) |
| **Collaborer** | Les participants s'entraident pendant les événements | Les autres stations ralentissent ou accélèrent pour aider celui en difficulté | Encouragements sonores, harmonies se stabilisent | Le système favorise la survie de la potion si les participants coordonnent leurs actions |
| **Ajuster** | Entre les événements (1 min de calme) | Les participants peuvent réajuster leurs dosages librement | Retour à l'ambiance calme du laboratoire | Le système permet la correction de l'équilibre avant le prochain événement |
| **Exploser** | Déséquilibre critique (trop de liquide, trop de feu, etc.) | La potion explose violemment, projection de liquide virtuel | Son d'explosion dramatique | Retour immédiat à la Phase 0, session réinitialisée |

 
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
| **Réinitialiser** | La potion a complètement disparu | Le bécher disparaît, retour à la scène initiale du laboratoire vide avec le bouton central | Silence, attente d'une nouvelle session | Les stations se désactivent, prêtes pour un nouveau groupe de participants | -->