---
title: Slider (élément)
description: Slider (élément)
ms.assetid: f1da8987-5430-46ef-b7d7-ac92f34a2185
keywords:
- Apparences du lecteur Windows Media, élément Slider
- apparences, élément Slider
- Slider (élément)
- référence pour les habillages, élément Slider
- éléments, curseur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34607c8706fccc8f416ebc83ae483c98a784c08b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310310"
---
# <a name="slider-element"></a>Slider (élément)

L’élément **Slider** permet de créer et de manipuler un contrôle Slider horizontal ou vertical simple. Il prend en charge les attributs et gestionnaires d’événements suivants. Les éléments **Slider** prédéfinis sont également fournis pour des raisons pratiques.

L’élément **Slider** prend en charge les attributs suivants.



| Attribut                                                 | Description                                                                                                       |
|-----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [backgroundColor](slider-backgroundcolor.md)             | Spécifie ou récupère la couleur d’arrière-plan du contrôle Slider.                                                |
| [backgroundEndColor](slider-backgroundendcolor.md)       | Spécifie ou récupère la couleur de fin d’arrière-plan du contrôle Slider.                                         |
| [backgroundHoverImage](slider-backgroundhoverimage.md)   | Spécifie ou récupère l’image d’arrière-plan du curseur qui s’affiche lorsque vous pointez dessus avec la souris.      |
| [backgroundImage](slider-backgroundimage.md)             | Spécifie ou récupère l’image d’arrière-plan par défaut du curseur.                                                |
| [Bordure](slider-bordersize.md)                       | Spécifie ou récupère la taille de la bordure en pixels.                                                                 |
| [cursor](slider-cursor.md)                               | Spécifie ou récupère une valeur indiquant le type de curseur qui s’affiche lorsque la souris se trouve sur le contrôle Slider. |
| [direction](slider-direction.md)                         | Spécifie ou récupère la direction dans laquelle les images Slider sont disposées.                                             |
| [disabledColor](slider-disabledcolor.md)                 | Spécifie ou récupère la couleur désactivée du contrôle Slider.                                                  |
| [disabledImage](slider-disabledimage.md)                 | Spécifie ou récupère l’image du curseur qui s’affiche lorsque le contrôle est désactivé.                         |
| [foregroundColor](slider-foregroundcolor.md)             | Spécifie ou récupère la couleur de premier plan du contrôle Slider.                                                |
| [foregroundEndColor](slider-foregroundendcolor.md)       | Spécifie ou récupère la couleur de fin de premier plan du contrôle Slider.                                         |
| [foregroundHoverImage](slider-foregroundhoverimage.md)   | Spécifie ou récupère l’image de premier plan du curseur qui s’affiche lorsque vous pointez dessus avec la souris.      |
| [foregroundImage](slider-foregroundimage.md)             | Spécifie ou récupère l’image de premier plan par défaut du curseur.                                                |
| [foregroundProgress](slider-foregroundprogress.md)       | Spécifie ou récupère la position actuelle de la barre de progression en premier plan sous la forme d’un pourcentage de la zone de curseur.    |
| [max](slider-max.md)                                     | Spécifie ou récupère la valeur maximale de la plage définie par le contrôle Slider.                              |
| [min](slider-min.md)                                     | Spécifie ou récupère la valeur minimale de la plage définie par le contrôle Slider.                              |
| [lame](slider-slide.md)                                 | Spécifie ou récupère une valeur indiquant si l’image de premier plan glisse sur l’image d’arrière-plan.          |
| [thumbDisabledImage](slider-thumbdisabledimage.md)       | Spécifie ou récupère l’image de curseur désactivé du contrôle Slider.                                            |
| [thumbDownImage](slider-thumbdownimage.md)               | Spécifie ou récupère l’image représentant l’état inactif du curseur de défilement.                                        |
| [thumbHoverImage](slider-thumbhoverimage.md)             | Spécifie ou récupère l’image du curseur qui s’affiche lorsque vous pointez dessus avec la souris.                  |
| [thumbImage](slider-thumbimage.md)                       | Spécifie ou récupère l’image qui sera utilisée pour représenter la position actuelle du curseur.               |
| [en mosaïque](slider-tiled.md)                                 | Spécifie ou récupère une valeur indiquant si les images de curseur seront en mosaïque.                                |
| [Bulle](slider-tooltip.md)                             | Spécifie ou récupère le texte d’info-bulle pour le contrôle Slider.                                                   |
| [Transparente](slider-transparencycolor.md)         | Spécifie ou récupère la couleur transparente des images de curseur.                                                |
| [useForegroundProgress](slider-useforegroundprogress.md) | Spécifie ou récupère une valeur indiquant si la barre de progression du premier plan sera utilisée.                       |
| [value](slider-value.md)                                 | Spécifie et récupère la position actuelle du curseur.                                                       |



 

L’élément **Slider** peut implémenter les gestionnaires d’événements suivants.



| Gestionnaire d'événements                                   | Description                                                                                                          |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [onDragBegin](slider-ondragbegin.md)           | Gère un événement qui se produit lorsque l’utilisateur clique et maintient le bouton gauche de la souris enfoncé et commence à faire glisser la souris. |
| [onDragEnd](slider-ondragend.md)               | Gère un événement qui se produit lorsque le bouton gauche de la souris est relâché après une opération de glissement.                      |
| [onPositionChange](slider-onpositionchange.md) | Gère un événement qui se produit lorsque la position du curseur change suite à un clic ou un glissement de l’utilisateur.   |



 

L’élément **Slider** prend en charge les attributs ambiants et peut implémenter les gestionnaires d’événements ambiants. Pour plus d’informations, consultez [attributs ambiants](ambient-attributes.md) et [gestionnaires d’événements ambiants](ambient-event-handlers.md).

Les curseurs prédéfinis sont des éléments de **curseur** normaux avec différents paramètres d’attribut communs spécifiés par défaut. Les curseurs prédéfinis suivants sont disponibles.



| CURSEUR prédéfini                  | Description                                                    |
|------------------------------------|----------------------------------------------------------------|
| [BALANCESLIDER](balanceslider.md) | **Curseur** utilisé pour définir l’équilibre audio.                        |
| [SEEKSLIDER](seekslider.md)       | **Curseur** utilisé pour effectuer une recherche sur n’importe quelle position dans un fichier multimédia. |
| [VOLUMESLIDER](volumeslider.md)   | **Curseur** utilisé pour définir le volume audio.                         |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Référence de programmation de l’apparence**](skin-programming-reference.md)
</dt> </dl>

 

 




