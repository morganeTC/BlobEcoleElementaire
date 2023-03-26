# Mode opératoire
## Présentation
**Cet outil vous accompagne**  - pas à pas - dans **l'analyse des photos de blobs**, afin de fournir les données nécessaires à l'apprentissage du _Machine Learning_. 

L'analyse se déroule en **5 étapes** :

[1. Charger une photo](#Étape-1-charger-une-photo) <br>
[2. Positionner la règle](#Étape-2-positioner-la-règle) <br>
[3. Positionner la boîte de Petri](#Étape-3-positionner-la-boîte-de-petri) <br>
[4. Détourer le blob à main levée](#Étape-4-détourer-le-blob) <br>
[5. Télécharger les fichiers de mesures](#Étape-5-télécharger-les-résultats) <br>
[5'. Fusionner les .csv ](#Étape-539-fusionner-les-csv)

Chaque étape est décrite dans la partie droite du _lab_. Il est possible de revenir à tout moment
en arrière en cliquant sur le titre de l'étape.

C'est parti...

---

## Étape 1 : charger une photo

**Charger une photo** à analyser - située sur l'ordinateur - avec le **bouton "Parcourir..."**.

![](images/file_panel.png)

Une fois la photo chargée, **l'étape 2 est automatiquement activée**.

Mais avant...

> ### Comment zoomer et déplacer la photo
> Pour prendre les mesures avec le plus de précision, il est possible de :
> * **zoomer/dézoomer (agrandir/rétrécir) la photo** avec la molette de la souris
> * **déplacer la photo** : tout en appuyant sur la touche contrôle (le curseur devient des flèches), cliquer sur la photo et la déplacer avec la souris
> 
> La barre de boutons de zoom sur le haut de la page permet d'ajuster l'affichage :
> * ![](images/zoom_in.png) : agrandir la photo
> * ![](images/zoom_out.png) : rétrécir la photo
> * ![](images/zoom_fit.png) : ajuster la photo à l'écran et la repositionner au centre (:sparkles: bien utile si l'on perd la photo de vue)
> * ![](images/zoom_1-1.png) : afficher la photo en taille réelle

Maintenant au travail !

---

## Étape 2 : positioner la règle
Cette étape permet au logiciel de déterminer l'échelle de la photo.

**Déplacer la ligne jaune à l'aide des 2 "poignées"** (petits carrés blancs) à chacune de ses extrémités afin de 
**couvrir 10cm de la règle**. 

![](images/ruler_handles.png)

Pour s'assurer que 10 centimètres sont bien couverts, **les petits points "détrompeurs" doivent tomber sur chaque centimètre**.

![](images/ruler_pokayoke.png)

Si il y a moins de 10cm règle sur la photo, il est possible de modifier la taille à couvrir avec les boutons +/- (en bleu ci-dessous).
Le nombre de détrompeurs sera ajusté.

Pour placer la règle avec plus de précision, utiliser le bouton ![Zoom règle](images/zoom_object.png) (en jaune ci-dessous).

![](images/ruler_panel.png)

Une fois la règle placée, **passer à l'étape suivante en appuyant sur le bouton "Terminé !"** (en vert ci-dessus).

---

## Étape 3 : positionner la boîte de Petri

Tout comme la règle, **placer la boîte de Petri à l'aide des poignées**, et utiliser le bouton ![Zoom boîte de Petri](images/zoom_object.png)
pour la placer avec précision.

![](images/petri_handles.png)

>
>
> Au début on y va à tâtons, mais on prend vite le coup de main.
>
> 

![](images/petri_panel.png)

Une fois la boîte de Petri correctement positionnée, **passer à l'étape suivante en appuyant sur "C'est fini !"**

---

## Étape 4 : détourer le blob

Lors de cette étape, **entourer d'une ligne jaune le blob** (dessiner en maintenant le bouton de la souris pressé).

![](images/blob_draw.png)

>
> **Oh non !** Si près de la fin
>
> ![](https://i.giphy.com/media/JuFwy0zPzd6jC/giphy.webp)
> ![](images/blob_scrambled.png)
> 
> Il est possible de revenir en arrière sur les derniers points du tracé avec le bouton  ![](blob_back_button.png)
> 
> ![](images/blob_back_panel.png)
>

Lorsque l'on a rejoint le point de départ marqué par un carré blanc, **le contour est terminé et colorié en jaune**.

![](images/blob_closed.png)

Le bouton  ![](images/blob_done.png) s'active et permet de **passer à l'étape suivante**.

---

## Étape 5 : télécharger les résultats

![](images/download_panel.png)

**Télécharger les fichiers un à un** avec ![](images/download_button.png).

Les fichiers sont stockés dans le répertoire "Téléchargements" du navigateur.  

> [!NOTE|label:Attention]
> Ces fichiers ne peuvent pas être tout de suite déposés sur l'espace de dépôt des fichiers d'analyse (https://blob.cnrs.fr/).
> 
> En effet, le fichier _.csv_ généré ne contient que les mesures (aire, périmètre, circualirité, etc.) que pour la photo qui vient d'être analysée. 
> Le nom du fichier contient le numéro du blob (par exemple: Results_ConJ1Ex*B3*.csv).
> 
> L'espace de dépôt des analyses n'attend qu'**un seul fichier** _.csv_ **pour toutes** les photos d'une séquence groupe/jour/expérience (par ex.: Results_ConJ1Ex.csv).
> 
> Une étape supplémentaire permet de regrouper les fichiers.

## Étape 5' : fusionner les .csv

> :gift: Pour 5 étapes effectuées une étape offerte !

Un bouton dans l'étape 5 permet d'ouvrir l'outil de fusion des fichiers.

![](images/fusion_button.png)

Une fenêtre comme celle-ci s'affiche :

![](images/fusion_dialog.png)

Pas à pas : 
1. \[encadré en vert] Sélectionner des fichiers à fusionner. Plusieurs fichiers peuvent être sélectionnés à la fois. Ils peuvent être sélectionnés en vrac mêmes s'ils font partie de séquences (groupe/jour/expérience) d'analyse différentes.
2. \[marqué en rouge] Les fichiers sont automatiquement triés et regroupés par séquence (groupe/jour/expérience)
3. \[entouré en jaune] Les fichiers résultats sont téléchargeables avec le bouton ![](images/download_button.png)

Maintenant **les fichiers peuvent être transmis par [la plateforme de dépôt de données](https://blob.cnrs.fr/)**.
