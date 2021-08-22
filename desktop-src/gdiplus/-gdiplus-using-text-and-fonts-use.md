---
description: Windows GDI+ fournit plusieurs classes qui constituent la base pour dessiner du texte.
ms.assetid: 12bc38c3-5fbc-4d7b-902c-92a5f5057473
title: Utilisation du texte et des polices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2cffc8c36da4c9dd8bbc78c6660a7cc85094071350003c5b23ce4d6a6ce7cad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119359599"
---
# <a name="using-text-and-fonts"></a>Utilisation du texte et des polices

Windows GDI+ fournit plusieurs classes qui constituent la base pour dessiner du texte. La classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) possède plusieurs méthodes [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) qui vous permettent de spécifier différentes fonctionnalités de texte, telles que l’emplacement, le rectangle englobant, la police et le format. Les autres classes qui contribuent à la restitution du texte incluent notamment [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font), [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat), [**InstalledFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-installedfontcollection)et [**la**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection).

Les rubriques suivantes traitent du texte et des polices plus en détail :

-   [Construction des familles de polices et des polices](-gdiplus-constructing-font-families-and-fonts-use.md)
-   [Dessiner du texte](-gdiplus-drawing-text-use.md)
-   [Mise en forme du texte](-gdiplus-formatting-text-use.md)
-   [Énumération des polices installées](-gdiplus-enumerating-installed-fonts-use.md)
-   [Création de collections de polices privées](-gdiplus-creating-a-private-font-collection-use.md)
-   [Obtention de métriques de police](-gdiplus-obtaining-font-metrics-use.md)
-   [Anticrénelage avec du texte](-gdiplus-antialiasing-with-text-use.md)

 

 



