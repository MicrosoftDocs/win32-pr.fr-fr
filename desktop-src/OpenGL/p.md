---
title: P (OpenGL)
description: Définitions des termes OpenGL qui commencent par la lettre P.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: bc7b0c93-af06-44a4-8bb8-adc0c6fedb6e
keywords:
- parameters
- Division de perspective
- pixels
- points
- polygones
- Primitives
- matrices de projection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9970b3eb84920184e693ace93b14120828573e30
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103941585"
---
# <a name="p-opengl"></a><span data-ttu-id="ddb60-110">P (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="ddb60-110">P (OpenGL)</span></span>

<span data-ttu-id="ddb60-111">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [e](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) P [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="ddb60-111">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) P [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="ddb60-112"><span id="opengl_parameter"></span><span id="OPENGL_PARAMETER"></span>**paramètre**</span><span class="sxs-lookup"><span data-stu-id="ddb60-112"><span id="opengl_parameter"></span><span id="OPENGL_PARAMETER"></span>**parameter**</span></span>
</dt> <dd>

<span data-ttu-id="ddb60-113">Valeur passée comme argument à une commande OpenGL.</span><span class="sxs-lookup"><span data-stu-id="ddb60-113">A value passed as an argument to an OpenGL command.</span></span> <span data-ttu-id="ddb60-114">Parfois, l’une des valeurs passées par référence à une commande OpenGL.</span><span class="sxs-lookup"><span data-stu-id="ddb60-114">Sometimes one of the values passed by reference to an OpenGL command.</span></span>

</dd> <dt>

<span data-ttu-id="ddb60-115"><span id="opengl_perspective_division"></span><span id="OPENGL_PERSPECTIVE_DIVISION"></span>**Division de perspective**</span><span class="sxs-lookup"><span data-stu-id="ddb60-115"><span id="opengl_perspective_division"></span><span id="OPENGL_PERSPECTIVE_DIVISION"></span>**perspective division**</span></span>
</dt> <dd>

<span data-ttu-id="ddb60-116">Division de x, y et z par w, effectuée en coordonnées de clip.</span><span class="sxs-lookup"><span data-stu-id="ddb60-116">The division of x, y, and z by w, carried out in clip coordinates.</span></span> <span data-ttu-id="ddb60-117">Voir aussi [coordonnées](c.md)de l’élément.</span><span class="sxs-lookup"><span data-stu-id="ddb60-117">See also [clip coordinates](c.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddb60-118"><span id="opengl_pixel"></span><span id="OPENGL_PIXEL"></span>**pixellisé**</span><span class="sxs-lookup"><span data-stu-id="ddb60-118"><span id="opengl_pixel"></span><span id="OPENGL_PIXEL"></span>**pixel**</span></span>
</dt> <dd>

<span data-ttu-id="ddb60-119">Élément image.</span><span class="sxs-lookup"><span data-stu-id="ddb60-119">Picture element.</span></span> <span data-ttu-id="ddb60-120">Les bits à l’emplacement (x, y) de tous les bitplanes dans le trame constituent le pixel unique (x, y).</span><span class="sxs-lookup"><span data-stu-id="ddb60-120">The bits at location (x, y) of all the bitplanes in the framebuffer constitute the single pixel (x, y).</span></span> <span data-ttu-id="ddb60-121">Dans une image de la mémoire du client, un pixel est un groupe d’éléments.</span><span class="sxs-lookup"><span data-stu-id="ddb60-121">In an image in client memory, a pixel is one group of elements.</span></span> <span data-ttu-id="ddb60-122">Dans les coordonnées de fenêtre OpenGL, chaque pixel correspond à une zone d’écran 1.0 x 1.0.</span><span class="sxs-lookup"><span data-stu-id="ddb60-122">In OpenGL window coordinates, each pixel corresponds to a 1.0x1.0 screen area.</span></span> <span data-ttu-id="ddb60-123">Les coordonnées de l’angle inférieur gauche des noms de Pixel x, y sont (x, y) et le coin supérieur droit sont (x + 1, y + 1).</span><span class="sxs-lookup"><span data-stu-id="ddb60-123">The coordinates of the lower-left corner of the pixel names x, y are (x, y), and the upper-right corner are (x+1, y+1).</span></span>

</dd> <dt>

<span data-ttu-id="ddb60-124"><span id="opengl_point"></span><span id="OPENGL_POINT"></span>**point**</span><span class="sxs-lookup"><span data-stu-id="ddb60-124"><span id="opengl_point"></span><span id="OPENGL_POINT"></span>**point**</span></span>
</dt> <dd>

<span data-ttu-id="ddb60-125">Emplacement exact dans l’espace, qui est rendu sous la forme d’un point de diamètre fini.</span><span class="sxs-lookup"><span data-stu-id="ddb60-125">An exact location in space, which is rendered as a finite-diameter dot.</span></span>

</dd> <dt>

<span data-ttu-id="ddb60-126"><span id="opengl_polygon"></span><span id="OPENGL_POLYGON"></span>**Polygone**</span><span class="sxs-lookup"><span data-stu-id="ddb60-126"><span id="opengl_polygon"></span><span id="OPENGL_POLYGON"></span>**polygon**</span></span>
</dt> <dd>

<span data-ttu-id="ddb60-127">Surface quasi-planaire délimitée par des arêtes spécifiées par des sommets.</span><span class="sxs-lookup"><span data-stu-id="ddb60-127">A near-planar surface bounded by edges specified by vertices.</span></span> <span data-ttu-id="ddb60-128">Chaque triangle d’un maillage de triangle est un polygone, comme chaque quadrilatère d’un filet quadrangulaires.</span><span class="sxs-lookup"><span data-stu-id="ddb60-128">Each triangle of a triangle mesh is a polygon, as is each quadrilateral of a quadrilateral mesh.</span></span> <span data-ttu-id="ddb60-129">Le rectangle spécifié par glRect est également un polygone.</span><span class="sxs-lookup"><span data-stu-id="ddb60-129">The rectangle specified by glRect is also a polygon.</span></span>

</dd> <dt>

<span data-ttu-id="ddb60-130"><span id="opengl_primitive"></span><span id="OPENGL_PRIMITIVE"></span>**primitifs**</span><span class="sxs-lookup"><span data-stu-id="ddb60-130"><span id="opengl_primitive"></span><span id="OPENGL_PRIMITIVE"></span>**primitive**</span></span>
</dt> <dd>

<span data-ttu-id="ddb60-131">Forme (telle qu’un point, une ligne, un polygone, une image bitmap ou une image) qui peut être dessinée, stockée et manipulée en tant qu’entité discrète ; éléments à partir desquels les conceptions graphiques volumineuses sont créées.</span><span class="sxs-lookup"><span data-stu-id="ddb60-131">A shape (such as a point, line, polygon, bitmap, or image) that can be drawn, stored, and manipulated as a discrete entity; elements from which large graphic designs are created.</span></span>

</dd> <dt>

<span data-ttu-id="ddb60-132"><span id="opengl_projection_matrix"></span><span id="OPENGL_PROJECTION_MATRIX"></span>**matrice de projection**</span><span class="sxs-lookup"><span data-stu-id="ddb60-132"><span id="opengl_projection_matrix"></span><span id="OPENGL_PROJECTION_MATRIX"></span>**projection matrix**</span></span>
</dt> <dd>

<span data-ttu-id="ddb60-133">Matrice 4x4 qui transforme des points, des lignes, des polygones et des positions raster des coordonnées oculaires aux coordonnées de l’élément.</span><span class="sxs-lookup"><span data-stu-id="ddb60-133">The 4x4 matrix that transforms points, lines, polygons, and raster positions from eye coordinates to clip coordinates.</span></span>

</dd> </dl>

 

 




