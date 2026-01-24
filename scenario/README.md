# Scénarisation de l'interactivité

Cette section présente le scénario de l'interactivité du projet Symbiose.

---

## Scène 0 : Découverte

| Verbe action | Condition de déclenchement | Effet visuel | Effet sonore | Effet interactif |
|--------------|---------------------------|--------------|--------------|------------------|
| **Observer** | Les participants arrivent devant l'installation | Projection du laboratoire de chimie 3D avec bécher vide au centre. Faisceau lumineux illumine uniquement la station Eau. Checklist projetée : "☐ 1. Verser de l'eau" | Ambiance de laboratoire calme, sons ambiants discrets | Le système attend l'interaction avec la station Eau. Les autres stations restent inactives |

**Déclencheur suivant** : → Passe à **Scène 1** dès qu'un participant agite l'erlenmeyer à la station Eau

---

## Scène 1 : Tutoriel - Station Eau

| Verbe action | Condition de déclenchement | Effet visuel | Effet sonore | Effet interactif |
|--------------|---------------------------|--------------|--------------|------------------|
| **Verser** | L'erlenmeyer est agité (accéléromètre détecte le mouvement) | Main virtuelle verse l'eau dans le bécher, le niveau d'eau monte progressivement. "✓ 1. Verser de l'eau" se coche. Faisceau lumineux se déplace vers la station Feu. "☐ 2. Allumer le feu" apparaît | Son d'eau versée + Note de validation musicale | La station Feu se débloque. Le timer global démarre |

**Déclencheur suivant** : → Passe à **Scène 2** dès que le knob du brûleur est tourné

---

## Scène 2 : Tutoriel - Station Feu

| Verbe action | Condition de déclenchement | Effet visuel | Effet sonore | Effet interactif |
|--------------|---------------------------|--------------|--------------|------------------|
| **Tourner** | Le knob du brûleur est tourné (potentiomètre détecte la rotation) | Le feu s'allume sous le bécher, flammes animées apparaissent. LEDs physiques du brûleur s'illuminent. "✓ 2. Allumer le feu" se coche. Faisceau lumineux se déplace vers la station Poudres. "☐ 3. Ajouter des poudres" apparaît | Flamme crépitante + Note de validation musicale | La station Poudres se débloque |

**Déclencheur suivant** : → Passe à **Scène 3** dès qu'un knob de poudre est tourné

---

## Scène 3 : Tutoriel - Station Poudres

| Verbe action | Condition de déclenchement | Effet visuel | Effet sonore | Effet interactif |
|--------------|---------------------------|--------------|--------------|------------------|
| **Appuyer** | Un (ou plusieurs) des 3 boutons de poudre est appuyé en continu. | Flux de poudre colorée (bleue, verte ou rose selon le knob) tombe dans le bécher. La potion commence à se colorer légèrement. "✓ 3. Ajouter des poudres" se coche. Faisceau lumineux se déplace vers la station Tourbillon. "☐ 4. Brasser la potion" apparaît | Son de poudre versée + Note de validation musicale | La station Tourbillon se débloque |

**Déclencheur suivant** : → Passe à **Scène 4** dès que le joystick est manipulé

---

## Scène 4 : Tutoriel - Station Tourbillon

| Verbe action | Condition de déclenchement | Effet visuel | Effet sonore | Effet interactif |
|--------------|---------------------------|--------------|--------------|------------------|
| **Basculer** | Le joystick est manipulé dans n'importe quelle direction | La potion tourbillonne dans le bécher, effet de rotation visible. "✓ 4. Brasser la potion" se coche. Tous les faisceaux lumineux s'éteignent. Message central apparaît : "Tutoriel terminé ! Les événements commencent dans 10 secondes..." avec compte à rebours | Son de brassage liquide + Accord de succès musical | Les 4 stations deviennent toutes actives simultanément. La checklist disparaît progressivement |

**Déclencheur suivant** : → Passe à **Scène 6** automatiquement après 10 secondes (déclenchement du premier événement aléatoire)

