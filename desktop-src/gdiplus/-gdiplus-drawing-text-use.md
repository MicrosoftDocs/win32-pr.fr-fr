---
description: Vous pouvez utiliser la méthode DrawString de la classe Graphics pour dessiner du texte à un emplacement spécifié ou dans un rectangle spécifié.
ms.assetid: a873c132-f232-4144-bcc3-ca200055074c
title: Dessiner du texte (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e16ed49a5ab92380b42ed3316346ac547f95be9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115231"
---
# <a name="drawing-text-gdi"></a>Dessiner du texte (GDI+)

Vous pouvez utiliser la méthode [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) de la classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) pour dessiner du texte à un emplacement spécifié ou dans un rectangle spécifié.

-   [Dessin de texte à un emplacement spécifié](#drawing-text-at-a-specified-location)
-   [Dessiner du texte dans un rectangle](#drawing-text-in-a-rectangle)

## <a name="drawing-text-at-a-specified-location"></a>Dessin de texte à un emplacement spécifié

Pour dessiner du texte à un emplacement spécifié, vous avez besoin d’objets [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font), [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf)et [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) .

L’exemple suivant dessine la chaîne « Hello » à l’emplacement (30, 10). La famille de polices est Times New Roman. La police, qui est un membre individuel de la famille de polices, est Times New Roman, taille 24 pixels, style normal. Supposons que **Graphics** est un objet [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) existant.

```
FontFamily  fontFamily(L"Times New Roman");
Font        font(&fontFamily, 24, FontStyleRegular, UnitPixel);
PointF      pointF(30.0f, 10.0f);
SolidBrush  solidBrush(Color(255, 0, 0, 255));

graphics.DrawString(L"Hello", -1, &font, pointF, &solidBrush);

```

L’illustration suivante montre la sortie du code précédent.

![capture d’écran d’une petite fenêtre contenant le texte « Hello »](images/fontstext1.png)

Dans l’exemple précédent, le constructeur [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) reçoit une chaîne qui identifie la famille de polices. L’adresse de l’objet **FontFamily** est passée comme premier argument au constructeur [**font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) . Le deuxième argument passé au constructeur **font** spécifie la taille de la police mesurée dans les unités fournies par le quatrième argument. Le troisième argument spécifie le style (normal, gras, italique, etc.) de la police.

La méthode [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) reçoit cinq arguments. Le premier argument est la chaîne à dessiner et le deuxième argument est la longueur (en caractères, et non en octets) de cette chaîne. Si la chaîne se termine par un caractère null, vous pouvez passer-1 pour la longueur. Le troisième argument est l’adresse de l’objet [**font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) qui a été construit précédemment. Le quatrième argument est un objet [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf) qui contient les coordonnées de l’angle supérieur gauche de la chaîne. Le cinquième argument est l’adresse d’un objet [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) qui sera utilisé pour remplir les caractères de la chaîne.

## <a name="drawing-text-in-a-rectangle"></a>Dessiner du texte dans un rectangle

L’une des méthodes [**DrawString**](https://www.bing.com/search?q=**DrawString**) de la classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) a un paramètre *RectF* . En appelant cette méthode **DrawString** , vous pouvez dessiner du texte encapsulé dans un rectangle spécifié. Pour dessiner du texte dans un rectangle, vous avez besoin des objets **Graphics**, [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font), [**RectF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf)et [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) .

L’exemple suivant crée un rectangle avec l’angle supérieur gauche (30, 10), la largeur 100 et la hauteur 122. Le code dessine ensuite une chaîne à l’intérieur de ce rectangle. La chaîne est limitée au rectangle et s’encapsule de telle sorte que les mots individuels ne sont pas rompus.

```
WCHAR string[] = 
   L"Draw text in a rectangle by passing a RectF to the DrawString method.";

FontFamily   fontFamily(L"Arial");
Font         font(&fontFamily, 12, FontStyleBold, UnitPoint);
RectF        rectF(30.0f, 10.0f, 100.0f, 122.0f);
SolidBrush   solidBrush(Color(255, 0, 0, 255));

graphics.DrawString(string, -1, &font, rectF, NULL, &solidBrush);

Pen pen(Color(255, 0, 0, 0));
graphics.DrawRectangle(&pen, rectF);
```

L’illustration suivante montre le texte dessiné dans le rectangle.

![capture d’écran d’une petite fenêtre contenant un recangle, dans laquelle apparaît la première partie d’une phrase](images/fontstext2.png)

Dans l’exemple précédent, le quatrième argument passé à la méthode [**DrawString**](https://www.bing.com/search?q=**DrawString**) est un objet [**RectF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf) qui spécifie le rectangle englobant du texte. Le cinquième paramètre est de type [**StringFormat**](/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat): l’argument a la **valeur null** , car aucune mise en forme de chaîne spéciale n’est requise.
