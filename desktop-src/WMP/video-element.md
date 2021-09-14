---
title: Élément VIDEO
description: Élément VIDEO
ms.assetid: 817e0d2e-cbc3-4b61-81c0-876104125f39
keywords:
- skins Lecteur Windows Media, élément VIDEO
- Skins, élément VIDEO
- Élément VIDEO
- référence pour les apparences, élément VIDEO
- éléments, vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbd8ab6bd014d2968483120fd1dd98804905faa4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010827"
---
# <a name="video-element"></a>Élément VIDEO

L’élément **Video** permet de manipuler une fenêtre vidéo dans une apparence, en utilisant les attributs et les événements suivants. Un élément **vidéo** prédéfini est également fourni pour des raisons pratiques.

L’élément **Video** prend en charge les attributs suivants.



| Attribut                                            | Description                                                                                                                                                                                                                              |
|------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [backgroundColor](video-backgroundcolor.md)         | Spécifie ou récupère la couleur d’arrière-plan du contrôle Video.                                                                                                                                                                        |
| [cursor](video-cursor.md)                           | Spécifie ou récupère la valeur de curseur utilisée lorsque la souris se trouve sur une zone cliquable de la vidéo.                                                                                                                               |
| [Large](video-fullscreen.md)                   | Spécifie ou récupère une valeur indiquant si la vidéo est affichée en mode plein écran. Ne peut être défini qu’au moment de l’exécution.                                                                                                               |
| [maintainAspectRatio](video-maintainaspectratio.md) | Spécifie ou récupère une valeur indiquant si la vidéo conserve les proportions lors de la tentative d’ajustement de la largeur et de la hauteur définies pour le contrôle.                                                                       |
| [shrinkToFit](video-shrinktofit.md)                 | Spécifie ou récupère une valeur indiquant si la vidéo sera réduite à la largeur et à la hauteur définies pour le contrôle vidéo.                                                                                                           |
| [stretchToFit](video-stretchtofit.md)               | Spécifie ou récupère une valeur indiquant si la vidéo se redimensionnera à la largeur et à la hauteur définies pour le contrôle vidéo.                                                                                                   |
| [Bulle](video-tooltip.md)                         | Spécifie ou récupère le texte d’info-bulle pour la fenêtre vidéo.                                                                                                                                                                            |
| [sans fenêtre](video-windowless.md)                   | Spécifie ou récupère une valeur indiquant si le contrôle vidéo sera fenêtre ou sans fenêtre ; autrement dit, si le rectangle entier du contrôle est visible à tout moment ou s’il peut être coupé. Ne peut être défini qu’au moment de la conception. |
| [focale](video-zoom.md)                               | Spécifie le pourcentage de mise à l’échelle de la vidéo.                                                                                                                                                                                    |



 

L’élément **Video** peut implémenter les gestionnaires d’événements suivants.



| Gestionnaire d'événements                          | Description                                                                  |
|----------------------------------------|------------------------------------------------------------------------------|
| [onvideoend](video-onvideoend.md)     | Gère un événement qui se produit lorsque la vidéo arrête le rendu et est déchargée. |
| [onvideostart](video-onvideostart.md) | Gère un événement qui se produit lorsque la vidéo est chargée et commence à effectuer le rendu.  |



 

L’élément **Video** prend en charge les attributs ambiants et peut implémenter les gestionnaires d’événements ambiants, sauf indication contraire. Pour plus d’informations, consultez [attributs ambiants](ambient-attributes.md) et [gestionnaires d’événements ambiants](ambient-event-handlers.md).

Les éléments vidéo prédéfinis sont des éléments **vidéo** normaux avec divers paramètres d’attribut communs spécifiés par défaut. Les éléments vidéo prédéfinis suivants sont disponibles.



| VIDÉO prédéfinie         | Description                                                |
|--------------------------|------------------------------------------------------------|
| [WMPVIDEO](wmpvideo.md) | Élément **vidéo** qui étire la vidéo lorsqu’elle est redimensionnée. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Référence de programmation de l’apparence**](skin-programming-reference.md)
</dt> </dl>

 

 




