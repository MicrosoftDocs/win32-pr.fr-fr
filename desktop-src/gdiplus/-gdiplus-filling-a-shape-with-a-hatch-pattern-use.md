---
description: 'Un motif hachuré est constitué de deux couleurs : une pour l’arrière-plan et une pour les lignes qui forment le modèle sur l’arrière-plan.'
ms.assetid: 7c2bfe54-3259-40d6-9eb4-1a8ad3dda477
title: Remplissage d’une forme avec un motif hachuré
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b571ab09dc91c037e0cc89a2b107c2f8d253b832b593bb32a169bc970295d41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015099"
---
# <a name="filling-a-shape-with-a-hatch-pattern"></a>Remplissage d’une forme avec un motif hachuré

Un motif hachuré est constitué de deux couleurs : une pour l’arrière-plan et une pour les lignes qui forment le modèle sur l’arrière-plan. Pour remplir une forme fermée avec un modèle hachuré, utilisez un objet [**HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) . L’exemple suivant montre comment remplir une ellipse avec un modèle de hachurage :


```
HatchBrush hBrush(HatchStyleHorizontal, Color(255, 255, 0, 0),
   Color(255, 128, 255, 255));
stat = graphics.FillEllipse(&hBrush, 0, 0, 100, 60);
```



L’illustration suivante montre l’Ellipse remplie.

![illustration d’une Ellipse remplie d’un motif hachuré de lignes horizontales sur un arrière-plan Uni](images/hatch1.png)

Le constructeur [**HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) prend trois arguments : le style de hachurage, la couleur de la ligne hachurée et la couleur de l’arrière-plan. L’argument de style de hachurage peut être n’importe quel élément de l’énumération [**HatchStyle**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-hatchstyle) . Il y a plus de 50 éléments dans l’énumération **HatchStyle** ; quelques-uns de ces éléments sont affichés dans la liste suivante :

-   **HatchStyleHorizontal**
-   **HatchStyleVertical**
-   **HatchStyleForwardDiagonal**
-   **HatchStyleBackwardDiagonal**
-   **HatchStyleCross**
-   **HatchStyleDiagonalCross**

 

 



