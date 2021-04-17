---
title: Élément VIEW
description: Élément VIEW
ms.assetid: e1dfde08-33a0-4f12-8db0-ad62e4a1d467
keywords:
- Apparences du lecteur Windows Media, élément d’affichage
- Skins, élément VIEW
- Élément VIEW
- informations de référence sur les apparences, l’élément VIEW
- éléments, vue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07e907cced22b4d1cd498054df06ac8677a7488b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380068"
---
# <a name="view-element"></a>Élément VIEW

L’élément **View** contient les détails de l’interface utilisateur d’une apparence et utilise les attributs, les méthodes et les gestionnaires d’événements présentés dans les tableaux suivants.

Plusieurs éléments de **vue** peuvent être définis en tant qu’enfants de l’élément **Theme** d’une apparence pour fournir différentes interfaces pour différentes situations. Les éléments d' **affichage** ne peuvent pas être spécifiés en tant qu’enfants de tout autre élément et ils contiennent tous les autres éléments d’apparence. Notez que chaque vue a sa propre portée variable, ce qui signifie qu’elle ne peut pas partager des valeurs d’attribut avec d’autres vues.

L’attribut global **View** peut être utilisé pour référencer un élément **View** spécifique à partir de n’importe où dans celui-ci. Il s’agit d’une alternative à l’utilisation de son attribut **ID** , qui doit être utilisé à partir d’autres éléments d' **affichage** ou à partir de l’élément de **thème** .

L’élément **View** prend en charge les attributs suivants. Les attributs marqués d’un astérisque ( \* ) sont également pris en charge par l’élément **subview** .



| Attribut                                                       | Description                                                                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [backgroundColor](view-backgroundcolor.md)\*                  | Spécifie ou récupère la couleur d’arrière-plan de la **vue** ou de la sous- **vue**.                                             |
| [backgroundImage](view-backgroundimage.md) \*                  | Spécifie ou récupère l’image d’arrière-plan de la **vue** ou de la sous- **vue**.                                             |
| [backgroundImageHueShift](view-backgroundimagehueshift.md)     | Spécifie ou récupère la valeur de décalage de la teinte de l’image d’arrière-plan.                                  |
| [backgroundImageSaturation](view-backgroundimagesaturation.md) | Spécifie ou récupère la valeur de saturation de l’image d’arrière-plan.                                                    |
| [backgroundTiled](view-backgroundtiled.md)\*                  | Spécifie ou récupère une valeur indiquant si l’image d’arrière-plan de la **vue** ou de la sous- **vue** est affichée en mosaïque.         |
| [category](view-category.md)                                   | Spécifie ou récupère la catégorie pour laquelle l’interface utilisateur s’affiche.                                           |
| [focusObjectID](view-focusobjectid.md)                         | Spécifie ou récupère une valeur indiquant l’élément qui a le focus clavier.                                             |
| [Telle](view-maxheight.md)                                 | Spécifie ou récupère la hauteur maximale de la **vue** lors du redimensionnement.                                                |
| [maxWidth](view-maxwidth.md)                                   | Spécifie ou récupère la largeur maximale de la **vue** lors du redimensionnement.                                                 |
| [minHeight](view-minheight.md)                                 | Spécifie ou récupère la hauteur minimale de la **vue** lors du redimensionnement.                                                |
| [minWidth](view-minwidth.md)                                   | Spécifie ou récupère la largeur minimale de la **vue** lors du redimensionnement.                                                 |
| [redimensionnable](view-resizable.md)                                 | Spécifie ou récupère une valeur indiquant si la **vue** peut être redimensionnée.                                          |
| [resizeBackgroundImage](view-resizebackgroundimage.md)         | Spécifie ou récupère une valeur indiquant si l’image d’arrière-plan peut être redimensionnée.                                  |
| [scriptFile](view-scriptfile.md)                               | Spécifie les noms de fichiers des fichiers JScript associés.                                                                 |
| [timerInterval](view-timerinterval.md)                         | Spécifie ou récupère l’intervalle, en millisecondes, auquel la minuterie déclenche des événements dans le gestionnaire d’événements **OnTimer** . |
| [title](view-title.md)                                         | Spécifie ou récupère le titre de la **vue**. Ne peut être défini qu’au moment de la conception.                                       |
| [Spreadsheet](view-titlebar.md)                                   | Spécifie ou récupère une valeur indiquant si la barre de titre de la fenêtre est affichée.                                        |
| [transparencyColor](view-transparencycolor.md)\*              | Spécifie ou récupère la couleur de transparence de l’image d’arrière-plan.                                                  |



 

L’élément **View** prend en charge les méthodes suivantes.



| Méthode                                              | Description                                                |
|-----------------------------------------------------|------------------------------------------------------------|
| [close](view-close.md)                             | Ferme la **vue**.                                       |
| [valoris](view-maximize.md)                       | Agrandit la **vue**.                                    |
| [icône](view-minimize.md)                       | Réduit la **vue**.                                    |
| [restore](view-restore.md)                         | Restaure la **vue**.                                     |
| [returnToMediaCenter](view-returntomediacenter.md) | Retourne l’utilisateur au mode complet du lecteur Windows Media. |
| [size](view-size.md)                               | Redimensionne la **vue** sur un bord spécifié.                  |



 

L’élément **View** peut implémenter les gestionnaires d’événements suivants.



| Gestionnaire d'événements               | Description                                                                |
|-----------------------------|----------------------------------------------------------------------------|
| [OnClose](view-onclose.md) | Gère un événement qui se produit lorsque la **vue** est sur le point d’être fermée.      |
| [OnError](view-onerror.md) | Gère un événement d’erreur si **Settings. enableErrorDialogs** est défini sur false. |
| [OnLoad](view-onload.md)   | Gère un événement qui se produit lorsque la **vue** est affichée pour la première fois.         |
| [minute](view-ontimer.md) | Gère les événements de minuterie.                                                      |



 

L’élément **View** prend en charge les attributs ambiants et peut implémenter les gestionnaires d’événements ambiants, sauf indication contraire. Pour plus d’informations, consultez [attributs ambiants](ambient-attributes.md) et [gestionnaires d’événements ambiants](ambient-event-handlers.md),

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Référence de programmation de l’apparence**](skin-programming-reference.md)
</dt> </dl>

 

 




