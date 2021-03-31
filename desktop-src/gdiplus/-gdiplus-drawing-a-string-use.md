---
description: La rubrique dessine une ligne montre comment écrire une application Windows qui utilise GDI+ pour dessiner une ligne.
ms.assetid: fcf45b19-456c-4551-8901-d587a73a5638
title: Dessin d’une chaîne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a88e76fd38dd640a402edf202dc6cdbd3008a76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202427"
---
# <a name="drawing-a-string"></a>Dessin d’une chaîne

La rubrique [dessine une ligne](-gdiplus-drawing-a-line-use.md) montre comment écrire une application Windows qui utilise GDI+ pour dessiner une ligne. Pour dessiner une chaîne, remplacez la fonction **OnPaint** présentée dans cette rubrique par la fonction **OnPaint** suivante :


```
VOID OnPaint(HDC hdc)
{
   Graphics    graphics(hdc);
   SolidBrush  brush(Color(255, 0, 0, 255));
   FontFamily  fontFamily(L"Times New Roman");
   Font        font(&fontFamily, 24, FontStyleRegular, UnitPixel);
   PointF      pointF(10.0f, 20.0f);
   
   graphics.DrawString(L"Hello World!", -1, &font, pointF, &brush);
}
```



Le code précédent crée plusieurs objets GDI+. L’objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) fournit la méthode [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) , qui effectue le dessin réel. L’objet [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) spécifie la couleur de la chaîne.

Le constructeur [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) reçoit un argument de chaîne unique qui identifie la famille de polices. L’adresse de l’objet **FontFamily** est le premier argument passé au constructeur [**font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) . Le deuxième argument passé au constructeur [font](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(constfont_)) spécifie la taille de la police et le troisième argument spécifie le style. La valeur **FontStyleRegular** est un membre de l’énumération [**FontStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-fontstyle) , qui est déclarée dans Gdiplusenums. h. Le dernier argument du constructeur **font** indique que la taille de la police (24 dans ce cas) est mesurée en pixels. La valeur **UnitPixel** est un membre de l’énumération d' [**unités**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-unit) .

Le premier argument passé à la méthode [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) est l’adresse d’une chaîne de caractères larges. Le deuxième argument,-1, spécifie que la chaîne se termine par une valeur null. (Si la chaîne ne se termine pas par null, le deuxième argument doit spécifier le nombre de caractères larges dans la chaîne.) Le troisième argument est l’adresse de l’objet [**font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) . Le quatrième argument est une référence à un objet [**PointF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf) qui spécifie l’emplacement où la chaîne sera dessinée. Le dernier argument est l’adresse de l’objet [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) , qui spécifie la couleur de la chaîne.

 

 
