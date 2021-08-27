---
description: Windows GDI+ fournit des conteneurs que vous pouvez utiliser pour remplacer ou augmenter temporairement une partie de l’état dans un objet graphics.
ms.assetid: f3fce8ef-903a-4b9d-b76c-562739d02eb3
title: Conteneurs Graphics imbriqués
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d88b3a768e5b156eb5d28410ad69d58227e9660618764ca4b084b5e35662b839
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114979"
---
# <a name="nested-graphics-containers"></a>Conteneurs Graphics imbriqués

Windows GDI+ fournit des conteneurs que vous pouvez utiliser pour remplacer ou augmenter temporairement une partie de l’état dans un objet [**graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Pour créer un conteneur, appelez la méthode [**Graphics :: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) d’un objet **Graphics** . Vous pouvez appeler **Graphics :: BeginContainer** à plusieurs reprises pour former des conteneurs imbriqués.

## <a name="transformations-in-nested-containers"></a>Transformations dans les conteneurs imbriqués

L’exemple suivant crée un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) et un conteneur dans cet objet **Graphics** . La transformation universelle de l’objet **Graphics** est une translation de 100 unités sur la direction x et de 80 unités sur l’axe y. La transformation universelle du conteneur est une rotation à 30 degrés. Le code effectue l’appel


```
DrawRectangle(&pen, -60, -30, 120, 60)
```



deux fois. Le premier appel à [**Graphics ::D rawrectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) est *à l’intérieur du conteneur*; autrement dit, l’appel se trouve entre les appels à [**Graphics :: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) et [**Graphics :: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer). Le deuxième appel à **Graphics ::D rawrectangle** est après l’appel à **Graphics :: EndContainer**.


```
Graphics           graphics(hdc);
Pen                pen(Color(255, 255, 0, 0));
GraphicsContainer  graphicsContainer;

graphics.TranslateTransform(100.0f, 80.0f);

graphicsContainer = graphics.BeginContainer();
   graphics.RotateTransform(30.0f);
   graphics.DrawRectangle(&pen, -60, -30, 120, 60);
graphics.EndContainer(graphicsContainer);

graphics.DrawRectangle(&pen, -60, -30, 120, 60);
```



Dans le code précédent, le Rectangle dessiné à partir de l’intérieur du conteneur est transformé en premier par la transformation universelle du conteneur (rotation), puis par la transformation universelle de l’objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) (translation). Le Rectangle dessiné à l’extérieur du conteneur est transformé uniquement par la transformation universelle de l’objet **Graphics** (translation). L’illustration suivante montre les deux rectangles.

![capture d’écran d’une fenêtre avec deux rectangles rouges centrés sur le même point, mais avec des rotations différentes](images/nestedcontainers1.png)

 

## <a name="clipping-in-nested-containers"></a>Découpage dans les conteneurs imbriqués

L’exemple suivant illustre la façon dont les conteneurs imbriqués gèrent les régions de découpage. Le code crée un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) et un conteneur dans cet objet **Graphics** . La zone de découpage de l’objet **Graphics** est un rectangle et la zone de découpage du conteneur est une ellipse. Le code effectue deux appels à la méthode [**Graphics ::D rawline**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) . Le premier appel à **Graphics ::D rawline** est à l’intérieur du conteneur, et le deuxième appel à **graphics ::D rawline** se trouve en dehors du conteneur (après l’appel à [**Graphics :: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)). La première ligne est découpée en fonction de l’intersection des deux régions de découpage. La deuxième ligne est découpée uniquement par la zone de découpage rectangulaire de l’objet **Graphics** .


```
Graphics           graphics(hdc);
GraphicsContainer  graphicsContainer;
Pen                redPen(Color(255, 255, 0, 0), 2);
Pen                bluePen(Color(255, 0, 0, 255), 2);
SolidBrush         aquaBrush(Color(255, 180, 255, 255));
SolidBrush         greenBrush(Color(255, 150, 250, 130));

graphics.SetClip(Rect(50, 65, 150, 120));
graphics.FillRectangle(&aquaBrush, 50, 65, 150, 120);

graphicsContainer = graphics.BeginContainer();
   // Create a path that consists of a single ellipse.
   GraphicsPath path;
   path.AddEllipse(75, 50, 100, 150);

  // Construct a region based on the path.
   Region region(&path);
   graphics.FillRegion(&greenBrush, &region);

   graphics.SetClip(&region);
   graphics.DrawLine(&redPen, 50, 0, 350, 300);
graphics.EndContainer(graphicsContainer);

graphics.DrawLine(&bluePen, 70, 0, 370, 300);
```



L’illustration suivante montre les deux lignes écrêtées.

