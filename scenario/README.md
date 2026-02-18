# Scénarisation de l'interactivité

Cette section présente le scénario de l'interactivité du projet Symbiose.

---

## Scène 0 : Découverte

| Verbe action | Condition de déclenchement | Effet visuel | Effet sonore | Effet interactif |
|---|---|---|---|---|
| **Observer** | Les participants arrivent devant l'installation | Projection du laboratoire 3D avec bécher vide au centre. Faisceau lumineux illumine uniquement la station Eau. Checklist projetée : "☐ 1. Verser de l'eau" | Ambiance de laboratoire calme, sons ambiants discrets | Le système attend l'interaction avec la station Eau. Les autres stations restent inactives |

**Déclencheur suivant** : → Passe à **Scène 1** dès qu'un participant agite l'erlenmeyer à la station Eau

---

## Scène 1 : Tutoriel – Station Eau

| Verbe action | Condition de déclenchement | Effet visuel | Effet sonore | Effet interactif |
|---|---|---|---|---|
| **Verser** | L'erlenmeyer est agité (accéléromètre détecte le mouvement) | Main virtuelle verse l'eau dans le bécher, niveau monte. Jauge verticale + zone cible mobile apparaissent. "✓ 1. Verser de l'eau" se coche. Faisceau lumineux vers station Feu. "☐ 2. Allumer le feu" | Son d'eau versée + Note de validation musicale | Station Feu débloquée. Le timer global démarre |

**Déclencheur suivant** : → Passe à **Scène 2** dès que le knob du brûleur est tourné

---

## Scène 2 : Tutoriel – Station Feu

| Verbe action | Condition de déclenchement | Effet visuel | Effet sonore | Effet interactif |
|---|---|---|---|---|
| **Tourner** | Le knob est tourné (potentiomètre détecte la rotation) | Flammes animées sous le bécher. LEDs physiques s'illuminent. Knob circulaire + zone cible mobile apparaissent. "✓ 2. Allumer le feu" se coche. Faisceau vers station Poudres. "☐ 3. Ajouter des poudres" | Flamme crépitante + Note de validation musicale | Station Poudres débloquée |

**Déclencheur suivant** : → Passe à **Scène 3** dès qu'un bouton de poudre est appuyé

---

## Scène 3 : Tutoriel – Station Poudres

| Verbe action | Condition de déclenchement | Effet visuel | Effet sonore | Effet interactif |
|---|---|---|---|---|
| **Appuyer** | Un bouton de poudre est appuyé | Flux de poudre colorée tombe dans le bécher. Cercle coloré + chronomètre apparaissent. "✓ 3. Ajouter des poudres" se coche. Faisceau vers station Tourbillon. "☐ 4. Brasser la potion" | Son de poudre versée + Note de validation musicale | Station Tourbillon débloquée |

**Déclencheur suivant** : → Passe à **Scène 4** dès que le joystick est manipulé

---

## Scène 4 : Tutoriel – Station Tourbillon

| Verbe action | Condition de déclenchement | Effet visuel | Effet sonore | Effet interactif |
|---|---|---|---|---|
| **Basculer** | Le joystick est manipulé dans n'importe quelle direction | La potion tourbillonne. Flèche directionnelle rotative apparaît. "✓ 4. Brasser la potion" se coche. Tous les faisceaux s'éteignent. Message : "Tutoriel terminé ! La partie commence dans 10 secondes…" + compte à rebours | Son de brassage liquide + Accord de succès musical | Les 4 stations actives simultanément. La checklist disparaît progressivement |

**Déclencheur suivant** : → Passe à **Scène 5** automatiquement après 10 secondes

---

## Scène 5 : Phase principale – Manipulations continues

