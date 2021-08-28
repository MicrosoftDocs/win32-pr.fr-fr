---
title: TEXT, élément (Lecteur Windows Media SDK)
description: Élément de texte
ms.assetid: 4523fe7a-a77a-4bf2-9195-3943bff0eb21
keywords:
- habillages Lecteur Windows Media, élément de texte
- habillages, élément de texte
- Élément de texte
- référence pour les apparences, élément de texte
- éléments, texte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 333c0d30393ef4fdeb62061ee58b0c7bd2f3f58bd685945e62c0e8062f22d881
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122849"
---
# <a name="text-element"></a>Élément de texte

L’élément de **texte** fournit un moyen de créer et contrôler l’apparence du texte dans une apparence à l’aide des attributs suivants. Des éléments de **texte** prédéfinis sont également fournis pour des raisons pratiques.

L’élément de **texte** prend en charge les attributs suivants.



| Attribut                                                   | Description                                                                                                 |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [backgroundColor](text-backgroundcolor.md)                 | Spécifie ou récupère la couleur d’arrière-plan du contrôle de texte.                                           |
| [cursor](text-cursor.md)                                   | Spécifie ou récupère une valeur indiquant le curseur qui apparaît lorsque la souris se trouve sur le contrôle de texte.     |
| [disabledBackgroundColor](text-disabledbackgroundcolor.md) | Spécifie ou récupère la couleur d’arrière-plan utilisée pour le contrôle de texte lorsqu’il est désactivé.                  |
| [disabledFontStyle](text-disabledfontstyle.md)             | Spécifie ou récupère le style de police utilisé pour le contrôle de texte lorsqu’il est désactivé.                        |
| [disabledForegroundColor](text-disabledforegroundcolor.md) | Spécifie ou récupère la couleur de texte utilisée lorsque le contrôle de texte est désactivé.                               |
| [fontFace](text-fontface.md)                               | Spécifie ou récupère la police du contrôle de texte.                                                   |
| [fontSize](text-fontsize.md)                               | Spécifie ou récupère la taille de police du contrôle de texte.                                                  |
| [fontSmoothing](text-fontsmoothing.md)                     | Spécifie ou récupère une valeur indiquant si le lissage des polices est activé.                                |
| [fontStyle](text-fontstyle.md)                             | Spécifie ou récupère le style de police pour le contrôle de texte.                                                 |
| [foregroundColor](text-foregroundcolor.md)                 | Spécifie ou récupère la couleur de texte du contrôle de texte.                                                 |
| [hoverBackgroundColor](text-hoverbackgroundcolor.md)       | Spécifie ou récupère la couleur d’arrière-plan utilisée pour le contrôle de texte lorsque le curseur de la souris pointe dessus. |
| [hoverFontStyle](text-hoverfontstyle.md)                   | Spécifie ou récupère le style de police utilisé pour le contrôle de texte lorsque le curseur de la souris pointe dessus.       |
| [hoverForegroundColor](text-hoverforegroundcolor.md)       | Spécifie ou récupère la couleur de texte utilisée pour le contrôle de texte lorsque le curseur de la souris pointe dessus.       |
| [motivation](text-justification.md)                     | Spécifie ou récupère l’alignement du texte dans le contrôle de texte.                                   |
| [défilement](text-scrolling.md)                             | Spécifie ou récupère une valeur indiquant si le texte défile.                                         |
| [scrollingAmount](text-scrollingamount.md)                 | Spécifie ou récupère le nombre de pixels que le texte déplace au cours de chaque mouvement de défilement.             |
| [scrollingDelay](text-scrollingdelay.md)                   | Spécifie ou récupère le délai entre les mouvements de défilement.                                          |
| [scrollingDirection](text-scrollingdirection.md)           | Spécifie ou récupère la direction du texte défilant.                                                 |
| [textWidth](text-textwidth.md)                             | Récupère la largeur en pixels de la chaîne contenue dans l’attribut **value** .                           |
| [Bulle](text-tooltip.md)                                 | Spécifie ou récupère le texte d’info-bulle pour le contrôle de texte.                                               |
| [value](text-value.md)                                     | Spécifie ou récupère le texte affiché dans le contrôle de texte.                                      |
| [wordWrap](text-wordwrap.md)                               | Spécifie ou récupère une valeur indiquant si le retour automatique à la valeur est activé ou désactivé.                     |



 

L’élément de **texte** prend en charge les attributs ambiants et peut implémenter les gestionnaires d’événements ambiants. Pour plus d’informations, consultez [attributs ambiants](ambient-attributes.md) et [gestionnaires d’événements ambiants](ambient-event-handlers.md).

Les éléments de texte prédéfinis sont des éléments de **texte** normaux avec différents paramètres d’attribut communs spécifiés par défaut. Les éléments de texte prédéfinis suivants sont disponibles.



| TEXTE prédéfini                                | Description                                                                                |
|------------------------------------------------|--------------------------------------------------------------------------------------------|
| [CURRENTPOSITIONTEXT](currentpositiontext.md) | Élément de **texte** avec un écouteur intégré pour **Player. Controls. currentPositionString**. |
| [DURATIONTEXT](durationtext.md)               | Élément de **texte** avec un écouteur intégré pour **Player. currentMedia. DurationString**.    |
| [STATUSTEXT](statustext.md)                   | Élément de **texte** avec un écouteur intégré pour **Player. Status**.                         |
| [TRACKNAMETEXT](tracknametext.md)             | Élément de **texte** avec un écouteur intégré pour **Player.currentMedia.Name**.              |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Référence de programmation de l’apparence**](skin-programming-reference.md)
</dt> </dl>

 

 




