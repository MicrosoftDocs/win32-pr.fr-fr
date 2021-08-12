---
description: Windows GDI+ fournit différents niveaux de qualité pour dessiner du texte. En règle générale, un rendu de qualité supérieure prend plus de temps de traitement que le rendu de qualité inférieure.
ms.assetid: 780d97ec-f446-4d19-837f-517a7d6dd27d
title: Anticrénelage avec du texte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9411206351340f58b63196ff880745743ad92325918b112ad2ddb5bcb8591e9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118249923"
---
# <a name="antialiasing-with-text"></a>Anticrénelage avec du texte

Windows GDI+ fournit différents niveaux de qualité pour dessiner du texte. En règle générale, un rendu de qualité supérieure prend plus de temps de traitement que le rendu de qualité inférieure.

Le niveau de qualité est une propriété de la classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Pour définir le niveau de qualité, appelez la méthode [**Graphics :: SetTextRenderingHint**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settextrenderinghint) d’un objet **Graphics** . La méthode **Graphics :: SetTextRenderingHint** reçoit l’un des éléments de l’énumération [**TextRenderingHint**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint) , qui est déclarée dans Gdiplusenums. h.

GDI+ fournit un anticrénelage traditionnel et un nouveau type d’anticrénelage basé sur la technologie d’affichage Microsoft ClearType uniquement disponible sur Windows XP et Windows Server 2003 et versions ultérieures de Windows. Le lissage ClearType améliore la lisibilité sur les moniteurs LCD couleur qui ont une interface numérique, comme les moniteurs des ordinateurs portables et les écrans plats de haute qualité. La lisibilité sur les écrans CRT est également un peu améliorée.

ClearType dépend de l’orientation et de l’ordre des bandes LCD. À l’heure actuelle, ClearType est implémenté uniquement pour les bandes verticales qui sont triées RVB. Cela peut être un problème si vous utilisez un Tablet PC, où l’affichage peut être orienté dans n’importe quelle direction ou si vous utilisez un écran qui peut être converti en mode portrait.

L’exemple suivant dessine du texte avec deux paramètres de qualité différents :


```
FontFamily  fontFamily(L"Times New Roman");
Font        font(&fontFamily, 32, FontStyleRegular, UnitPixel);
SolidBrush  solidBrush(Color(255, 0, 0, 255));
WCHAR       string1[] = L"SingleBitPerPixel";
WCHAR       string2[] = L"AntiAlias";

graphics.SetTextRenderingHint(TextRenderingHintSingleBitPerPixel);
graphics.DrawString(string1, -1, &font, PointF(10.0f, 10.0f), &solidBrush);

graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);
graphics.DrawString(string2, -1, &font, PointF(10.0f, 60.0f), &solidBrush);
            
```



L’illustration suivante montre la sortie du code précédent.

![capture d’écran d’une chaîne dont les caractères ont des bords dentelés et un avec des bords lisses](images/fontstext10.png)

 

 