| Verbe action | Condition de déclenchement | Effet visuel | Effet sonore | Effet interactif |
|---|---|---|---|---|
| **Maintenir** | Démarrage de la phase principale | Interface divisée en 4 colonnes actives simultanément. Jauge de stabilité globale visible en haut de l'écran | Ambiance musicale de tension légère, évoluant avec le temps | Chaque station exige une manipulation continue indépendante |
| **Agiter** | En continu – Station Eau | Jauge verticale + zone cible mobile (haut/milieu/bas). Indicateur vert si dans la zone, rouge si hors zone | Son d'eau rythmique selon intensité | Maintenir l'erlenmeyer agité pour garder le niveau dans la zone cible |
| **Tourner** | En continu – Station Feu | Knob circulaire + zone cible mobile en rotation. Indicateur vert = équilibre, rouge = danger | Son de flamme modulé selon la position | Suivre la position cible avec le knob pour maintenir la chaleur |
| **Appuyer** | En continu – Station Poudres | Cercle coloré (Bleu/Vert/Rose) + chronomètre visible. Succès = nouvelle couleur, échec = danger | Son de poudre + bip d'alerte si raté | Appuyer sur le bouton correspondant à la couleur affichée avant la fin du chrono |
| **Orienter** | En continu – Station Tourbillon | Flèche directionnelle rotative. Indicateur vert = aligné, rouge = désaligné | Son de tourbillon modulé selon l'alignement | Orienter le joystick dans la direction de la flèche affichée |
| **Négliger** | Une station dépasse son seuil d'échec (mauvaise zone, mauvais bouton, mauvaise direction) | Colonne concernée clignote rouge. Jauge de stabilité globale descend progressivement | Son d'alerte grave | La stabilité globale diminue. Si elle atteint 0% → Scène 7 |

**Déclencheur suivant** : → Passe à **Scène 6** dès qu'un événement aléatoire se déclenche (après 10 secondes de phase principale, puis fréquence croissante)

---

## Scène 6 : Événement aléatoire

| Verbe action | Condition de déclenchement | Effet visuel | Effet sonore | Effet interactif |
|---|---|---|---|---|
| **Réagir** | Déclenchement aléatoire sur une station ciblée | Flash rouge sur la colonne concernée. Jauge de l'événement apparaît. Visuel spécifique sur la potion et la fenêtre du laboratoire. Les 3 autres colonnes restent actives normalement | Alerte sonore dramatique + Son spécifique à l'événement | Seule la station ciblée résout l'événement. Les 3 autres stations maintiennent leurs manipulations continues sans interruption |
| **Résoudre** | Le participant exécute l'action requise à la station ciblée (voir détails ci-dessous) | Jauge de l'événement se remplit graduellement. Le visuel de crise diminue proportionnellement | Feedback sonore positif progressif (notes ascendantes) | Chaque action correcte fait progresser la résolution |
| **Négliger** | Inactivité de 30+ secondes à la station ciblée OU manipulation continue échouée sur une autre station | Jauge de stabilité globale descend rapidement | Son d'alarme continu | La stabilité diminue. Si elle atteint 0% → Scène 7 |
| **Compléter** | Jauge de l'événement atteint 100% | Flash vert de succès. La potion revient à un état stable. Colonne redevient normale | Accord de victoire + son de résolution | L'événement est résolu. Les 4 stations reprennent leurs manipulations continues normalement |

**Déclencheur suivant** : → Retourne à **Scène 5** après résolution (un nouvel événement se déclenchera selon la fréquence en cours)

**Déclencheur échec** : → Passe à **Scène 7** si la stabilité globale atteint 0%

---

## Détails des événements (Scène 6)

### Événement : Évaporation (Station Eau)

| Verbe action | Condition de déclenchement | Effet visuel | Effet sonore | Effet interactif |
|---|---|---|---|---|
| **Agiter frénétiquement** | Événement Évaporation déclenché | Liquide disparaît progressivement (transparence accrue). Brouillard dense à la fenêtre. Jauge "Niveau d'eau" + indicateur de rythme apparaissent | Sifflement d'évaporation + alerte sonore | L'accéléromètre détecte l'intensité du mouvement |
| **Maintenir le rythme** | Erlenmeyer agité avec vigueur et régularité | Jauge se remplit selon l'intensité et la constance. L'eau est progressivement restituée dans le bécher | Son d'eau versée continu + feedback positif rythmique | Chaque agitation compte pour remplir la jauge |
| **Compléter** | Jauge atteint 100% | Niveau d'eau revient à la normale. Effets visuels de crise disparaissent. Flash vert | Accord de résolution | Événement résolu |

---

### Événement : Cristallisation (Station Poudres)

