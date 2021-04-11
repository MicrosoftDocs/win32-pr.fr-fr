---
title: T (OpenGL)
description: Définitions des termes OpenGL qui commencent par la lettre T.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: effb170b-fea3-4954-9f9c-3bc1aa829bc0
keywords:
- mosaïque
- Texel
- texture
- mappage de texture
- matrice de texture
- transformations
- triangles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1cb324179137dbf9f9046c0c19acfffdf7394e1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102656"
---
# <a name="t-opengl"></a><span data-ttu-id="12c68-110">T (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="12c68-110">T (OpenGL)</span></span>

<span data-ttu-id="12c68-111">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [e](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) T [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="12c68-111">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) T [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="12c68-112"><span id="opengl_tessellation"></span><span id="OPENGL_TESSELLATION"></span>**mosaïque**</span><span class="sxs-lookup"><span data-stu-id="12c68-112"><span id="opengl_tessellation"></span><span id="OPENGL_TESSELLATION"></span>**tessellation**</span></span>
</dt> <dd>

<span data-ttu-id="12c68-113">Réduction d’une partie d’une surface analytique à un maillage de polygones ou d’une partie d’une courbe analytique à une séquence de lignes.</span><span class="sxs-lookup"><span data-stu-id="12c68-113">Reduction of a portion of an analytic surface to a mesh of polygons, or of a portion of an analytic curve to a sequence of lines.</span></span>

</dd> <dt>

<span data-ttu-id="12c68-114"><span id="opengl_texel"></span><span id="OPENGL_TEXEL"></span>**Texel**</span><span class="sxs-lookup"><span data-stu-id="12c68-114"><span id="opengl_texel"></span><span id="OPENGL_TEXEL"></span>**texel**</span></span>
</dt> <dd>

<span data-ttu-id="12c68-115">Élément de texture.</span><span class="sxs-lookup"><span data-stu-id="12c68-115">A texture element.</span></span> <span data-ttu-id="12c68-116">Un Texel est obtenu à partir de la mémoire de texture et représente la couleur de la texture à appliquer à un fragment correspondant.</span><span class="sxs-lookup"><span data-stu-id="12c68-116">A texel is obtained from texture memory and represents the color of the texture to be applied to a corresponding fragment.</span></span> <span data-ttu-id="12c68-117">Voir aussi [fragment](f.md).</span><span class="sxs-lookup"><span data-stu-id="12c68-117">See also [fragment](f.md).</span></span>

</dd> <dt>

<span data-ttu-id="12c68-118"><span id="opengl_texture"></span><span id="OPENGL_TEXTURE"></span>**motif**</span><span class="sxs-lookup"><span data-stu-id="12c68-118"><span id="opengl_texture"></span><span id="OPENGL_TEXTURE"></span>**texture**</span></span>
</dt> <dd>

<span data-ttu-id="12c68-119">Image à une ou deux dimensions utilisée pour modifier la couleur des fragments produits par la pixellisation.</span><span class="sxs-lookup"><span data-stu-id="12c68-119">A one- or two-dimensional image used to modify the color of fragments produced by rasterization.</span></span> <span data-ttu-id="12c68-120">Voir aussi [pixellisation](r.md).</span><span class="sxs-lookup"><span data-stu-id="12c68-120">See also [rasterize](r.md).</span></span>

</dd> <dt>

<span data-ttu-id="12c68-121"><span id="opengl_texture_mapping"></span><span id="OPENGL_TEXTURE_MAPPING"></span>**mappage de texture**</span><span class="sxs-lookup"><span data-stu-id="12c68-121"><span id="opengl_texture_mapping"></span><span id="OPENGL_TEXTURE_MAPPING"></span>**texture mapping**</span></span>
</dt> <dd>

<span data-ttu-id="12c68-122">Processus d’application d’une image (la texture) à une primitive.</span><span class="sxs-lookup"><span data-stu-id="12c68-122">The process of applying an image (the texture) to a primitive.</span></span> <span data-ttu-id="12c68-123">Le mappage de texture est souvent utilisé pour ajouter un réalisme à une scène.</span><span class="sxs-lookup"><span data-stu-id="12c68-123">Texture mapping is often used to add realism to a scene.</span></span> <span data-ttu-id="12c68-124">Par exemple, vous pouvez appliquer une image d’une façade de bâtiment à un polygone représentant un mur.</span><span class="sxs-lookup"><span data-stu-id="12c68-124">For example, you could apply a picture of a building facade to a polygon representing a wall.</span></span> <span data-ttu-id="12c68-125">Voir aussi texture.</span><span class="sxs-lookup"><span data-stu-id="12c68-125">See also texture.</span></span>

</dd> <dt>

<span data-ttu-id="12c68-126"><span id="opengl_texture_matrix"></span><span id="OPENGL_TEXTURE_MATRIX"></span>**matrice de texture**</span><span class="sxs-lookup"><span data-stu-id="12c68-126"><span id="opengl_texture_matrix"></span><span id="OPENGL_TEXTURE_MATRIX"></span>**texture matrix**</span></span>
</dt> <dd>

<span data-ttu-id="12c68-127">Matrice 4x4 qui transforme les coordonnées de texture des coordonnées qu’elles spécifient en coordonnées utilisées pour l’interpolation et la recherche de texture.</span><span class="sxs-lookup"><span data-stu-id="12c68-127">The 4x4 matrix that transforms texture coordinates from the coordinates that they're specified in to the coordinates that are used for interpolation and texture lookup.</span></span>

</dd> <dt>

<span data-ttu-id="12c68-128"><span id="opengl_transformation"></span><span id="OPENGL_TRANSFORMATION"></span>**DTS**</span><span class="sxs-lookup"><span data-stu-id="12c68-128"><span id="opengl_transformation"></span><span id="OPENGL_TRANSFORMATION"></span>**transformation**</span></span>
</dt> <dd>

<span data-ttu-id="12c68-129">Une distorsion de l’espace.</span><span class="sxs-lookup"><span data-stu-id="12c68-129">A warping of space.</span></span> <span data-ttu-id="12c68-130">Dans OpenGL, les transformations sont limitées aux transformations projective qui incluent tout ce qui peut être représenté par une matrice 4x4.</span><span class="sxs-lookup"><span data-stu-id="12c68-130">In OpenGL, transformations are limited to projective transformations that include anything that can be represented by a 4x4 matrix.</span></span> <span data-ttu-id="12c68-131">Ces transformations incluent les rotations, les translations, les mises à l’échelle (non uniformes) le long des axes de coordonnées, les transformations de perspective et les combinaisons de ces transformations.</span><span class="sxs-lookup"><span data-stu-id="12c68-131">Such transformations include rotations, translations, (nonuniform) scalings along the coordinate axes, perspective transformations, and combinations of these.</span></span>

</dd> <dt>

<span data-ttu-id="12c68-132"><span id="opengl_triangle"></span><span id="OPENGL_TRIANGLE"></span>**placé**</span><span class="sxs-lookup"><span data-stu-id="12c68-132"><span id="opengl_triangle"></span><span id="OPENGL_TRIANGLE"></span>**triangle**</span></span>
</dt> <dd>

<span data-ttu-id="12c68-133">Polygone avec trois bords.</span><span class="sxs-lookup"><span data-stu-id="12c68-133">A polygon with three edges.</span></span> <span data-ttu-id="12c68-134">Les triangles sont toujours convexes.</span><span class="sxs-lookup"><span data-stu-id="12c68-134">Triangles are always convex.</span></span>

</dd> </dl>

 

 