---

## Scène 6 : Événement aléatoire 1

| Verbe action | Condition de déclenchement | Effet visuel | Effet sonore | Effet interactif |
|--------------|---------------------------|--------------|--------------|------------------|
| **Réagir** | 10 secondes après la scène 20 | Un événement aléatoire se déclenche parmi : **Évaporation** (station Eau), **Cristallisation** (station Poudres), **Gel** (station Feu), ou **Vortex** (station Tourbillon). Alerte visuelle : flash rouge, jauge de l'événement apparaît. Visuel spécifique à l'événement sur la potion et la fenêtre du laboratoire | Alerte sonore dramatique + Son spécifique à l'événement (ex: sifflement pour évaporation, craquements pour cristallisation) | Seule la station concernée peut résoudre l'événement. Les 3 autres stations restent actives mais n'influencent pas directement la résolution |
| **Résoudre** | Le participant à la station concernée exécute l'action requise (voir détails ci-dessous) | La jauge de progression de l'événement se remplit graduellement. Le visuel de crise diminue proportionnellement | Feedback sonore positif progressif (notes ascendantes, sons apaisants) | Chaque action correcte fait progresser la résolution. Les autres participants peuvent surveiller et encourager |
| **Maintenir** | Le participant continue l'action requise jusqu'à ce que la jauge soit pleine | La jauge atteint 100%. L'événement se résout complètement. Flash vert de succès. La potion revient à un état stable | Accord de victoire + Son de résolution | L'événement est résolu. Transition vers le prochain événement après 20 secondes |

**Déclencheur suivant** : → Passe à **Scène 7** automatiquement 20 secondes après résolution de l'événement

**Déclencheur échec** : → Passe à **Scène 11 (Échec)** si inactivité prolongée (30 secondes sans action) ou si stabilité globale atteint zéro

---

## Scène 7 : Événement aléatoire 2

| Verbe action | Condition de déclenchement | Effet visuel | Effet sonore | Effet interactif |
|--------------|---------------------------|--------------|--------------|------------------|
| **Réagir** | 20 secondes après résolution de l'événement 1 | Deuxième événement aléatoire se déclenche (parmi les 3 événements restants non utilisés). Alerte visuelle et jauge apparaissent | Alerte sonore + Son spécifique au nouvel événement | Seule la nouvelle station concernée peut résoudre |
| **Résoudre** | Action spécifique à l'événement (voir détails ci-dessous) | Jauge se remplit, visuel de crise diminue | Feedback positif progressif | Progression vers résolution |
| **Maintenir** | Action continue jusqu'à jauge pleine | Flash vert de succès, événement résolu | Accord de victoire | Événement résolu |

**Déclencheur suivant** : → Passe à **Scène 8** automatiquement 20 secondes après résolution

**Déclencheur échec** : → Passe à **Scène 11 (Échec)** si échec de résolution

---

## Scène 8 : Événement aléatoire 3

| Verbe action | Condition de déclenchement | Effet visuel | Effet sonore | Effet interactif |
|--------------|---------------------------|--------------|--------------|------------------|
| **Réagir** | 20 secondes après résolution de l'événement 2 | Troisième événement aléatoire se déclenche (parmi les 2 événements restants). Alerte visuelle et jauge | Alerte sonore + Son spécifique | Seule la station concernée peut résoudre |
| **Résoudre** | Action spécifique à l'événement | Jauge se remplit, visuel diminue | Feedback positif | Progression |
| **Maintenir** | Action continue jusqu'à résolution | Flash vert, événement résolu | Accord de victoire | Événement résolu |

**Déclencheur suivant** : → Passe à **Scène 9** automatiquement 20 secondes après résolution

**Déclencheur échec** : → Passe à **Scène 11 (Échec)** si échec

---

## Scène 9 : Événement aléatoire 4 (Final)

