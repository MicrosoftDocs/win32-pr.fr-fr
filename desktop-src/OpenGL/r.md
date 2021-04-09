---
title: R (OpenGL)
description: Définitions des termes OpenGL qui commencent par la lettre R.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: ab0286f5-cad2-4537-aa98-be0fce55ff53
keywords:
- rastérisation
- rectangles
- rendu
- RGBA
- Mode RVBA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b82a2db1bade12a0ff844006a1572cdc3b977dd
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103842970"
---
# <a name="r-opengl"></a><span data-ttu-id="8ea0d-108">R (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="8ea0d-108">R (OpenGL)</span></span>

<span data-ttu-id="8ea0d-109">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [e](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) R [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="8ea0d-109">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) R [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="8ea0d-110"><span id="opengl_rasterize"></span><span id="OPENGL_RASTERIZE"></span>**rastérisation**</span><span class="sxs-lookup"><span data-stu-id="8ea0d-110"><span id="opengl_rasterize"></span><span id="OPENGL_RASTERIZE"></span>**rasterize**</span></span>
</dt> <dd>

<span data-ttu-id="8ea0d-111">Pour convertir un point, une ligne ou un polygone projeté, ou les pixels d’une bitmap ou d’une image, en fragments, chacun correspondant à un pixel dans le trame.</span><span class="sxs-lookup"><span data-stu-id="8ea0d-111">To convert a projected point, line, or polygon, or the pixels of a bitmap or image, to fragments, each corresponding to a pixel in the framebuffer.</span></span> <span data-ttu-id="8ea0d-112">Notez que toutes les primitives sont pixellisées, pas seulement des points, des lignes et des polygones</span><span class="sxs-lookup"><span data-stu-id="8ea0d-112">Note that all primitives are rasterized, not just points, lines, and polygons</span></span>

</dd> <dt>

<span data-ttu-id="8ea0d-113"><span id="opengl_rectangle"></span><span id="OPENGL_RECTANGLE"></span>**Rectangle**</span><span class="sxs-lookup"><span data-stu-id="8ea0d-113"><span id="opengl_rectangle"></span><span id="OPENGL_RECTANGLE"></span>**rectangle**</span></span>
</dt> <dd>

<span data-ttu-id="8ea0d-114">Quadrilatère dont les bords secondaires sont parallèles les uns aux autres dans les coordonnées d’objet.</span><span class="sxs-lookup"><span data-stu-id="8ea0d-114">A quadrilateral whose alternate edges are parallel to each other in object coordinates.</span></span> <span data-ttu-id="8ea0d-115">Les polygones spécifiés avec glRect \* () sont toujours des rectangles ; d’autres quadrilatères peuvent être des rectangles.</span><span class="sxs-lookup"><span data-stu-id="8ea0d-115">Polygons specified with glRect\*( ) are always rectangles; other quadrilaterals might be rectangles.</span></span>

</dd> <dt>

<span data-ttu-id="8ea0d-116"><span id="opengl_rendering"></span><span id="OPENGL_RENDERING"></span>**rendu**</span><span class="sxs-lookup"><span data-stu-id="8ea0d-116"><span id="opengl_rendering"></span><span id="OPENGL_RENDERING"></span>**rendering**</span></span>
</dt> <dd>

<span data-ttu-id="8ea0d-117">Conversion de primitives spécifiées en coordonnées d’objets en image dans le trame.</span><span class="sxs-lookup"><span data-stu-id="8ea0d-117">Conversion of primitives specified in object coordinates to an image in the framebuffer.</span></span> <span data-ttu-id="8ea0d-118">Le rendu est l’opération principale de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="8ea0d-118">Rendering is the primary operation of OpenGL.</span></span>

</dd> <dt>

<span data-ttu-id="8ea0d-119"><span id="opengl_rgba"></span><span id="OPENGL_RGBA"></span>**RGBA**</span><span class="sxs-lookup"><span data-stu-id="8ea0d-119"><span id="opengl_rgba"></span><span id="OPENGL_RGBA"></span>**RGBA**</span></span>
</dt> <dd>

<span data-ttu-id="8ea0d-120">Composants de couleur rouge, vert, bleu et alpha du mode RVBA.</span><span class="sxs-lookup"><span data-stu-id="8ea0d-120">The red, green, blue, and alpha color components of the RGBA mode.</span></span>

</dd> <dt>

<span data-ttu-id="8ea0d-121"><span id="opengl_rgba_mode"></span><span id="OPENGL_RGBA_MODE"></span>**Mode RVBA**</span><span class="sxs-lookup"><span data-stu-id="8ea0d-121"><span id="opengl_rgba_mode"></span><span id="OPENGL_RGBA_MODE"></span>**RGBA mode**</span></span>
</dt> <dd>

<span data-ttu-id="8ea0d-122">Contexte OpenGL dans lequel ses mémoires tampons de couleurs stockent les composants de couleur rouge, vert, bleu et alpha, plutôt que les index de couleurs.</span><span class="sxs-lookup"><span data-stu-id="8ea0d-122">An OpenGL context in which its color buffers store red, green, blue, and alpha color components, rather than color indexes.</span></span>

</dd> </dl>

 

 




