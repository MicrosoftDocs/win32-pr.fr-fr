---
description: Un chemin d’accès est une séquence de primitives graphiques (lignes, rectangles, courbes, texte et autres) qui peuvent être manipulées et dessinées en tant qu’unité unique. Un chemin d’accès peut être divisé en figures ouvertes ou fermées. Une figure peut contenir plusieurs Primitives.
ms.assetid: dbfe8cea-bd9e-43ad-85c8-37cce3ef97a4
title: Génération et dessin de tracés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fe5f1528e58e3df19afbc83bb6acfdc2a6fca19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991376"
---
# <a name="constructing-and-drawing-paths"></a><span data-ttu-id="c3a88-105">Génération et dessin de tracés</span><span class="sxs-lookup"><span data-stu-id="c3a88-105">Constructing and Drawing Paths</span></span>

<span data-ttu-id="c3a88-106">Un chemin d’accès est une séquence de primitives graphiques (lignes, rectangles, courbes, texte et autres) qui peuvent être manipulées et dessinées en tant qu’unité unique.</span><span class="sxs-lookup"><span data-stu-id="c3a88-106">A path is a sequence of graphics primitives (lines, rectangles, curves, text, and the like) that can be manipulated and drawn as a single unit.</span></span> <span data-ttu-id="c3a88-107">Un chemin d’accès peut être divisé en *figures* ouvertes ou fermées.</span><span class="sxs-lookup"><span data-stu-id="c3a88-107">A path can be divided into *figures* that are either open or closed.</span></span> <span data-ttu-id="c3a88-108">Une figure peut contenir plusieurs Primitives.</span><span class="sxs-lookup"><span data-stu-id="c3a88-108">A figure can contain several primitives.</span></span>

<span data-ttu-id="c3a88-109">Vous pouvez dessiner un tracé en appelant la méthode [**Graphics ::D rawpath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) de la classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , et vous pouvez remplir un chemin d’accès en appelant la méthode [**Graphics :: FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) de la classe **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="c3a88-109">You can draw a path by calling the [**Graphics::DrawPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) method of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class, and you can fill a path by calling the [**Graphics::FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) method of the **Graphics** class.</span></span>

<span data-ttu-id="c3a88-110">Les rubriques suivantes traitent des chemins plus en détail :</span><span class="sxs-lookup"><span data-stu-id="c3a88-110">The following topics cover paths in more detail:</span></span>

-   [<span data-ttu-id="c3a88-111">Création de figures à partir de lignes, de courbes et de formes</span><span class="sxs-lookup"><span data-stu-id="c3a88-111">Creating Figures from Lines, Curves, and Shapes</span></span>](-gdiplus-creating-figures-from-lines-curves-and-shapes-use.md)
-   [<span data-ttu-id="c3a88-112">Remplissage des figures ouvertes</span><span class="sxs-lookup"><span data-stu-id="c3a88-112">Filling Open Figures</span></span>](-gdiplus-filling-open-figures-use.md)

 

 



