---
description: Pour appliquer une mise en forme spéciale à du texte, initialisez un objet StringFormat et transmettez l’adresse de cet objet à la méthode DrawString de la classe Graphics.
ms.assetid: 4014a602-88f6-4fac-b4b2-3dafdcff8f33
title: Mise en forme du texte (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e6b2cc6109e7b946e9b4e98645c9445b8268bb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104553255"
---
# <a name="formatting-text-gdi"></a>Mise en forme du texte (GDI+)

Pour appliquer une mise en forme spéciale à du texte, initialisez un objet [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) et transmettez l’adresse de cet objet à la méthode [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) de la classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .

Pour dessiner du texte mis en forme dans un rectangle, vous avez besoin des objets [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font), [**RectF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rectf), [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat)et [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) .

-   [Aligner du texte](#aligning-text)
-   [Définir des taquets de tabulation](#setting-tab-stops)
-   [Dessiner du texte vertical](#drawing-vertical-text)

## <a name="aligning-text"></a>Aligner du texte

L’exemple suivant dessine du texte dans un rectangle. Chaque ligne de texte est centrée (côte à côte) et le bloc de texte entier est centré (de haut en bas) dans le rectangle.


```
WCHAR string[] = 
   L"Use StringFormat and RectF objects to center text in a rectangle.";
                       
FontFamily   fontFamily(L"Arial");
Font         font(&fontFamily, 12, FontStyleBold, UnitPoint);
RectF        rectF(30.0f, 10.0f, 120.0f, 140.0f);
StringFormat stringFormat;
SolidBrush   solidBrush(Color(255, 0, 0, 255));

// Center-justify each line of text.
stringFormat.SetAlignment(StringAlignmentCenter);

// Center the block of text (top to bottom) in the rectangle.
stringFormat.SetLineAlignment(StringAlignmentCenter);

graphics.DrawString(string, -1, &font, rectF, &stringFormat, &solidBrush);

Pen pen(Color(255, 0, 0, 0));
graphics.DrawRectangle(&pen, rectF);
            
```



L’illustration suivante montre le rectangle et le texte centré.

![capture d’écran d’une fenêtre contenant un rectangle, qui contient six lignes de texte, centrées horizontalement](images/fontstext3.png)

Le code précédent appelle deux méthodes de l’objet [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) : [**StringFormat :: SetAlignment**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setalignment) et [**StringFormat :: SetLineAlignment**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setlinealignment). L’appel à **StringFormat :: SetAlignment** spécifie que chaque ligne de texte est centrée dans le rectangle donné par le troisième argument passé à la méthode [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) . L’appel à **StringFormat :: SetLineAlignment** spécifie que le bloc de texte est centré (de haut en bas) dans le rectangle.

La valeur [* * * * StringAlignmentCenter * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringalignment) * * est un élément de l’énumération **StringAlignment** , qui est déclarée dans Gdiplusenums. h.

## <a name="setting-tab-stops"></a>Définir des taquets de tabulation

Vous pouvez définir des taquets de tabulation pour le texte en appelant la méthode [**StringFormat :: SetTabStops**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-settabstops) d’un objet [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) , puis en passant l’adresse de cet objet **StringFormat** à la méthode [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) de la classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .

L’exemple suivant définit des taquets de tabulation à 150, 250 et 350. Ensuite, le code affiche une liste avec onglets de noms et de scores de test.


```
WCHAR string[150] = 
   L"Name\tTest 1\tTest 2\tTest 3\n";

StringCchCatW(string, 150, L"Joe\t95\t88\t91\n");
StringCchCatW(string, 150, L"Mary\t98\t84\t90\n");
StringCchCatW(string, 150, L"Sam\t42\t76\t98\n");
StringCchCatW(string, 150, L"Jane\t65\t73\t92\n");
                       
FontFamily   fontFamily(L"Courier New");
Font         font(&fontFamily, 12, FontStyleRegular, UnitPoint);
RectF        rectF(10.0f, 10.0f, 450.0f, 100.0f);
StringFormat stringFormat;
SolidBrush   solidBrush(Color(255, 0, 0, 255));
REAL         tabs[] = {150.0f, 100.0f, 100.0f};

stringFormat.SetTabStops(0.0f, 3, tabs);

graphics.DrawString(string, -1, &font, rectF, &stringFormat, &solidBrush);

Pen pen(Color(255, 0, 0, 0));
graphics.DrawRectangle(&pen, rectF);
            
```



L’illustration suivante montre le texte avec onglets.

![illustration d’un rectangle contenant quatre colonnes de texte ; chaque colonne est redéfinie à gauche](images/fontstext4.png)

Le code précédent passe trois arguments à la méthode [**StringFormat :: SetTabStops**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-settabstops) . Le troisième argument est l’adresse d’un tableau contenant les décalages de tabulation. Le deuxième argument indique qu’il y a trois décalages dans ce tableau. Le premier argument passé à **StringFormat :: SetTabStops** est 0, ce qui indique que le premier décalage dans le tableau est mesuré à partir de la position 0, le bord gauche du rectangle englobant.

## <a name="drawing-vertical-text"></a>Dessiner du texte vertical

Vous pouvez utiliser un objet [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) pour spécifier que le texte doit être dessiné verticalement plutôt que horizontalement.

L’exemple suivant passe la valeur [* * * * StringFormatFlagsDirectionVertical * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringformatflags) * * à la méthode [**StringFormat :: SetFormatFlags**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setformatflags) d’un objet [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) . L’adresse de cet objet **StringFormat** est passée à la méthode [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) de la classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . La valeur [* * * * StringFormatFlagsDirectionVertical * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringformatflags) * * est un élément de l’énumération **StringFormatFlags** , qui est déclarée dans Gdiplusenums. h.


```
WCHAR string[] = L"Vertical text";
                     
FontFamily   fontFamily(L"Lucida Console");
Font         font(&fontFamily, 14, FontStyleRegular, UnitPoint);
PointF       pointF(40.0f, 10.0f);
StringFormat stringFormat;
SolidBrush   solidBrush(Color(255, 0, 0, 255));

stringFormat.SetFormatFlags(StringFormatFlagsDirectionVertical);

graphics.DrawString(string, -1, &font, pointF, &stringFormat, &solidBrush);
            
```



L’illustration suivante montre le texte vertical.

![Illustration montrant une fenêtre contenant du texte pivoté de 90 degrés dans le sens des aiguilles d’une montre](images/fontstext5.png)

 

 



