---
description: Les dimensions d’un stylet géométrique sont spécifiées en unités logiques.
ms.assetid: e7030490-d10c-4d1c-87ae-5b4cc4858ee1
title: Stylos géométriques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9725f6440f62458d4c87232400f16e27f9b978ce
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521532"
---
# <a name="geometric-pens"></a>Stylos géométriques

Les dimensions d’un stylet géométrique sont spécifiées en unités logiques. Par conséquent, les lignes dessinées avec un stylet géométrique peuvent être mises à l’échelle, car elles peuvent apparaître plus larges ou plus étroites, selon la transformation universelle actuelle. Pour plus d’informations sur la transformation universelle, consultez [espaces de coordonnées et transformations](coordinate-spaces-and-transformations.md).

Outre les trois attributs partagés avec des plumes cosmétiques (largeur, style et couleur), les plumes géométriques possèdent les quatre attributs suivants : modèle, hachage facultatif, style de fin et style de jointure. Pour plus d’informations sur ces attributs, consultez [Pen Attributes](pen-attributes.md).

Pour créer un stylet géométrique, une application utilise la fonction [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) . Comme avec les plumes cosmétiques, la fonction [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) sélectionne un stylet géométrique dans le contrôleur de l’application.

 

 



