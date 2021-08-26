---
description: Une application crée une région en appelant une fonction associée à une forme spécifique. Le tableau suivant indique la ou les fonctions associées à chacune des formes standard.
ms.assetid: e94ae371-8365-4e42-ac8c-04c3928fcffb
title: Création et sélection de régions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75ce2711b2d1ae9dc6641748c72fd586d02e25964102a8c034593d6e60cbaa33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092689"
---
# <a name="region-creation-and-selection"></a>Création et sélection de régions

Une application crée une région en appelant une fonction associée à une forme spécifique. Le tableau suivant indique la ou les fonctions associées à chacune des formes standard.



| Forme                                   | Fonction                                                                                                                         |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| Zone rectangulaire                      | [**CreateRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgn), [**CreateRectRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgnindirect), [**SetRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-setrectrgn) |
| Zone rectangulaire avec angles arrondis | [**CreateRoundRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createroundrectrgn)                                                                                 |
| Région elliptique                       | [**CreateEllipticRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgn), [ **CreateEllipticRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgnindirect)                   |
| Région polygonale                        | [**CreatePolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolygonrgn), [ **CreatePolyPolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolypolygonrgn)                               |



 

Chaque fonction de création de région retourne un handle qui identifie la nouvelle région. Une application peut utiliser ce handle pour sélectionner la région dans un contexte de périphérique en appelant la fonction [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) et en fournissant ce handle comme deuxième argument. Une fois qu’une région est sélectionnée dans un contexte de périphérique, l’application peut effectuer diverses opérations sur celle-ci.

 

 



