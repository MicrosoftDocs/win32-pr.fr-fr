---
description: L’une des propriétés de la classe Graphics est la zone de découpage. Tout le dessin effectué par un objet Graphics donné est limité à la zone de découpage de cet objet Graphics. Vous pouvez définir la région de découpage en appelant la méthode SetClip.
ms.assetid: 816a5845-ca03-46c6-bdda-e6a7d02ff614
title: Découpage avec une région
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae2569350dd0d25066c42fc8ee102cad76e8e77c425bd075122da2179dd3249c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943899"
---
# <a name="clipping-with-a-region"></a>Découpage avec une région

L’une des propriétés de la classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) est la zone de découpage. Tout le dessin effectué par un objet **Graphics** donné est limité à la zone de découpage de cet objet **Graphics** . Vous pouvez définir la région de découpage en appelant la méthode **SetClip** .

L’exemple suivant construit un tracé qui se compose d’un seul polygone. Ensuite, le code construit une région basée sur ce chemin. L’adresse de la région est passée à la méthode **SetClip** d’un objet [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , puis deux chaînes sont dessinées.


```
// Create a path that consists of a single polygon.
Point polyPoints[] = {Point(10, 10), Point(150, 10), 
   Point(100, 75), Point(100, 150)};
GraphicsPath path;
path.AddPolygon(polyPoints, 4);
// Construct a region based on the path.
Region region(&path);
// Draw the outline of the region.
Pen pen(Color(255, 0, 0, 0));
graphics.DrawPath(&pen, &path);
// Set the clipping region of the Graphics object.
graphics.SetClip(&region);
// Draw some clipped strings.
FontFamily fontFamily(L"Arial");
Font font(&fontFamily, 36, FontStyleBold, UnitPixel);
SolidBrush solidBrush(Color(255, 255, 0, 0));
graphics.DrawString(L"A Clipping Region", 20, &font, 
   PointF(15, 25), &solidBrush);
graphics.DrawString(L"A Clipping Region", 20, &font, 
   PointF(15, 68), &solidBrush);
```



L’illustration suivante montre les chaînes découpées.

![Illustration montrant des parties de deux phrases apparaissant à l’intérieur d’une forme à quatre côtés](images/clip1.png)

 

 



