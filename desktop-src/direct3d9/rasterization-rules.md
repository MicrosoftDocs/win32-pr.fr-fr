---
description: Souvent, les points spécifiés pour les vertex ne correspondent pas exactement aux pixels de l’écran. Dans ce cas, Direct3D applique les règles de pixellisation des triangles pour décider quels pixels s’appliquent à un triangle donné.
ms.assetid: 919b36f1-d4de-4d5d-ba1a-0605bf59a6cd
title: Règles de pixellisation (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5115b2f12e0064202fcbca58f52cb163166d0a82
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104211158"
---
# <a name="rasterization-rules-direct3d-9"></a><span data-ttu-id="827c2-104">Règles de pixellisation (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="827c2-104">Rasterization Rules (Direct3D 9)</span></span>

<span data-ttu-id="827c2-105">Souvent, les points spécifiés pour les vertex ne correspondent pas exactement aux pixels de l’écran.</span><span class="sxs-lookup"><span data-stu-id="827c2-105">Often, the points specified for vertices do not precisely match the pixels on the screen.</span></span> <span data-ttu-id="827c2-106">Dans ce cas, Direct3D applique les règles de pixellisation des triangles pour décider quels pixels s’appliquent à un triangle donné.</span><span class="sxs-lookup"><span data-stu-id="827c2-106">When this happens, Direct3D applies triangle rasterization rules to decide which pixels apply to a given triangle.</span></span>

-   [<span data-ttu-id="827c2-107">Règles de pixellisation des triangles</span><span class="sxs-lookup"><span data-stu-id="827c2-107">Triangle Rasterization Rules</span></span>](#triangle-rasterization-rules)
-   [<span data-ttu-id="827c2-108">Règles de point et de ligne</span><span class="sxs-lookup"><span data-stu-id="827c2-108">Point and Line Rules</span></span>](#point-and-line-rules)
-   [<span data-ttu-id="827c2-109">Règles de point Sprite</span><span class="sxs-lookup"><span data-stu-id="827c2-109">Point Sprite Rules</span></span>](#point-sprite-rules)

## <a name="triangle-rasterization-rules"></a><span data-ttu-id="827c2-110">Règles de pixellisation des triangles</span><span class="sxs-lookup"><span data-stu-id="827c2-110">Triangle Rasterization Rules</span></span>

<span data-ttu-id="827c2-111">Direct3D utilise une convention de remplissage en haut à gauche pour remplir la géométrie.</span><span class="sxs-lookup"><span data-stu-id="827c2-111">Direct3D uses a top-left filling convention for filling geometry.</span></span> <span data-ttu-id="827c2-112">Il s’agit de la même convention que celle utilisée pour les rectangles dans GDI et OpenGL.</span><span class="sxs-lookup"><span data-stu-id="827c2-112">This is the same convention that is used for rectangles in GDI and OpenGL.</span></span> <span data-ttu-id="827c2-113">Dans Direct3D, le centre du pixel est le point déterminant.</span><span class="sxs-lookup"><span data-stu-id="827c2-113">In Direct3D, the center of the pixel is the decisive point.</span></span> <span data-ttu-id="827c2-114">Si le centre est à l’intérieur d’un triangle, le pixel fait partie du triangle.</span><span class="sxs-lookup"><span data-stu-id="827c2-114">If the center is inside a triangle, the pixel is part of the triangle.</span></span> <span data-ttu-id="827c2-115">Les centres de pixels sont des coordonnées entières.</span><span class="sxs-lookup"><span data-stu-id="827c2-115">Pixel centers are at integer coordinates.</span></span>

<span data-ttu-id="827c2-116">Cette description des règles de pixellisation des triangles utilisées par Direct3D ne s’applique pas nécessairement à tout le matériel disponible.</span><span class="sxs-lookup"><span data-stu-id="827c2-116">This description of triangle-rasterization rules used by Direct3D does not necessarily apply to all available hardware.</span></span> <span data-ttu-id="827c2-117">Vos tests peuvent découvrir des variations mineures dans l’implémentation de ces règles.</span><span class="sxs-lookup"><span data-stu-id="827c2-117">Your testing may uncover minor variations in the implementation of these rules.</span></span>

<span data-ttu-id="827c2-118">L’illustration suivante montre un rectangle dont l’angle supérieur gauche se trouve à (0,0) et dont l’angle inférieur droit est (5, 5).</span><span class="sxs-lookup"><span data-stu-id="827c2-118">The following illustration shows a rectangle whose upper-left corner is at (0, 0) and whose lower-right corner is at (5, 5).</span></span> <span data-ttu-id="827c2-119">Ce rectangle remplit 25 pixels, comme prévu.</span><span class="sxs-lookup"><span data-stu-id="827c2-119">This rectangle fills 25 pixels, just as you would expect.</span></span> <span data-ttu-id="827c2-120">La largeur du rectangle est définie à droite, moins gauche.</span><span class="sxs-lookup"><span data-stu-id="827c2-120">The width of the rectangle is defined as right minus left.</span></span> <span data-ttu-id="827c2-121">La hauteur est définie en tant que bas moins haut.</span><span class="sxs-lookup"><span data-stu-id="827c2-121">The height is defined as bottom minus top.</span></span>

![illustration d’un carré numéroté divisé en six lignes et colonnes](images/pixmap.png)

<span data-ttu-id="827c2-123">Dans la Convention de remplissage en haut à gauche, *Top* fait référence à l’emplacement vertical des étendues horizontales, tandis que *Left* fait référence à l’emplacement horizontal des pixels dans une étendue.</span><span class="sxs-lookup"><span data-stu-id="827c2-123">In the top-left filling convention, *top* refers to the vertical location of horizontal spans, and *left* refers to the horizontal location of pixels within a span.</span></span> <span data-ttu-id="827c2-124">Un bord ne peut pas être un bord supérieur, sauf s’il est horizontal.</span><span class="sxs-lookup"><span data-stu-id="827c2-124">An edge cannot be a top edge unless it is horizontal.</span></span> <span data-ttu-id="827c2-125">En général, la plupart des triangles ont uniquement des bords gauche et droit.</span><span class="sxs-lookup"><span data-stu-id="827c2-125">In general, most triangles have only left and right edges.</span></span> <span data-ttu-id="827c2-126">L’illustration suivante montre un bord supérieur et un bord droit.</span><span class="sxs-lookup"><span data-stu-id="827c2-126">The following illustration shows a top edge and a right edge.</span></span>

![illustration d’un carré numéroté qui contient deux triangles](images/triedge.png)

<span data-ttu-id="827c2-128">La Convention de remplissage en haut à gauche détermine l’action effectuée par Direct3D lorsqu’un triangle passe au centre d’un pixel.</span><span class="sxs-lookup"><span data-stu-id="827c2-128">The top-left filling convention determines the action taken by Direct3D when a triangle passes through the center of a pixel.</span></span> <span data-ttu-id="827c2-129">L’illustration suivante montre deux triangles, un à (0, 0), (5, 0) et (5, 5) et l’autre à (0, 5), (0, 0) et (5, 5).</span><span class="sxs-lookup"><span data-stu-id="827c2-129">The following illustration shows two triangles, one at (0, 0), (5, 0), and (5, 5), and the other at (0, 5), (0, 0), and (5, 5).</span></span> <span data-ttu-id="827c2-130">Dans ce cas, le premier triangle obtient 15 pixels (en noir), tandis que le second obtient uniquement 10 pixels (indiqué en gris), car la périphérie partagée est le bord gauche du premier triangle.</span><span class="sxs-lookup"><span data-stu-id="827c2-130">The first triangle in this case gets 15 pixels (shown in black), whereas the second gets only 10 pixels (shown in gray) because the shared edge is the left edge of the first triangle.</span></span>

![illustration d’un carré numéroté qui affiche deux triangles](images/twotris.png)

<span data-ttu-id="827c2-132">Si vous définissez un rectangle avec son coin supérieur gauche à (0,5, 0,5) et son coin inférieur droit à (2,5, 4,5), le point central de ce rectangle est (1,5, 2,5).</span><span class="sxs-lookup"><span data-stu-id="827c2-132">If you define a rectangle with its upper-left corner at (0.5, 0.5) and its lower-right corner at (2.5, 4.5), the center point of this rectangle is at (1.5, 2.5).</span></span> <span data-ttu-id="827c2-133">Lorsque le rastériseur Direct3D tessellates ce rectangle, le centre de chaque pixel est sans ambiguïté à l’intérieur de chacun des quatre triangles, et la Convention de remplissage supérieure gauche n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="827c2-133">When the Direct3D rasterizer tessellates this rectangle, the center of each pixel is unambiguously inside each of the four triangles, and the top-left filling convention is not needed.</span></span> <span data-ttu-id="827c2-134">L’illustration suivante montre cela.</span><span class="sxs-lookup"><span data-stu-id="827c2-134">The following illustration shows this.</span></span> <span data-ttu-id="827c2-135">Les pixels du rectangle sont étiquetés en fonction du triangle dans lequel Direct3D les intègre.</span><span class="sxs-lookup"><span data-stu-id="827c2-135">The pixels in the rectangle are labeled according to the triangle in which Direct3D includes them.</span></span>

![Affiche un carré numéroté qui contient un rectangle divisé en quatre triangles.](images/noambig.png)

<span data-ttu-id="827c2-137">Si vous déplacez le rectangle de l’illustration précédente afin que son coin supérieur gauche se trouve à l’emplacement (1,0, 1,0), à l’angle inférieur droit à (3,0, 5,0) et à son point central à (2,0, 3,0), Direct3D applique la Convention de remplissage en haut à gauche.</span><span class="sxs-lookup"><span data-stu-id="827c2-137">If you move the rectangle in the preceding illustration so that its upper-left corner is at (1.0, 1.0), its lower-right corner at (3.0, 5.0), and its center point at (2.0, 3.0), Direct3D applies the top-left filling convention.</span></span> <span data-ttu-id="827c2-138">La plupart des pixels de ce rectangle chevauchent la bordure entre deux ou plusieurs triangles, comme le montre l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="827c2-138">Most pixels in this rectangle straddle the border between two or more triangles, as the following illustration shows.</span></span>

![illustration d’un carré numéroté qui contient un rectangle divisé en quatre triangles](images/fillrule.png)

<span data-ttu-id="827c2-140">Pour les deux rectangles, les mêmes pixels sont affectés, comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="827c2-140">For both rectangles, the same pixels are affected, as shown in the following illustration.</span></span>

![illustration des pixels affectés par les deux carrés numérotés précédents](images/samepix.png)

## <a name="point-and-line-rules"></a><span data-ttu-id="827c2-142">Règles de point et de ligne</span><span class="sxs-lookup"><span data-stu-id="827c2-142">Point and Line Rules</span></span>

<span data-ttu-id="827c2-143">Les points sont restitués de la même façon que les points sprites, qui sont rendus sous forme de quadrilatères alignés sur l’écran et sont donc conformes aux mêmes règles que le rendu de polygones.</span><span class="sxs-lookup"><span data-stu-id="827c2-143">Points are rendered the same as point sprites, which are both rendered as screen-aligned quadrilaterals and thus adhere to the same rules as polygon rendering.</span></span>

<span data-ttu-id="827c2-144">Les règles de rendu de ligne sans anticrénelage sont exactement les mêmes que celles pour les [lignes GDI](../gdi/lines.md).</span><span class="sxs-lookup"><span data-stu-id="827c2-144">Non-antialiased line rendering rules are exactly the same as those for [GDI lines](../gdi/lines.md).</span></span>

<span data-ttu-id="827c2-145">Pour plus d’informations sur le rendu de ligne avec anticrénelage, consultez [**ID3DXLine**](id3dxline.md).</span><span class="sxs-lookup"><span data-stu-id="827c2-145">For information about antialiased line rendering, see [**ID3DXLine**](id3dxline.md).</span></span>

## <a name="point-sprite-rules"></a><span data-ttu-id="827c2-146">Règles de point Sprite</span><span class="sxs-lookup"><span data-stu-id="827c2-146">Point Sprite Rules</span></span>

<span data-ttu-id="827c2-147">Les points de soulignement et les primitives de correctif sont pixellisés comme si les primitives étaient d’abord fractionnées en triangles et les triangles obtenus pixellisés.</span><span class="sxs-lookup"><span data-stu-id="827c2-147">Point sprites and patch primitives are rasterized as if the primitives were first tessellated into triangles and the resulting triangles rasterized.</span></span> <span data-ttu-id="827c2-148">Pour plus d’informations, consultez [points sprites (Direct3D 9)](point-sprites.md).</span><span class="sxs-lookup"><span data-stu-id="827c2-148">For more information, see [Point Sprites (Direct3D 9)](point-sprites.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="827c2-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="827c2-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="827c2-150">Systèmes de coordonnées et géométrie</span><span class="sxs-lookup"><span data-stu-id="827c2-150">Coordinate Systems and Geometry</span></span>](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 
