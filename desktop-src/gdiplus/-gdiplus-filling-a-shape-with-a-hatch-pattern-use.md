---
description: 'Un motif hachuré est constitué de deux couleurs : une pour l’arrière-plan et une pour les lignes qui forment le modèle sur l’arrière-plan.'
ms.assetid: 7c2bfe54-3259-40d6-9eb4-1a8ad3dda477
title: Remplissage d’une forme avec un motif hachuré
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c37f06c93a6ac66a4a6066874c99b88652a0819
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104987752"
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

 

 



