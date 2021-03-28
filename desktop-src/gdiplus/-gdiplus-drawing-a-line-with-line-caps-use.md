---
description: Vous pouvez dessiner le début ou la fin d’une ligne dans l’une des différentes formes appelées lignes d’épaisseur de ligne. Windows GDI+ prend en charge plusieurs extrémités de ligne, telles que l’arrondi, le carré, le losange et la flèche.
ms.assetid: c9d90114-3913-486c-a808-b08dd473d9a1
title: Dessin d’une ligne avec des embouts de ligne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50ee4dd12a3068fe5200e0f1ae786765170ccba7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988306"
---
# <a name="drawing-a-line-with-line-caps"></a>Dessin d’une ligne avec des embouts de ligne

Vous pouvez dessiner le début ou la fin d’une ligne dans l’une des différentes formes appelées lignes d’épaisseur de ligne. Windows GDI+ prend en charge plusieurs extrémités de ligne, telles que l’arrondi, le carré, le losange et la flèche.

Vous pouvez spécifier des extrémités de ligne pour le début d’une ligne (extrémité de début), la fin d’une ligne (extrémité de fin) ou les tirets d’une ligne en pointillés (tirets).

L’exemple suivant dessine une ligne avec une flèche à une extrémité et une extrémité arrondie à l’autre extrémité :


```
Pen pen(Color(255, 0, 0, 255), 8);
stat = pen.SetStartCap(LineCapArrowAnchor);
stat = pen.SetEndCap(LineCapRoundAnchor);
stat = graphics.DrawLine(&pen, 20, 175, 300, 175);
```



L’illustration suivante montre la ligne résultante.

![Illustration montrant une ligne horizontale avec une flèche à l’extrémité gauche et un cercle à l’extrémité droite](images/pens4.png)

**LineCapArrowAnchor** et **LineCapRoundAnchor** sont des éléments de l’énumération [**LineCap**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-linecap) .

 

 