![illustration d’une ellipse à l’intérieur d’un rectangle, avec une ligne coupée par l’ellipse et l’autre par le rectangle](images/nestedcontainers2.png)

Comme le montrent les deux exemples précédents, les transformations et les régions de découpage sont cumulatives dans les conteneurs imbriqués. Si vous définissez les transformations universelles du conteneur et de l’objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , les deux transformations s’appliqueront aux éléments dessinés à partir de l’intérieur du conteneur. La transformation du conteneur est appliquée en premier, et la transformation de l’objet **Graphics** est appliquée en second. Si vous définissez les régions de découpage du conteneur et de l’objet **Graphics** , les éléments dessinés à l’intérieur du conteneur sont découpés par l’intersection des deux régions de découpage.

## <a name="quality-settings-in-nested-containers"></a>Paramètres de qualité dans les conteneurs imbriqués

Les paramètres de qualité ( [**SmoothingMode**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode), [**TextRenderingHint**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)et like) dans les conteneurs imbriqués ne sont pas cumulatifs ; au lieu de cela, les paramètres de qualité du conteneur remplacent temporairement les paramètres de qualité d’un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Lorsque vous créez un conteneur, les paramètres de qualité de ce conteneur sont définis sur les valeurs par défaut. Par exemple, supposons que vous ayez un objet **Graphics** avec un mode de lissage [* * * * SmoothingModeAntiAlias * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode)* *. Lorsque vous créez un conteneur, le mode de lissage à l’intérieur du conteneur est le mode de lissage par défaut. Vous êtes libre de définir le mode de lissage du conteneur, et tous les éléments dessinés à l’intérieur du conteneur sont dessinés en fonction du mode que vous définissez. Les éléments dessinés après l’appel à [**Graphics :: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) sont dessinés en fonction du mode de lissage ([* * * * SmoothingModeAntiAlias * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode)* *) qui était en place avant l’appel à [**Graphics :: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)).

## <a name="several-layers-of-nested-containers"></a>Plusieurs couches de conteneurs imbriqués

Vous n’êtes pas limité à un conteneur dans un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Vous pouvez créer une séquence de conteneurs, chacun imbriqué dans le précédent, et vous pouvez spécifier la transformation universelle, la région de découpage et les paramètres de qualité de chacun de ces conteneurs imbriqués. Si vous appelez une méthode de dessin à partir de l’intérieur du conteneur le plus profond, les transformations sont appliquées dans l’ordre, en commençant par le conteneur le plus profond et en terminant par le conteneur le plus à l’extérieur. Les éléments dessinés à l’intérieur du conteneur le plus profond sont découpés par l’intersection de toutes les régions de découpage.

L’exemple suivant crée un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) et définit son indicateur de rendu de texte sur [* * * * TextRenderingHintAntiAlias * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)* *. Le code crée deux conteneurs, l’un imbriqué dans l’autre. L’indicateur de rendu de texte du conteneur externe est défini sur [* * * * TextRenderingHintSingleBitPerPixel * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)* *, et l’indicateur de rendu de texte du conteneur interne est défini sur [* * * * TextRenderingHintAntiAlias * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)* *. Le code dessine trois chaînes : une à partir du conteneur interne, une à partir du conteneur externe et une à partir de l’objet **Graphics** lui-même.


```
Graphics graphics(hdc);
GraphicsContainer innerContainer;
GraphicsContainer outerContainer;
SolidBrush brush(Color(255, 0, 0, 255));
FontFamily fontFamily(L"Times New Roman");
Font font(&fontFamily, 36, FontStyleRegular, UnitPixel);

graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);

outerContainer = graphics.BeginContainer();

   graphics.SetTextRenderingHint(TextRenderingHintSingleBitPerPixel);

   innerContainer = graphics.BeginContainer();
      graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);
      graphics.DrawString(L"Inner Container", 15, &font,
         PointF(20, 10), &brush);
   graphics.EndContainer(innerContainer);

   graphics.DrawString(L"Outer Container", 15, &font, PointF(20, 50), &brush);

graphics.EndContainer(outerContainer);

graphics.DrawString(L"Graphics Object", 15, &font, PointF(20, 90), &brush);
```



L’illustration suivante montre les trois chaînes. Les chaînes dessinées à partir du conteneur interne et de l’objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) sont lissées par l’anticrénelage. La chaîne dessinée à partir du conteneur externe n’est pas lissée par l’anticrénelage en raison du paramètre TextRenderingHintSingleBitPerPixel.

![illustration d’un rectangle contenant la même chaîne à l’heure ; Seuls les caractères de la première et de la dernière lignes sont lisses](images/nestedcontainers3.png)

 

 
