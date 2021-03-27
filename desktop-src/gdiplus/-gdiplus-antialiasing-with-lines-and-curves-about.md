---
description: Lorsque vous utilisez GDI+ pour dessiner une ligne, vous fournissez le point de départ et le point de fin de la ligne, mais vous n’avez pas besoin de fournir des informations sur les pixels individuels sur la ligne.
ms.assetid: 7c4869c1-76ff-42d1-abf1-387121943b2a
title: Anticrénelage avec des lignes et des courbes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c817d3e11b4699c9fc892b41dcc827c0861f192
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755773"
---
# <a name="antialiasing-with-lines-and-curves"></a><span data-ttu-id="d06b4-103">Anticrénelage avec des lignes et des courbes</span><span class="sxs-lookup"><span data-stu-id="d06b4-103">Antialiasing with Lines and Curves</span></span>

<span data-ttu-id="d06b4-104">Lorsque vous utilisez GDI+ pour dessiner une ligne, vous fournissez le point de départ et le point de fin de la ligne, mais vous n’avez pas besoin de fournir des informations sur les pixels individuels sur la ligne.</span><span class="sxs-lookup"><span data-stu-id="d06b4-104">When you use Windows GDI+ to draw a line, you provide the starting point and ending point of the line, but you don't have to provide any information about the individual pixels on the line.</span></span> <span data-ttu-id="d06b4-105">GDI+ fonctionne conjointement avec le logiciel de pilote d’affichage pour déterminer les pixels qui seront activés pour afficher la ligne sur un périphérique d’affichage particulier.</span><span class="sxs-lookup"><span data-stu-id="d06b4-105">GDI+ works in conjunction with the display driver software to determine which pixels will be turned on to show the line on a particular display device.</span></span>

<span data-ttu-id="d06b4-106">Envisagez une ligne rouge droite qui va du point (4, 2) jusqu’au point (16, 10).</span><span class="sxs-lookup"><span data-stu-id="d06b4-106">Consider a straight red line that goes from the point (4, 2) to the point (16, 10).</span></span> <span data-ttu-id="d06b4-107">Supposons que le système de coordonnées a son origine dans l’angle supérieur gauche et que l’unité de mesure est le pixel.</span><span class="sxs-lookup"><span data-stu-id="d06b4-107">Assume the coordinate system has its origin in the upper-left corner and that the unit of measure is the pixel.</span></span> <span data-ttu-id="d06b4-108">Supposons également que l’axe des x pointe vers la droite et que l’axe des y pointe vers le dessous.</span><span class="sxs-lookup"><span data-stu-id="d06b4-108">Also assume that the x-axis points to the right and the y-axis points down.</span></span> <span data-ttu-id="d06b4-109">L’illustration suivante montre une vue agrandie de la ligne rouge dessinée sur un arrière-plan multicolore.</span><span class="sxs-lookup"><span data-stu-id="d06b4-109">The following illustration shows an enlarged view of the red line drawn on a multicolored background.</span></span>

![Illustration montrant des pixels rouges pleins sur un arrière-plan multicolore](images/aboutgdip02-art33.png)

<span data-ttu-id="d06b4-111">Notez que les pixels rouges utilisés pour le rendu de la ligne sont opaques.</span><span class="sxs-lookup"><span data-stu-id="d06b4-111">Note that the red pixels used to render the line are opaque.</span></span> <span data-ttu-id="d06b4-112">Aucun pixel partiellement transparent n’est impliqué dans l’affichage de la ligne.</span><span class="sxs-lookup"><span data-stu-id="d06b4-112">There are no partially transparent pixels involved in displaying the line.</span></span> <span data-ttu-id="d06b4-113">Ce type de rendu de ligne donne une apparence irrégulière à la ligne, et la ligne ressemble à un peu comme un escalier.</span><span class="sxs-lookup"><span data-stu-id="d06b4-113">This type of line rendering gives the line a jagged appearance, and the line looks a bit like a staircase.</span></span> <span data-ttu-id="d06b4-114">Cette technique de représentation d’une ligne avec un escalier est appelée crénelage. l’escalier est un alias pour la ligne théorique.</span><span class="sxs-lookup"><span data-stu-id="d06b4-114">This technique of representing a line with a staircase is called aliasing; the staircase is an alias for the theoretical line.</span></span>

