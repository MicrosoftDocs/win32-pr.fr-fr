---
description: Les fonctions suivantes sont utilisées pour créer, modifier ou dessiner des chemins d’accès.
ms.assetid: 68390601-1542-41dc-bea0-78f6c3318806
title: fonctions de chemin d’accès (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ab85e52392b3e600877f8f5adac08d5de77e873
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118285"
---
# <a name="path-functions-windows-gdi"></a>fonctions de chemin d’accès (Windows GDI)

Les fonctions suivantes sont utilisées pour créer, modifier ou dessiner des chemins d’accès.



| Fonction                                       | Description                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AbortPath**](/windows/desktop/api/Wingdi/nf-wingdi-abortpath)                 | Ferme et ignore tous les chemins d’accès dans le contexte de périphérique spécifié.                                                                                                   |
| [**BeginPath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath)                 | Ouvre un crochet de chemin d’accès dans le contexte de périphérique spécifié.                                                                                                            |
| [**CloseFigure**](/windows/desktop/api/Wingdi/nf-wingdi-closefigure)             | Ferme une figure ouverte dans un chemin d’accès.                                                                                                                                 |
| [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath)                     | Ferme un crochet de tracé et sélectionne le chemin d’accès défini par le crochet dans le contexte de périphérique spécifié.                                                             |
| [**FillPath**](/windows/desktop/api/Wingdi/nf-wingdi-fillpath)                   | Ferme toutes les figures ouvertes dans le chemin d’accès actuel et remplit l’intérieur du tracé à l’aide du pinceau actuel et du mode de remplissage du polygone.                                   |
| [**FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath)             | Transforme toutes les courbes dans le chemin d’accès sélectionné dans le contexte de périphérique (DC) actuel, en transformant chaque courbe en une séquence de lignes.                            |
| [**GetMiterLimit**](/windows/desktop/api/Wingdi/nf-wingdi-getmiterlimit)         | Récupère la limite d’angle pour le contexte de périphérique spécifié.                                                                                                      |
| [**GetPath**](/windows/desktop/api/Wingdi/nf-wingdi-getpath)                     | Récupère les coordonnées qui définissent les points de terminaison de lignes et les points de contrôle des courbes trouvées dans le chemin d’accès sélectionné dans le contexte de périphérique spécifié. |
| [**PathToRegion**](/windows/desktop/api/Wingdi/nf-wingdi-pathtoregion)           | Crée une région à partir du chemin d’accès sélectionné dans le contexte de périphérique spécifié.                                                                               |
| [**SetMiterLimit**](/windows/desktop/api/Wingdi/nf-wingdi-setmiterlimit)         | Définit la limite de la longueur des jointures mitres pour le contexte de périphérique spécifié.                                                                                   |
| [**StrokeAndFillPath**](/windows/desktop/api/Wingdi/nf-wingdi-strokeandfillpath) | Ferme toutes les figures ouvertes dans un tracé, contourne le contour du tracé à l’aide du stylet actuel et remplit son intérieur à l’aide du pinceau actuel.                  |
| [**StrokePath**](/windows/desktop/api/Wingdi/nf-wingdi-strokepath)               | Restitue le chemin d’accès spécifié à l’aide du stylet actuel.                                                                                                             |
| [**WidenPath**](/windows/desktop/api/Wingdi/nf-wingdi-widenpath)                 | Redéfinit le chemin d’accès actuel comme zone qui serait peinte si le tracé était tracé à l’aide du stylet actuellement sélectionné dans le contexte de périphérique donné.            |



 

 

 