| Verbe action | Condition de déclenchement | Effet visuel | Effet sonore | Effet interactif |
|---|---|---|---|---|
| **Enchaîner** | Événement Cristallisation déclenché | Poudres cristallisées dans la potion, couches colorées séparées. Brouillard coloré (bleu/vert/rose) à la fenêtre. Jauge "Mélange homogène" + pattern Bleu→Vert→Rose affiché | Craquements de cristallisation + alerte sonore | Les boutons détectent la séquence |
| **Suivre le pattern** | Boutons appuyés dans l'ordre : Bleu→Vert→Rose, répété | Jauge progresse à chaque cycle correct. Couches colorées se mélangent progressivement | Sons de poudres + rythme musical qui s'accélère + feedback positif par cycle | Le système valide la séquence et suit la progression |
| **Compléter** | 5 à 7 cycles corrects complétés | Potion redevient homogène et liquide. Flash vert | Accord de résolution harmonieux | Événement résolu |

---

### Événement : Gel (Station Feu)

| Verbe action | Condition de déclenchement | Effet visuel | Effet sonore | Effet interactif |
|---|---|---|---|---|
| **Tourner au maximum** | Événement Gel déclenché | Cristaux de glace sur les parois du bécher. Potion solidifiée, teinte bleutée. Tempête de neige à la fenêtre avec givre. Jauge "Température" + indicateur d'intensité apparaissent | Sons de gel (craquements glacés) + vent froid + alerte sonore | Le potentiomètre détecte la position maximale |
| **Maintenir le pattern** | Knob tourné au maximum + pattern rythmique (max→min→max) | Flammes hautes sous le bécher. Glace fond progressivement. Jauge se remplit selon l'intensité maintenue | Son de feu intense + pattern rythmique de réchauffement + feedback positif | Chaque cycle du pattern fait progresser le dégel |
| **Compléter** | Jauge atteint 100% | Potion redevient liquide. Tourbillon reprend. Flash vert | Accord de résolution chaleureux | Événement résolu |

---

### Événement : Vortex (Station Tourbillon)

| Verbe action | Condition de déclenchement | Effet visuel | Effet sonore | Effet interactif |
|---|---|---|---|---|
| **Basculer inversement** | Événement Vortex déclenché | Potion tourbillonne de façon erratique. Éclaboussures virtuelles. Tornade visible à la fenêtre. Cercle cible + curseur + jauge "Stabilisation" apparaissent | Tourbillon violent + vent intense + alerte sonore | Le joystick doit être maintenu dans le sens inverse du vortex |
| **Stabiliser** | Joystick maintenu dans la zone du cercle cible | Curseur reste dans le cercle. Jauge se remplit graduellement. Tourbillon commence à se calmer | Son de tourbillon qui diminue + feedback positif apaisant | Chaque seconde dans la zone cible fait progresser la stabilisation |
| **Compléter** | Jauge atteint 100% | Vortex se calme. Rotation redevient douce et contrôlée. Flash vert | Accord de résolution serein | Événement résolu |

---

## Scène 7 : Échec

| Verbe action | Condition de déclenchement | Effet visuel | Effet sonore | Effet interactif |
|---|---|---|---|---|
| **Subir** | Jauge de stabilité globale atteint 0% | La potion explose violemment. Éclaboussures virtuelles sur l'écran. Flash rouge intense. Écran d'échec : "LA POTION EST RUINÉE !" + Temps de survie (ex: 4:32) + Événements résolus (ex: 12) + Record absolu (ex: 6:47 – 18 événements) + "Pouvez-vous faire mieux ?" | Explosion dramatique + Musique d'échec | Le timer s'arrête. Toutes les stations se désactivent immédiatement |

**Déclencheur suivant** : → Passe à **Scène 8** automatiquement après 8 secondes

---

## Scène 8 : Réinitialisation

| Verbe action | Condition de déclenchement | Effet visuel | Effet sonore | Effet interactif |
|---|---|---|---|---|
| **Attendre** | 8 secondes après l'affichage d'échec | Écran de résultat disparaît en fondu. La potion se dissipe du bécher. Le laboratoire revient à son état initial vide | Sons s'éteignent doucement. Retour progressif à l'ambiance calme du laboratoire | Toutes les stations se désactivent. Le timer se réinitialise à zéro. Le système retourne à l'état d'attente |

**Déclencheur suivant** : → Retourne à **Scène 0 (Découverte)** automatiquement, prêt pour de nouveaux participants