# Ryan Dufault

![Ryan Dufault]( ryan_dufault.webp)


## Planification

Cette section, complétée lors de la première semaine, présente les tâches individuelles **hebdomadaires** prévues.

<!--
- Planification sur 9 semaines (8 semaines de cours et 1 semaine de rattrapage) présentant les tâches individuelles hebdomadaires prévues.
- Au moins une tâche par semaine. Les tâches ne peuvent pas se répéter et doivent être suffisamment précises.
- Les tâches doivent être cohérentes avec celles des autres membres de l’équipe et avec le concept du projet, et être mises à jour en continu.
- Critères :
    - Intention et concept clairs
    - Description approfondie de la conception sonore et visuelle
    - Planification détaillée du contenu multimédia à intégrer
    - Planification technique rigoureuse
-->

### Semaine 1

- Faire la liste de choses à acheter pour les TTP     
- Modifier le budget et la liste d'équipement en conséquence     

### Semaine 2

- Réception de données des capteurs (platformIO / arduino)     
    - réception de données d'accéléromètre      
    - réception de données de sliders/faders (x/y)      
- envoie de données sur Unity      

### Semaine 3

- réception de données des capteurs sur Unity       
- développement c# événement gel    

### Semaine 4

- Cablage en dessous table        
- Déboguage capteurs si lieu
- Prendre mesures pour boîtier poudres    
- Dossier de presse sections :       
    - histoire      
    - description   
    - fonctionnalités         

### Semaine 5

- Tournage trailer        
- développement c# tutoriel progressif

### Semaine 6

- Montage vidéo trailer     
- Mapper le joystick analogique avec le arduino leopard  

### Semaine 6.5

- Animation unity de l’événement gel

### Semaine 7

- Update site complet 
- Mapper lumières selon échec/victoire (sem 5-8)

### Semaine 8

- Contrôle qualité (autre partie)


## Journal de bord

Cette section, complétée **quotidiennement** pendant l’exécution du projet, documente le travail individuel réellement réalisé chaque jour.

<!--
- Une entrée par jour sur 8 semaines (8 semaines à partir de la semaine 2).
   - Un total d'au moins 40 entrées uniques!
- Chaque jour :
    - Documentstion visuelle et/ou sonore du travail effectué
    - Lien vers les billets GitHub résolus
- Démarche rigoureuse de validation de la qualité
- Démonstration d'autonomie.
- Exécution technique précise et complète.
- Évaluation réfléchie de la contribution individuelle au travail d’équipe.
-->

### Semaine 2

