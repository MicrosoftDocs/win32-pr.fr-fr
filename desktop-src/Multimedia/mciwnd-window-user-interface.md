---
title: Interface utilisateur de la fenêtre MCIWnd
description: Interface utilisateur de la fenêtre MCIWnd
ms.assetid: 422c5acb-bce5-4be2-96ba-5ab7f9dcc826
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c98c0b11b6868828625c6c6e605f005fe842d669
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369164"
---
# <a name="mciwnd-window-user-interface"></a>Interface utilisateur de la fenêtre MCIWnd

MCIWnd fournit des fonctionnalités supplémentaires pour ajuster l’apparence de la fenêtre MCIWnd, personnaliser le comportement de votre application et optimiser les performances de lecture. Les fonctionnalités suivantes sont incluses dans la fenêtre MCIWnd :

-   Une barre d’outils avec des boutons **lire**, **arrêter**, **Enregistrer** et **menu**
-   TrackBar qui contrôle le positionnement dans le contenu de lecture
-   Menu contextuel contenant des commandes courantes
-   Zone de lecture pour les vidéos et autres périphériques qui affichent des images

L’illustration suivante montre l’état initial de la lecture vidéo contrôlée par l’utilisateur. L’exemple de fichier utilisé est CLOCK.AVI.

![Image clock.avi](images/mciwnd1.gif)

La fenêtre MCIWnd comprend une zone de lecture pour les vidéos et autres périphériques qui affichent des images pendant la lecture. MCIWnd omet la zone de lecture des appareils Wave-audio, des séquenceurs MIDI et des autres périphériques qui n’écrivent pas dans l’affichage. L’illustration suivante montre la zone de lecture de la forme d’onde audio.

![image fenêtre MCIWnd](images/mciwnd4.gif)

Le bouton **lecture** se trouve dans le coin inférieur gauche de la fenêtre MCIWnd. Il apparaît lorsque le contenu est arrêté. L’utilisateur peut lire le contenu des manières suivantes :

-   Pour lire le contenu à partir de la position de lecture actuelle, sélectionnez le bouton **lecture** .
-   Pour lire le contenu en plein écran à partir de la position de lecture actuelle, sélectionnez le bouton **lecture** tout en maintenant la touche CTRL enfoncée.
-   Pour lire le contenu en arrière à partir de la position de lecture actuelle, sélectionnez le bouton **lecture** tout en maintenant la touche Maj enfoncée.

Le bouton de **menu** , situé en regard du bouton de **lecture** , active un menu qui permet à l’utilisateur d’ouvrir et de fermer des fichiers AVI (Audio-Video entrelacés) et d’ajuster la taille de l’image, la vitesse de lecture et le volume. (L’utilisateur peut également activer le menu en cliquant sur le bouton droit de la souris chaque fois que le curseur se trouve dans la zone cliente de la fenêtre.) Le menu comprend également des commandes permettant de modifier la configuration de l’appareil actuel, de copier le contenu de lecture dans le presse-papiers et d’émettre des commandes MCI.

Le TrackBar situé à droite du bouton de **menu** représente la durée du contenu de lecture (ou enregistré). Le curseur sur la barre de défilement représente la position de lecture actuelle dans le contenu. Lorsque le curseur est positionné à l’extrémité gauche du TrackBar, la position de lecture actuelle est le début du contenu. L’utilisateur peut se déplacer vers différents emplacements dans le contenu en faisant glisser le curseur sur le TrackBar. Le bouton **arrêter** se trouve dans le coin inférieur gauche de la fenêtre MCIWnd. Il apparaît lorsque le contenu est lu. L’illustration suivante montre la lecture vidéo en cours.

![image de lecture vidéo](images/mciwnd2.gif)

Les contrôles MCIWnd peuvent également inclure un bouton d' **enregistrement** pour les appareils qui peuvent enregistrer. Le bouton **Enregistrer** est marqué d’un cercle rouge et s’affiche uniquement lorsque l’appareil est en capacité d’enregistrer.

> [!Note]  
> La fenêtre de lecture doit être alignée sur une limite de quatre pixels pour obtenir les meilleures performances de lecture vidéo. en général, Windows aligne automatiquement la fenêtre lorsqu’elle est créée. Si un utilisateur déplace ou étire la fenêtre à partir de sa position initiale, la vitesse de lecture de la vidéo peut être réduite de moitié.

 

 

 




