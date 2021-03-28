---
description: 'La classe Graphics fournit diverses méthodes de dessin, y compris celles répertoriées dans la liste suivante :'
ms.assetid: d3c8d16c-858a-42a9-a512-3fcfa144f5fc
title: Utilisation d'un stylet pour dessiner des lignes et des formes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 904f53149038d6109365adddc11d3c37881a8def
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112938"
---
# <a name="using-a-pen-to-draw-lines-and-shapes"></a><span data-ttu-id="0024c-103">Utilisation d'un stylet pour dessiner des lignes et des formes</span><span class="sxs-lookup"><span data-stu-id="0024c-103">Using a Pen to Draw Lines and Shapes</span></span>

<span data-ttu-id="0024c-104">La classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) fournit diverses méthodes de dessin, y compris celles répertoriées dans la liste suivante :</span><span class="sxs-lookup"><span data-stu-id="0024c-104">The [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class provides a variety of drawing methods including those shown in the following list:</span></span>

-   <span data-ttu-id="0024c-105">[Méthodes DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint))</span><span class="sxs-lookup"><span data-stu-id="0024c-105">[DrawLine Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint))</span></span>
-   <span data-ttu-id="0024c-106">[Méthodes DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inconstrectf_))</span><span class="sxs-lookup"><span data-stu-id="0024c-106">[DrawRectangle Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inconstrectf_))</span></span>
-   <span data-ttu-id="0024c-107">[DrawEllipse (méthodes)](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrectf_))</span><span class="sxs-lookup"><span data-stu-id="0024c-107">[DrawEllipse Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrectf_))</span></span>
-   <span data-ttu-id="0024c-108">[Méthodes DrawArc](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inconstrectf__inreal_inreal))</span><span class="sxs-lookup"><span data-stu-id="0024c-108">[DrawArc Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inconstrectf__inreal_inreal))</span></span>
-   [<span data-ttu-id="0024c-109">**Graphics ::D rawPath**</span><span class="sxs-lookup"><span data-stu-id="0024c-109">**Graphics::DrawPath**</span></span>](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath)
-   <span data-ttu-id="0024c-110">[DrawCurve, méthodes](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcurve(inconstpen_inconstpoint_inint))</span><span class="sxs-lookup"><span data-stu-id="0024c-110">[DrawCurve Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcurve(inconstpen_inconstpoint_inint))</span></span>
-   <span data-ttu-id="0024c-111">[DrawBezier, méthodes](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbezier(inconstpen_inconstpointf__inconstpointf__inconstpointf__inconstpointf_))</span><span class="sxs-lookup"><span data-stu-id="0024c-111">[DrawBezier Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbezier(inconstpen_inconstpointf__inconstpointf__inconstpointf__inconstpointf_))</span></span>

<span data-ttu-id="0024c-112">L’un des arguments que vous transmettez à une telle méthode de dessin est l’adresse d’un objet [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="0024c-112">One of the arguments that you pass to such a drawing method is the address of a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object.</span></span>

<span data-ttu-id="0024c-113">Les rubriques suivantes traitent de l’utilisation des stylets plus en détail :</span><span class="sxs-lookup"><span data-stu-id="0024c-113">The following topics cover the use of pens in more detail:</span></span>

-   [<span data-ttu-id="0024c-114">Utilisation d’un stylo pour tracer des lignes et des rectangles</span><span class="sxs-lookup"><span data-stu-id="0024c-114">Using a Pen to Draw Lines and Rectangles</span></span>](-gdiplus-using-a-pen-to-draw-lines-and-rectangles-use.md)
-   [<span data-ttu-id="0024c-115">Définition de la largeur et de l’alignement du stylet</span><span class="sxs-lookup"><span data-stu-id="0024c-115">Setting Pen Width and Alignment</span></span>](-gdiplus-setting-pen-width-and-alignment-use.md)
-   [<span data-ttu-id="0024c-116">Dessin d’une ligne avec des embouts de ligne</span><span class="sxs-lookup"><span data-stu-id="0024c-116">Drawing a Line with Line Caps</span></span>](-gdiplus-drawing-a-line-with-line-caps-use.md)
-   [<span data-ttu-id="0024c-117">Joindre des lignes</span><span class="sxs-lookup"><span data-stu-id="0024c-117">Joining Lines</span></span>](-gdiplus-joining-lines-use.md)
-   [<span data-ttu-id="0024c-118">Dessin d’une ligne en pointillés personnalisée</span><span class="sxs-lookup"><span data-stu-id="0024c-118">Drawing a Custom Dashed Line</span></span>](-gdiplus-drawing-a-custom-dashed-line-use.md)
-   [<span data-ttu-id="0024c-119">Dessin d’une ligne remplie d’une texture</span><span class="sxs-lookup"><span data-stu-id="0024c-119">Drawing a Line Filled with a Texture</span></span>](-gdiplus-drawing-a-line-filled-with-a-texture-use.md)

 

 



