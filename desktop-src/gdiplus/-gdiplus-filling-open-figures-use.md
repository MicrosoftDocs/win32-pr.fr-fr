---
description: 'Vous pouvez remplir un chemin d’accès en passant l’adresse d’un objet GraphicsPath à la méthode Graphics :: FillPath.'
ms.assetid: 4cf293cf-5155-4ce2-afeb-cc9ca9395764
title: Remplissage des figures ouvertes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 198a1a9e3a3cffa6aa5c0f3627c1415a54c8842c9f90a2ebdd6ebc2a9e0f3fb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977539"
---
# <a name="filling-open-figures"></a>Remplissage des figures ouvertes

Vous pouvez remplir un chemin d’accès en passant l’adresse d’un objet [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) à la méthode [**Graphics :: FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) . La méthode **Graphics :: FillPath** remplit le chemin d’accès en fonction du mode de remplissage (alternative ou enroulement) actuellement défini pour le tracé. Si le chemin d’accès comporte des figures ouvertes, le chemin d’accès est rempli comme si ces figures étaient fermées. GDI+ ferme une figure en dessinant une ligne droite à partir de son point de fin jusqu’à son point de départ.

L’exemple suivant crée un tracé qui a une figure ouverte (un arc) et une figure fermée (une ellipse). La méthode [**Graphics :: FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) remplit le chemin d’accès en fonction du mode de remplissage par défaut, qui est FillModeAlternate.


```
GraphicsPath path;

// Add an open figure.
path.AddArc(0, 0, 150, 120, 30, 120);

// Add an intrinsically closed figure.
path.AddEllipse(50, 50, 50, 100);

Pen pen(Color(128, 0, 0, 255), 5);
SolidBrush brush(Color(255, 255, 0, 0));

// The fill mode is FillModeAlternate by default.
graphics.FillPath(&brush, &path);
graphics.DrawPath(&pen, &path);
```



L’illustration suivante montre la sortie du code précédent. Notez que le chemin d’accès est rempli (selon FillModeAlternate) comme si la figure ouverte était fermée par une ligne droite, de son point de fin à son point de départ.

![Illustration montrant une ellipse supérieure qui chevauche la moitié inférieure d’une ellipse étendue ; l’Union est remplie, mais l’intersection est vide](images/fillopenpath.png)

 

 