| Verbe action | Condition de déclenchement | Effet visuel | Effet sonore | Effet interactif |
|--------------|---------------------------|--------------|--------------|------------------|
| **Réagir** | 20 secondes après résolution de l'événement 3 | Quatrième et dernier événement se déclenche. Alerte visuelle intense, jauge apparaît | Alerte finale dramatique + Son spécifique + Tension musicale accrue | Dernière station concernée doit résoudre |
| **Résoudre** | Action spécifique au dernier événement | Jauge se remplit, tension visuelle maximale puis diminue | Feedback positif + Crescendo musical | Approche de la victoire |
| **Maintenir** | Action continue jusqu'à résolution complète | Flash vert éclatant, tous les événements sont résolus. La potion brille intensément, effet de stabilisation spectaculaire | Crescendo musical victorieux culminant | Les 4 événements sont terminés |

**Déclencheur suivant** : → Passe à **Scène 10 (Victoire)** immédiatement après résolution

**Déclencheur échec** : → Passe à **Scène 11 (Échec)** si échec

---

## Scène 10 : Victoire

| Verbe action | Condition de déclenchement | Effet visuel | Effet sonore | Effet interactif |
|--------------|---------------------------|--------------|--------------|------------------|
| **Contempler** | Les 4 événements ont été résolus avec succès | La potion se stabilise, brillant d'une lumière intense. Le timer s'arrête. Écran de victoire s'affiche : "POTION STABILISÉE !" + Temps réalisé (ex: 20:32) + Record absolu (ex: 4:12) + Message : "EXCELLENT TRAVAIL D'ÉQUIPE !" + "Pouvez-vous faire mieux ?" | Thème musical de victoire triomphant | Toutes les stations deviennent inactives. Le timer final est enregistré |

**Déclencheur suivant** : → Passe à **Scène 12 (Réinitialisation)** automatiquement après 120 secondes d'affichage

---

## Scène 11 : Échec

| Verbe action | Condition de déclenchement | Effet visuel | Effet sonore | Effet interactif |
|--------------|---------------------------|--------------|--------------|------------------|
| **Subir** | Inactivité prolongée pendant un événement OU stabilité globale atteint zéro | La potion explose violemment. Éclaboussures virtuelles sur l'écran. Flash rouge intense. Écran d'échec apparaît : "ÉCHEC - La potion s'est ruinée !" + Temps écoulé avant échec (ex: 3:47) + Message : "Réessayez !" | Explosion dramatique + Musique d'échec | Le timer s'arrête. Toutes les stations se désactivent immédiatement |

**Déclencheur suivant** : → Passe à **Scène 12 (Réinitialisation)** automatiquement après 8 secondes

---

## Scène 12 : Réinitialisation

| Verbe action | Condition de déclenchement | Effet visuel | Effet sonore | Effet interactif |
|--------------|---------------------------|--------------|--------------|------------------|
| **Attendre** | Après affichage de victoire (120 sec) ou d'échec (8 sec) | L'écran de résultat disparaît progressivement en fondu. La potion se dissipe du bécher. Le laboratoire revient à son état initial vide. Le bécher redevient transparent et vide | Sons s'éteignent doucement. Retour progressif à l'ambiance calme du laboratoire | Toutes les stations se désactivent. Le timer se réinitialise à zéro. Le système retourne à l'état d'attente |

**Déclencheur suivant** : → Retourne à **Scène 0 (Découverte)** automatiquement, prêt pour de nouveaux participants

---

## Détails des événements (Scènes 6-9)

### Événement : Évaporation (Station Eau)

| Verbe action | Condition de déclenchement | Effet visuel | Effet sonore | Effet interactif |
|--------------|---------------------------|--------------|--------------|------------------|
| **Agiter frénétiquement** | Événement Évaporation déclenché | Le liquide disparaît progressivement de la potion (transparence accrue). Flocons "frosting" dans le décor du laboratoire. Brouillard dense à la fenêtre. Jauge "Niveau d'eau" + Indicateur de rythme d'agitation s'affichent | Sifflement d'évaporation + Son d'alerte | L'accéléromètre détecte l'intensité du mouvement |
| **Maintenir le rythme** | L'erlenmeyer est agité avec vigueur et régularité | La jauge se remplit graduellement selon l'intensité et la constance. L'eau est progressivement reverser dans le bécher | Son d'eau versée continu + Feedback positif rythmique | Chaque agitation compte pour remplir la jauge |
| **Compléter** | Jauge atteint 100% | Le niveau d'eau revient à la normale. Les effets visuels de crise disparaissent. Flash vert | Accord de résolution | Événement résolu |

