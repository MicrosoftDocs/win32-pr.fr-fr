---
description: Un chemin d’accès est une séquence de primitives graphiques (lignes, rectangles, courbes, texte et autres) qui peuvent être manipulées et dessinées en tant qu’unité unique. Un chemin d’accès peut être divisé en figures ouvertes ou fermées. Une figure peut contenir plusieurs Primitives.
ms.assetid: dbfe8cea-bd9e-43ad-85c8-37cce3ef97a4
title: Génération et dessin de tracés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fe5f1528e58e3df19afbc83bb6acfdc2a6fca19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991376"
---
# <a name="constructing-and-drawing-paths"></a>Génération et dessin de tracés

Un chemin d’accès est une séquence de primitives graphiques (lignes, rectangles, courbes, texte et autres) qui peuvent être manipulées et dessinées en tant qu’unité unique. Un chemin d’accès peut être divisé en *figures* ouvertes ou fermées. Une figure peut contenir plusieurs Primitives.

Vous pouvez dessiner un tracé en appelant la méthode [**Graphics ::D rawpath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) de la classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , et vous pouvez remplir un chemin d’accès en appelant la méthode [**Graphics :: FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) de la classe **Graphics** .

Les rubriques suivantes traitent des chemins plus en détail :

-   [Création de figures à partir de lignes, de courbes et de formes](-gdiplus-creating-figures-from-lines-curves-and-shapes-use.md)
-   [Remplissage des figures ouvertes](-gdiplus-filling-open-figures-use.md)

 

 



