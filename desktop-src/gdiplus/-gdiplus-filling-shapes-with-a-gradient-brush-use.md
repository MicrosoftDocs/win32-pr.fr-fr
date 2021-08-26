---
description: Vous pouvez utiliser un pinceau dégradé pour remplir une forme avec une couleur à variation progressive.
ms.assetid: e37b4c3a-b753-483a-990f-da3bcc70acf5
title: Remplissage de formes à l’aide d’un pinceau dégradé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0d471e9d3e2d7fb6d151d50ab3b5f10212874180b4554769b5c00a552085391
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015049"
---
# <a name="filling-shapes-with-a-gradient-brush"></a>Remplissage de formes à l’aide d’un pinceau dégradé

Vous pouvez utiliser un pinceau dégradé pour remplir une forme avec une couleur à variation progressive. Par exemple, vous pouvez utiliser un dégradé horizontal pour remplir une forme avec une couleur qui change graduellement à mesure que vous vous déplacez du bord gauche de la forme vers le bord droit. Imagine un rectangle avec un bord gauche noir (représenté par les composants rouge, vert et bleu 0, 0, 0) et un bord droit rouge (représenté par 255, 0,0). Si le rectangle a une largeur de 256 pixels, le composant rouge d’un pixel donné sera supérieur au composant rouge du pixel à sa gauche. Le pixel le plus à gauche d’une ligne possède des composants de couleur (0, 0, 0), le deuxième pixel a (1,0), le troisième pixel a (2, 0, 0), et ainsi de suite, jusqu’à ce que vous obteniez le pixel le plus à droite, qui a des composants de couleur (255, 0, 0). Ces valeurs de couleur interpolées composent le dégradé de couleur.

Un dégradé linéaire change de couleur lorsque vous le déplacez horizontalement, verticalement ou parallèlement à une ligne inclinée spécifiée. Un dégradé de tracé change de couleur à mesure que vous dépassez l’intérieur et la limite d’un tracé. Vous pouvez personnaliser les dégradés de tracés pour obtenir un grand nombre d’effets.

GDI+ fournit les classes [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) et [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) , qui héritent toutes deux de la classe [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) .

Les rubriques suivantes traitent des dégradés linéaires et de tracés plus en détail :

-   [Création d’un dégradé linéaire](-gdiplus-creating-a-linear-gradient-use.md)
-   [Création d’un dégradé de tracé](-gdiplus-creating-a-path-gradient-use.md)
-   [Application d’une correction gamma à un dégradé](-gdiplus-applying-gamma-correction-to-a-gradient-use.md)

 

 