---

### Événement : Cristallisation (Station Poudres)

| Verbe action | Condition de déclenchement | Effet visuel | Effet sonore | Effet interactif |
|--------------|---------------------------|--------------|--------------|------------------|
| **Tourner en alternance** | Événement Cristallisation déclenché | Les poudres se cristallisent dans la potion, liquide devient dense et rigide, couches colorées visibles et séparées. Couches de brouillard coloré (bleu/vert/rose) à la fenêtre. Jauge "Mélange homogène" + Pattern visuel (Bleu→Vert→Rose) s'affichent | Craquements de cristallisation + Son d'alerte | Les potentiomètres détectent la séquence |
| **Suivre le pattern** | Les 3 boutons sont appuyés dans l'ordre : Bleu → Vert → Rose, et répété | La jauge s'égalise à chaque cycle correct. Les couches colorées commencent à se mélanger progressivement | Sons de poudres + Rythme musical qui s'accélère + Feedback positif à chaque cycle correct | Le système valide la séquence et suit la progression |
| **Compléter** | Jauge atteint 100% après plusieurs cycles | La potion redevient homogène et liquide. Flash vert | Accord de résolution harmonieux | Événement résolu |

---

### Événement : Gel (Station Feu)

| Verbe action | Condition de déclenchement | Effet visuel | Effet sonore | Effet interactif |
|--------------|---------------------------|--------------|--------------|------------------|
| **Tourner au maximum** | Événement Gel déclenché | Cristaux de glace apparaissent sur les parois du bécher. La potion se solidifie, couleur bleutée/blanchâtre. Le tourbillon s'arrête. Flocons "frosting" dans le décor. Tempête de neige à la fenêtre avec givre. Jauge "Température" + Indicateur d'intensité du feu s'affichent | Sons de gel (craquements glacés) + Vent froid + Son d'alerte | Le potentiomètre détecte la position maximale |
| **Maintenir l'intensité** | Le knob est tourné au maximum ET un pattern rythmique est suivi | Flammes très hautes apparaissent sous le bécher. La glace commence à fondre progressivement. Jauge se remplit selon l'intensité maintenue | Son de feu intense + Pattern rythmique de réchauffement + Feedback positif | Le feu intense fait progresser le dégel |
| **Compléter** | Jauge atteint 100% | La potion redevient liquide. Le tourbillon reprend. Flash vert | Accord de résolution chaleureux | Événement résolu |

---

### Événement : Vortex (Station Tourbillon)

| Verbe action | Condition de déclenchement | Effet visuel | Effet sonore | Effet interactif |
|--------------|---------------------------|--------------|--------------|------------------|
| **Basculer inversement** | Événement Vortex déclenché | La potion tourbillonne de façon erratique et chaotique. Éclaboussures virtuelles sur les bords du bécher. Tornade/cyclone visible à la fenêtre. Cercle cible + Curseur + Jauge "Stabilisation du vortex" s'affichent | Tourbillon violent + Vent intense + Son d'alerte | Le joystick doit être manipulé dans le sens inverse |
| **Stabiliser** | Le joystick est maintenu dans la zone du cercle cible | Le curseur reste dans le cercle. La jauge se remplit graduellement. Le tourbillon commence à se calmer | Son de tourbillon qui diminue progressivement + Feedback positif apaisant | Chaque seconde dans la zone cible fait progresser la stabilisation |
| **Compléter** | Jauge atteint 100% | Le vortex se calme complètement. La rotation devient douce et contrôlée. Flash vert | Accord de résolution serein | Événement résolu |