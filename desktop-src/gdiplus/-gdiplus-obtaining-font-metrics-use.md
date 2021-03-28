---
description: 'La classe FontFamily fournit les méthodes suivantes qui récupèrent différentes mesures pour une combinaison famille/style particulière :'
ms.assetid: 3be485d0-9e0d-43e0-813e-668102ebc010
title: Obtention de métriques de police
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 800fcee7dd1729a6fd5e59bb5dd636af89670776
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033965"
---
# <a name="obtaining-font-metrics"></a>Obtention de métriques de police

La classe [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) fournit les méthodes suivantes qui récupèrent différentes mesures pour une combinaison famille/style particulière :

-   [**FontFamily :: GetEmHeight**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getemheight)(FontStyle)
-   [**FontFamily :: GetCellAscent**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getcellascent)(FontStyle)
-   [**FontFamily :: GetCellDescent**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getcelldescent)(FontStyle)
-   [**FontFamily :: GetLineSpacing**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getlinespacing)(FontStyle)

Les nombres retournés par ces méthodes sont des unités de conception de police, donc ils sont indépendants de la taille et des unités d’un objet de [**police**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) particulier.

L’illustration suivante montre les jambages ascendants, descendants et de ligne.

![diagramme de deux caractères sur les lignes adjacentes, montrant la hauteur des cellules, la descente des cellules et l’espacement des lignes](images/fontstext7a.png)

L’exemple suivant affiche les métriques du style normal de la famille de polices Arial. Le code crée également un objet de [**police**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) (basé sur la famille Arial) avec une taille de 16 pixels et affiche les métriques (en pixels) de cet objet de **police** particulier.


```
#define INFO_STRING_SIZE 100  // one line of output including null terminator
WCHAR infoString[INFO_STRING_SIZE] = L"";
UINT  ascent;                 // font family ascent in design units
REAL  ascentPixel;            // ascent converted to pixels
UINT  descent;                // font family descent in design units
REAL  descentPixel;           // descent converted to pixels
UINT  lineSpacing;            // font family line spacing in design units
REAL  lineSpacingPixel;       // line spacing converted to pixels
                       
FontFamily   fontFamily(L"Arial");
Font         font(&fontFamily, 16, FontStyleRegular, UnitPixel);
PointF       pointF(10.0f, 10.0f);
SolidBrush   solidBrush(Color(255, 0, 0, 0));

// Display the font size in pixels.
StringCchPrintf(
   infoString, 
   INFO_STRING_SIZE, 
   L"font.GetSize() returns %f.", font.GetSize());

graphics.DrawString(
   infoString, -1, &font, pointF, &solidBrush);

// Move down one line.
pointF.Y += font.GetHeight(0.0);

// Display the font family em height in design units.
StringCchPrintf(
   infoString, 
   INFO_STRING_SIZE, 
   L"fontFamily.GetEmHeight() returns %d.", 
   fontFamily.GetEmHeight(FontStyleRegular));

graphics.DrawString(infoString, -1, &font, pointF, &solidBrush);

// Move down two lines.
pointF.Y += 2.0f * font.GetHeight(0.0f);

// Display the ascent in design units and pixels.
ascent = fontFamily.GetCellAscent(FontStyleRegular);

// 14.484375 = 16.0 * 1854 / 2048
ascentPixel = 
   font.GetSize() * ascent / fontFamily.GetEmHeight(FontStyleRegular);

StringCchPrintf(
   infoString,
   INFO_STRING_SIZE,
   L"The ascent is %d design units, %f pixels.",
   ascent, 
   ascentPixel);

graphics.DrawString(infoString, -1, &font, pointF, &solidBrush);

// Move down one line.
pointF.Y += font.GetHeight(0.0f);

// Display the descent in design units and pixels.
descent = fontFamily.GetCellDescent(FontStyleRegular);

// 3.390625 = 16.0 * 434 / 2048
descentPixel = 
   font.GetSize() * descent / fontFamily.GetEmHeight(FontStyleRegular);

StringCchPrintf(
   infoString, 
   INFO_STRING_SIZE,
   L"The descent is %d design units, %f pixels.",
   descent, 
   descentPixel);

graphics.DrawString(infoString, -1, &font, pointF, &solidBrush);

// Move down one line.
pointF.Y += font.GetHeight(0.0f);

// Display the line spacing in design units and pixels.
lineSpacing = fontFamily.GetLineSpacing(FontStyleRegular);

// 18.398438 = 16.0 * 2355 / 2048
lineSpacingPixel = 
   font.GetSize() * lineSpacing / fontFamily.GetEmHeight(FontStyleRegular);

StringCchPrintf(
   infoString, 
   INFO_STRING_SIZE,
   L"The line spacing is %d design units, %f pixels.",
   lineSpacing, 
   lineSpacingPixel);

graphics.DrawString(infoString, -1, &font, pointF, &solidBrush);
            
```



L’illustration suivante montre la sortie du code précédent.

![capture d’écran d’une fenêtre avec du texte qui indique la taille de police et la hauteur, ainsi que l’espacement ascendant, descendant et de ligne](images/fontstext8.png)

Notez les deux premières lignes de la sortie de l’illustration précédente. L’objet [**font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) retourne une taille de 16, et l’objet [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) retourne une hauteur em de 2 048. Ces deux nombres (16 et 2 048) sont la clé de la conversion entre les unités de conception de police et les unités (en l’occurrence, les pixels) de l’objet **font** .

Par exemple, vous pouvez convertir la hauteur des unités de conception en pixels comme suit :

![équation qui multiplie 1854 unités de conception par 16 pixels divisée par unités de conception 2048, en équivalent à 14,484375 pixels](images/fontstext9.png)

Le code précédent positionne le texte verticalement en définissant le membre de données *y* d’un objet [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf) . La coordonnée y est augmentée `font.GetHeight(0.0f)` de pour chaque nouvelle ligne de texte. La méthode [**font :: GetHeight**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-getheight(inreal)) d’un objet [**font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) retourne l’interligne (en pixels) de cet objet **font** particulier. Dans cet exemple, le nombre retourné par **font :: GetHeight** est 18,398438. Notez que ce nombre est le même que celui obtenu en convertissant la métrique d’interligne en pixels.

 

 