#### Lundi
- Liste de choses à acheter pour les TTPs
![Liste d'objets technique du projet, à donner aux TTPs.](s2_lundi.webp)

#### Mardi
- Planification physique et virtuelle de l'espace
![Dessins de planification de l'espace physique et virtuel.](s2_mardi.webp)

#### Mercredi
- Envoie de données des capteurs via ATOM (sans accel/gyro)
![Envoie de données via OSC slip depuis le ATOM sur pure data.](s2_mercredi.webp)

#### Jeudi
- Envoie de données des capteurs via ATOMS3 + patch pure data
![Envoie de données via OSC slip depuis le ATOMS3, pour avoir accès au gyro et accéléromètre en plus des autres units. Patch pure data spécifique pour le projet commencé.](s2_jeudi.webp)

#### Vendredi
- Recevoir les données OSC sur Unity.
![Rotation d'un cube selon données XYZ de l'accéléromètre, données OSC représentées visuellement avec textes.](s2_vendredi.gif)
- Patch Pure Data unique au projet avancé.
![Patch Pure Data amélioré.](s2_vendredi2.webp)

### Semaine 3

#### Lundi
- Capteurs influencent la scène principale. (simple pour maquette #1)
    - L'accéléromètre remplit l'eau au fur et à mesure (scale)
    - L'angle allume le feu/l'éteint progressivement (scale)
    - Les keys changent la couleur du matériau de l'eau (mesh renderer)
    - Les faders rotationnent le bécher (rotation)
![Démonstration visuelle des capteurs qui influencent l'environnement de la scène.](s3_lundi.gif)

#### Mardi
- Développement de l'événement gel (seul événement disponible pour la maquette #1)
    - Démarre 5 secondes après interaction du fader
    - Barre de gel qui descend lorsque le knob est au max
    - Pattern rythmique à suivre pour faire descendre la barre (angle à tel value ainsi de suite)
![Démonstration de l'événement gel.](s3_mardi.gif)

#### Mercredi
- Développement de notion d'échec et de victoire
![Écran d'échec](s3_mercredi.png)
![Écran de victoire](s3_mercredi2.png)

#### Jeudi
- Début d'envoi OSC sur QLC+, ajustements finals pour la maquette #1.
![Liste d'ajustement final](s3_jeudi.png)
![Code C# d'envoi OSC sur QLC+](s3_jeudi2.png)

#### Vendredi
- Début de feedback visuel pour chaque station.
![Disposition en 4 colonnes pour donner l'effet ''split-screen'' pour plus d'immersion.](s3_vendredi.png)

### Semaine 4

#### Lundi
- Clean-up/refactoring du code, supression des bouts de code en lien avec la maquette #1.

#### Mardi
- Avancement du feedback visuel des manipulations continues des stations.
    - L'eau doit atteindre un niveau cible et maintenir son niveau pendant 2 secondes. (Ne marche pas pour l'instant; problème de tolérance/seuil)
    - Le feu doit aussi atteindre une cible et maintenir son intensité pendant 2 secondes.
    - Le bouton correspondant à la couleur du cercle affiché sur l'écran doit être appuyé dans un délai de 2 secondes. (Je vais rajouter une animation de fade out demain pour plus d'intuitivité)
    - Le joystick (faders X/Y pour l'instant) doit faire un rotation dans le sens indiqué de la flèche pendant un X nombre de secondes (anti horaire ou horaire). (Pour l'instant le feedback visuel marche mais pas le système derrière, je vais rajouter un clamp entre 1 et 6 secondes pour le temps de rotation à faire avant le changement de sens de la flèche).
![Démonstration visuelle du début des manipulations continues](s4_mardi.gif)

#### Mercredi
- Finitions du feedback visuel des manipulations continues des stations.
    - L'eau doit atteindre un niveau cible et maintenir son niveau pendant 3.5 secondes.
    - Le feu doit aussi atteindre une cible et maintenir son intensité pendant 2 secondes.
    - Le bouton correspondant à la couleur du cercle affiché sur l'écran doit être appuyé dans un délai de 4 secondes.
    - Le joystick (faders X/Y pour l'instant) doit faire un rotation dans le sens indiqué de la flèche pendant un X nombre de secondes (anti horaire ou horaire).
![Démonstration visuelle de l'avancement des manipulations continues](s4_mercredi.gif)
- Début du tutoriel progressif
- Début du TouchDesigner pour la 2ème projection (projection ultra wide)
![Début du TouchDesigner, pas d'interaction pour l'instant](s4_mercredi.png)
    - Je pense faire en sorte que chaque niveau d'eau atteint (via manip. continue de la station eau) fasse un pulse reset sur le top feedback
    - Que l'angle de la station feu ajoute de la saturation (ou des harmonics du noise, à voir)
    - Que les keys changent la couleur du noise
    - Que le tourbillon change le translate 4D du 2ème noise
    - L'événement évaporation enlève de la saturation (genre complètement)
    - L'événement gel "freeze"/slow le translate 4D du 2ème noise (et donne une teinte bleuté clair)
    - L'événement crystallisation rajoute beaucoup d'harmonics sur les 2 noise (poure donner l'effet de "grain") (je pourrais même rajouter un 3ème noise, à voir)
    - L'événement vortex pourrait accélérer le translate 4D du 2ème noise (et faire un effet de clignotement sur la projection?, à voir)
    - Victoire = saturation boosté
    - Échec = saturation basse
<!-- Finitions du feedback visuel des manipulations continues + Début du tutoriel progressif -->

#### Jeudi
<!-- Tutoriel progressif complété idéalement, acheter les matériaux nécéssaires-->
- J'ai passé la majorité de la journée à debug platformio.
- Après je suis allé acheter le matériel électronique nécéssaire concernant la station tourbillon du projet (celle avec le joystick).


#### Vendredi
<!-- Début structure événements aléatoires -->


### Semaine 5 <!-- Semaine concentrée sur les événements aléatoires, semaine 6 idéalement système de temps, semaine 7+ finitions (ui, ux, etc..)-->

#### Lundi

#### Mardi

#### Mercredi

#### Jeudi

#### Vendredi

### Semaine 6

#### Lundi

#### Mardi

#### Mercredi

#### Jeudi

#### Vendredi

### Semaine 6.5

#### Lundi

#### Mardi

#### Mercredi

#### Jeudi

#### Vendredi

### Semaine 7

#### Lundi

#### Mardi

#### Mercredi

#### Jeudi

#### Vendredi

### Semaine 8

#### Lundi

#### Mardi

#### Mercredi

#### Jeudi

#### Vendredi
                                                   
