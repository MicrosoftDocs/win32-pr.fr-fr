---
description: Windows GDI+ fournit plusieurs styles de tirets qui sont répertoriés dans l’énumération DashStyle. Si ces styles de tiret standard ne répondent pas à vos besoins, vous pouvez créer un modèle de tiret personnalisé.
ms.assetid: 0e75de3b-1006-4c8f-875c-eeb0782f24b0
title: Dessin d’une ligne en pointillés personnalisée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e108dcd6b32a47befcdd99d1f23e90c33d08446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988025"
---
# <a name="drawing-a-custom-dashed-line"></a>Dessin d’une ligne en pointillés personnalisée

Windows GDI+ fournit plusieurs styles de tirets qui sont répertoriés dans l’énumération [**DashStyle**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-dashstyle) . Si ces styles de tiret standard ne répondent pas à vos besoins, vous pouvez créer un modèle de tiret personnalisé.

Pour dessiner une ligne en pointillés personnalisée, placez les longueurs des tirets et des espaces dans un tableau et transmettez l’adresse du tableau en tant qu’argument à la méthode [**Pen :: SetDashPattern**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setdashpattern) d’un objet [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) . L’exemple suivant dessine une ligne en pointillés personnalisée basée sur le tableau {5, 2, 15, 4}. Si vous multipliez les éléments du tableau par la largeur de stylet 5, vous recevez {25, 10, 75, 20}. Les tirets alternés sont de longueur comprise entre 25 et 75, tandis que les espaces alternent entre 10 et 20.


```
REAL dashValues[4] = {5, 2, 15, 4};
Pen blackPen(Color(255, 0, 0, 0), 5);
blackPen.SetDashPattern(dashValues, 4);
stat = graphics.DrawLine(&blackPen, Point(5, 5), Point(405, 5));
```



L’illustration suivante montre la ligne en pointillés résultante. Notez que le tiret final doit être inférieur à 25 unités pour que la ligne puisse se terminer à (405, 5).

![Illustration montrant une ligne en pointillés ; chaque segment est une ligne abrégée suivie d’une longue](images/pens6.png)

 

 



