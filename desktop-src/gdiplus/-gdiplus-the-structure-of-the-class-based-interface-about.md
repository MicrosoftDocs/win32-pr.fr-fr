---
description: l’interface C++ à Windows GDI+ contient environ 40 classes, 50 énumérations et 6 structures. Il existe également quelques fonctions qui ne sont pas membres d’une classe.
ms.assetid: 46051bfa-b842-4e4e-bda8-e9003b5b5da4
title: Structure de l’interface basée sur une classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2627d695330c316a57c2593e75233d73b27a1524
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127522556"
---
# <a name="the-structure-of-the-class-based-interface"></a>Structure de l’interface basée sur une classe

l’interface C++ à Windows GDI+ contient environ 40 classes, 50 énumérations et 6 structures. Il existe également quelques fonctions qui ne sont pas membres d’une classe.

vous devez indiquer que l’espace de noms Gdiplus est utilisé avant l’appel de toutes les fonctions GDI+. L’instruction suivante indique que l’espace de noms Gdiplus est utilisé dans l’application.

`using namespace Gdiplus;`

la classe [**graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) est le cœur de l’interface GDI+; Il s’agit de la classe qui dessine réellement des lignes, des courbes, des figures, des images et du texte.

De nombreuses classes fonctionnent conjointement avec la classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Par exemple, la méthode [Graphics ::D rawline](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) reçoit un pointeur vers un objet [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) , qui contient les attributs (couleur, largeur, style de ligne et similaire) de la ligne à dessiner. La méthode [Graphics :: FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inconstrectf_)) peut recevoir un pointeur vers un objet [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) , qui fonctionne avec l’objet **Graphics** pour remplir un rectangle avec une couleur qui change progressivement. Les objets [**font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) et [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) influencent la manière dont un objet **Graphics** dessine le texte. Un objet [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) stocke et manipule la transformation universelle d’un objet **Graphics** , qui est utilisée pour faire pivoter, mettre à l’échelle et retourner des images.

Certaines classes servent principalement de types de données structurées. Certaines de ces classes (par exemple, [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect), [**point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point)et [**Size**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-size)) sont à des fins générales. D’autres sont à des fins spécialisées et sont considérées comme des classes d’assistance. Par exemple, la classe [**BitmapData**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-bitmapdata) est une application auxiliaire pour la classe [**bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) , et la classe [**PathData**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pathdata) est une application auxiliaire pour la classe [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) . GDI+ définit également quelques structures utilisées pour organiser les données. Par exemple, la structure [**ColorMap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) contient une paire d’objets [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) qui forment une entrée dans une table de conversion des couleurs.

GDI+ définit plusieurs énumérations, qui sont des collections de constantes associées. Par exemple, l’énumération [**LineJoin**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-linejoin) contient les [éléments * * * * LineJoinBevel * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-linejoin)* *, [* * * * LineJoinMiter *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-linejoin)* * *, et * * * * [LineJoinRound * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-linejoin)* *, qui spécifient les styles qui peuvent être utilisés pour joindre deux lignes.

GDI+ fournit quelques fonctions qui ne font partie d’aucune classe. Deux de ces fonctions sont [**GdiplusStartup**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) et [**GdiplusShutdown**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown). vous devez appeler **GdiplusStartup** avant d’effectuer d’autres appels de GDI+, et vous devez appeler **GdiplusShutdown** lorsque vous avez fini d’utiliser GDI+.

 

 
