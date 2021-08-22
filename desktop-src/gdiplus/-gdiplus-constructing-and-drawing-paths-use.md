---
description: Un chemin d’accès est une séquence de primitives graphiques (lignes, rectangles, courbes, texte et autres) qui peuvent être manipulées et dessinées en tant qu’unité unique. Un chemin d’accès peut être divisé en figures ouvertes ou fermées. Une figure peut contenir plusieurs Primitives.
ms.assetid: dbfe8cea-bd9e-43ad-85c8-37cce3ef97a4
title: Génération et dessin de tracés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d83608dfacbd75bcbe916c9b5528f4bed7be4ed65713927a65f3823670c93311
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612499"
---
# <a name="constructing-and-drawing-paths"></a>Génération et dessin de tracés

Un chemin d’accès est une séquence de primitives graphiques (lignes, rectangles, courbes, texte et autres) qui peuvent être manipulées et dessinées en tant qu’unité unique. Un chemin d’accès peut être divisé en *figures* ouvertes ou fermées. Une figure peut contenir plusieurs Primitives.

Vous pouvez dessiner un tracé en appelant la méthode [**Graphics ::D rawpath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) de la classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , et vous pouvez remplir un chemin d’accès en appelant la méthode [**Graphics :: FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) de la classe **Graphics** .

Les rubriques suivantes traitent des chemins plus en détail :

-   [Création de figures à partir de lignes, de courbes et de formes](-gdiplus-creating-figures-from-lines-curves-and-shapes-use.md)
-   [Remplissage des figures ouvertes](-gdiplus-filling-open-figures-use.md)

 

 



