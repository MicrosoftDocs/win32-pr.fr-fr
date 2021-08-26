---
description: Un espace de coordonnées est un espace planaire basé sur le système de coordonnées cartésien.
ms.assetid: 1a232030-8561-4b57-b274-dca0a8b3e3a1
title: Transformation des espaces de coordonnées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27ffaec6a6dab09b841f95f4704048a4145d2b2bd84c232658b2b659d26d37be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965159"
---
# <a name="transformation-of-coordinate-spaces"></a>Transformation des espaces de coordonnées

Un *espace de coordonnées* est un espace planaire basé sur le système de coordonnées cartésien. Ce système fournit un moyen de spécifier l’emplacement de chaque point sur un plan. Il requiert deux axes qui sont perpendiculaires et de longueur égale. L’illustration suivante montre un espace de coordonnées.

![illustration d’un espace de coordonnées, indiquant l’origine, les deux axes et les valeurs maximale et minimale de chaque axe](images/cstrn-07.png)

Le système prend en charge quatre espaces de coordonnées, comme décrit dans le tableau suivant.



| Espace de coordonnées | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| world            | Utilisé éventuellement comme espace de coordonnées de départ pour les transformations de graphiques. Il permet la mise à l’échelle, la translation, la rotation, la déformation et la réflexion. L’espace universel mesure 2 ^ 32 unités de haut par 2 ^ 32 unités de large.                                                                                                                                                                                                                                                                |
| page             | Utilisé comme espace suivant après l’espace universel ou comme espace de départ pour les transformations graphiques. Il définit le mode de mappage. L’espace de page mesure également 2 ^ 32 unités de haut par 2 ^ 32 unités de large.                                                                                                                                                                                                                                                                              |
| device           | Utilisé comme espace suivant après l’espace de la page. Il autorise uniquement la traduction, ce qui garantit que l’espace de l’appareil est mappé à l’emplacement approprié dans l’espace physique de l’appareil. L’espace de l’appareil mesure 2 ^ 27 unités d’une largeur de 2 ^ 27 unités.                                                                                                                                                                                                                                          |
| appareil physique  | Espace (de sortie) final pour les transformations de graphiques. Elle fait généralement référence à la zone cliente de la fenêtre d’application ; Toutefois, il peut également inclure l’intégralité du bureau, une fenêtre complète (y compris le cadre, la barre de titre et la barre de menus) ou une page de papier de l’imprimante ou du traceur, en fonction de la fonction qui a obtenu la poignée du contexte de périphérique. Les dimensions de l’appareil physique varient en fonction des dimensions définies par la technologie d’affichage, d’imprimante ou de traceur. |



 

L’espace de page fonctionne avec l’espace de l’appareil pour fournir aux applications des unités indépendantes du périphérique, telles que des millimètres et des pouces. Cette vue d’ensemble fait référence à l’espace universel et à l’espace de page comme un espace logique.

Pour représenter la sortie sur un appareil physique, le système copie (ou mappe) une zone rectangulaire d’un espace de coordonnées à l’autre à l’aide d’une transformation jusqu’à ce que la sortie apparaisse dans son intégralité sur l’appareil physique. Le mappage commence dans l’espace universel de l’application si l’application a appelé la fonction [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) ; Sinon, le mappage se produit dans l’espace de page. Étant donné que le système copie chaque point de la zone rectangulaire d’un espace à un autre, il applique un algorithme appelé transformation. Une *transformation* modifie (ou transforme) la taille, l’orientation et la forme des objets copiés à partir d’un espace de coordonnées dans un autre. Bien qu’une transformation affecte un objet dans son ensemble, elle est appliquée à chaque point ou à chaque ligne dans l’objet.

L’illustration suivante montre une transformation typique effectuée à l’aide de la fonction [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) .

![Illustration montrant un rectangle qui change la taille et la position telle qu’elle apparaît dans l’espace universel, l’espace de page, l’espace de l’appareil et l’appareil](images/cstrn-08.png)

 

 



