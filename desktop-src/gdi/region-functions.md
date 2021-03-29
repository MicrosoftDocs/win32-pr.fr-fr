---
description: Les fonctions suivantes sont utilisées avec les régions.
ms.assetid: 3a42fc7a-4c07-4540-99a7-520f99532f33
title: Fonctions de région (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de0f55549f978dd2868f231b9ff042f6f825459d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972546"
---
# <a name="region-functions-windows-gdi"></a>Fonctions de région (Windows GDI)

Les fonctions suivantes sont utilisées avec les régions.



| Fonction                                                       | Description                                                                                  |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**CombineRgn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn)                               | Combine deux régions et stocke le résultat dans une troisième région.                                |
| [**CreateEllipticRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgn)                 | Crée une région elliptique.                                                                |
| [**CreateEllipticRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgnindirect) | Crée une région elliptique.                                                                |
| [**CreatePolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolygonrgn)                   | Crée une région polygonale.                                                                  |
| [**CreatePolyPolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolypolygonrgn)           | Crée une région composée d’une série de polygones.                                         |
| [**CreateRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgn)                         | Crée une zone rectangulaire.                                                                |
| [**CreateRectRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgnindirect)         | Crée une zone rectangulaire.                                                                |
| [**CreateRoundRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createroundrectrgn)               | Crée une zone rectangulaire avec des angles arrondis.                                           |
| [**EqualRgn**](/windows/desktop/api/Wingdi/nf-wingdi-equalrgn)                                   | Vérifie les deux régions spécifiées pour déterminer si elles sont identiques.                    |
| [**ExtCreateRegion**](/windows/desktop/api/Wingdi/nf-wingdi-extcreateregion)                     | Crée une région à partir de la région et des données de transformation spécifiées.                          |
| [**FillRgn**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn)                                     | Remplit une région à l’aide du pinceau spécifié.                                                 |
| [**FrameRgn**](/windows/desktop/api/Wingdi/nf-wingdi-framergn)                                   | Dessine une bordure autour de la région spécifiée à l’aide du pinceau spécifié.                     |
| [**GetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode)                     | Récupère le mode de remplissage de polygone actuel.                                                     |
| [**GetRegionData**](/windows/desktop/api/Wingdi/nf-wingdi-getregiondata)                         | Remplit la mémoire tampon spécifiée avec des données décrivant une région.                                    |
| [**GetRgnBox**](/windows/desktop/api/Wingdi/nf-wingdi-getrgnbox)                                 | Récupère le rectangle englobant de la région spécifiée.                                    |
| [**InvertRgn**](/windows/desktop/api/Wingdi/nf-wingdi-invertrgn)                                 | Inverse les couleurs dans la région spécifiée.                                                  |
| [**OffsetRgn**](/windows/desktop/api/Wingdi/nf-wingdi-offsetrgn)                                 | Déplace une région selon les décalages spécifiés.                                                     |
| [**PaintRgn**](/windows/desktop/api/Wingdi/nf-wingdi-paintrgn)                                   | Peint la région spécifiée à l’aide du pinceau actuellement sélectionné dans le contexte de périphérique.   |
| [**PtInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion)                               | Détermine si le point spécifié se trouve à l’intérieur de la région spécifiée.                       |
| [**RectInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-rectinregion)                           | Détermine si une partie du rectangle spécifié se trouve dans les limites d’une zone. |
| [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode)                     | Définit le mode de remplissage du polygone pour les fonctions qui remplissent des polygones.                                 |
| [**SetRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-setrectrgn)                               | Convertit une zone en zone rectangulaire avec les coordonnées spécifiées.                  |



 

 

 