<span data-ttu-id="d06b4-115">Une technique plus sophistiquée pour le rendu d’une ligne implique l’utilisation de pixels partiellement transparents avec des pixels rouges purs.</span><span class="sxs-lookup"><span data-stu-id="d06b4-115">A more sophisticated technique for rendering a line involves using partially transparent pixels along with pure red pixels.</span></span> <span data-ttu-id="d06b4-116">Les pixels sont définis sur le rouge pur ou sur un mélange de rouge et de couleur d’arrière-plan en fonction de leur proximité sur la ligne.</span><span class="sxs-lookup"><span data-stu-id="d06b4-116">Pixels are set to pure red or to some blend of red and the background color depending on how close they are to the line.</span></span> <span data-ttu-id="d06b4-117">Ce type de rendu est appelé « anticrénelage » et produit une ligne que l’oeil humain perçoit comme plus lisse.</span><span class="sxs-lookup"><span data-stu-id="d06b4-117">This type of rendering is called antialiasing and results in a line that the human eye perceives as more smooth.</span></span> <span data-ttu-id="d06b4-118">L’illustration suivante montre comment certains pixels sont fusionnés avec l’arrière-plan pour produire une ligne avec un alias.</span><span class="sxs-lookup"><span data-stu-id="d06b4-118">The following illustration shows how certain pixels are blended with the background to produce an antialiased line.</span></span>

![Illustration montrant des pixels qui sont des nuances de rouge sur le même arrière-plan](images/aboutgdip02-art34.png)

<span data-ttu-id="d06b4-120">L’anticrénelage (lissage) peut également être appliqué à des courbes.</span><span class="sxs-lookup"><span data-stu-id="d06b4-120">Antialiasing (smoothing) can also be applied to curves.</span></span> <span data-ttu-id="d06b4-121">L’illustration suivante montre une vue agrandie d’une ellipse lissée.</span><span class="sxs-lookup"><span data-stu-id="d06b4-121">The following illustration shows an enlarged view of a smoothed ellipse.</span></span>

![illustration d’une ellipse constituée de différentes nuances de pixels bleus sur un arrière-plan blanc](images/aboutgdip02-art35.png)

<span data-ttu-id="d06b4-123">L’illustration suivante montre la même ellipse dans sa taille réelle, une fois sans anticrénelage et une fois avec l’anticrénelage.</span><span class="sxs-lookup"><span data-stu-id="d06b4-123">The following illustration shows the same ellipse in its actual size, once without antialiasing and once with antialiasing.</span></span>

![capture d’écran de deux ellipses : le premier avec anticrénelage apparaît correctement](images/aboutgdip02-art36.png)

<span data-ttu-id="d06b4-125">Pour dessiner des lignes et des courbes qui utilisent l’anticrénelage, créez un objet [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) et transmettez *SmoothingModeAntiAlias* à sa méthode [**Graphics :: SetSmoothingMode**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setsmoothingmode) .</span><span class="sxs-lookup"><span data-stu-id="d06b4-125">To draw lines and curves that use antialiasing, create a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and pass *SmoothingModeAntiAlias* to its [**Graphics::SetSmoothingMode**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setsmoothingmode) method.</span></span> <span data-ttu-id="d06b4-126">Appelez ensuite l’une des méthodes de dessin de ce même objet **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="d06b4-126">Then call one of the drawing methods of that same **Graphics** object.</span></span>


```
myGraphics.SetSmoothingMode(SmoothingModeAntiAlias);
myGraphics.DrawLine(&myPen, 0, 0, 12, 8);
```



<span data-ttu-id="d06b4-127">**SmoothingModeAntiAlias** est un élément de l’énumération [**SmoothingMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) .</span><span class="sxs-lookup"><span data-stu-id="d06b4-127">**SmoothingModeAntiAlias** is an element of the [**SmoothingMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) enumeration.</span></span>

 

 



