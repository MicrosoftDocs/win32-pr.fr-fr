---
description: 'Vous pouvez remplir un chemin d’accès en passant l’adresse d’un objet GraphicsPath à la méthode Graphics :: FillPath.'
ms.assetid: 4cf293cf-5155-4ce2-afeb-cc9ca9395764
title: Remplissage des figures ouvertes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53f4a4608b787d8b0af8b9e9c7100a43c0c76dc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104559463"
---
# <a name="filling-open-figures"></a><span data-ttu-id="fad97-103">Remplissage des figures ouvertes</span><span class="sxs-lookup"><span data-stu-id="fad97-103">Filling Open Figures</span></span>

<span data-ttu-id="fad97-104">Vous pouvez remplir un chemin d’accès en passant l’adresse d’un objet [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) à la méthode [**Graphics :: FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) .</span><span class="sxs-lookup"><span data-stu-id="fad97-104">You can fill a path by passing the address of a [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object to the [**Graphics::FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) method.</span></span> <span data-ttu-id="fad97-105">La méthode **Graphics :: FillPath** remplit le chemin d’accès en fonction du mode de remplissage (alternative ou enroulement) actuellement défini pour le tracé.</span><span class="sxs-lookup"><span data-stu-id="fad97-105">The **Graphics::FillPath** method fills the path according to the fill mode (alternate or winding) currently set for the path.</span></span> <span data-ttu-id="fad97-106">Si le chemin d’accès comporte des figures ouvertes, le chemin d’accès est rempli comme si ces figures étaient fermées.</span><span class="sxs-lookup"><span data-stu-id="fad97-106">If the path has any open figures, the path is filled as if those figures were closed.</span></span> <span data-ttu-id="fad97-107">GDI+ ferme une figure en dessinant une ligne droite à partir de son point de fin jusqu’à son point de départ.</span><span class="sxs-lookup"><span data-stu-id="fad97-107">GDI+ closes a figure by drawing a straight line from its ending point to its starting point.</span></span>

<span data-ttu-id="fad97-108">L’exemple suivant crée un tracé qui a une figure ouverte (un arc) et une figure fermée (une ellipse).</span><span class="sxs-lookup"><span data-stu-id="fad97-108">The following example creates a path that has one open figure (an arc) and one closed figure (an ellipse).</span></span> <span data-ttu-id="fad97-109">La méthode [**Graphics :: FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) remplit le chemin d’accès en fonction du mode de remplissage par défaut, qui est FillModeAlternate.</span><span class="sxs-lookup"><span data-stu-id="fad97-109">The [**Graphics::FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) method fills the path according to the default fill mode, which is FillModeAlternate.</span></span>


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



<span data-ttu-id="fad97-110">L’illustration suivante montre la sortie du code précédent.</span><span class="sxs-lookup"><span data-stu-id="fad97-110">The following illustration shows the output of the preceding code.</span></span> <span data-ttu-id="fad97-111">Notez que le chemin d’accès est rempli (selon FillModeAlternate) comme si la figure ouverte était fermée par une ligne droite, de son point de fin à son point de départ.</span><span class="sxs-lookup"><span data-stu-id="fad97-111">Note that path is filled (according to FillModeAlternate) as if the open figure were closed by a straight line from its ending point to its starting point.</span></span>

![Illustration montrant une ellipse supérieure qui chevauche la moitié inférieure d’une ellipse étendue ; l’Union est remplie, mais l’intersection est vide](images/fillopenpath.png)

 

 



