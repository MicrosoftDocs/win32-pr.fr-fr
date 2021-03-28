---
description: Windows GDI+ fournit plusieurs classes qui constituent la base pour dessiner du texte.
ms.assetid: 12bc38c3-5fbc-4d7b-902c-92a5f5057473
title: Utilisation du texte et des polices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f28ec157888dcf45b309237eb0f7eefff17808c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526056"
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

 

 



