---
title: F (OpenGL)
description: Définitions des termes OpenGL qui commencent par la lettre F.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: ba960409-84e0-4ece-967b-97f0e1183956
keywords:
- visages
- ombrage plat
- brouillard
- polices
- fragments
- framebuffers
- face avant
- frustum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7085765a5585268acb2f20a77c72bdd7cf1b4b81
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106509695"
---
# <a name="f-opengl"></a><span data-ttu-id="e9e8a-111">F (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="e9e8a-111">F (OpenGL)</span></span>

<span data-ttu-id="e9e8a-112">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [e](e.md) F [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="e9e8a-112">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) F [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="e9e8a-113"><span id="opengl_face"></span><span id="OPENGL_FACE"></span>**se**</span><span class="sxs-lookup"><span data-stu-id="e9e8a-113"><span id="opengl_face"></span><span id="OPENGL_FACE"></span>**face**</span></span>
</dt> <dd>

<span data-ttu-id="e9e8a-114">Un côté d’un polygone.</span><span class="sxs-lookup"><span data-stu-id="e9e8a-114">One side of a polygon.</span></span> <span data-ttu-id="e9e8a-115">Chaque polygone a deux visages : une face avant et une face arrière.</span><span class="sxs-lookup"><span data-stu-id="e9e8a-115">Each polygon has two faces: a front face and a back face.</span></span> <span data-ttu-id="e9e8a-116">Une seule face est toujours visible dans la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e9e8a-116">Only one face is ever visible in the window.</span></span> <span data-ttu-id="e9e8a-117">La visibilité de la face arrière ou de l’avant est déterminée une fois que le polygone est projeté dans la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e9e8a-117">Whether the back or front face is visible is effectively determined after the polygon is projected onto the window.</span></span> <span data-ttu-id="e9e8a-118">Après cette projection, si les bords du polygone sont dirigés dans le sens des aiguilles d’une montre, l’une des faces est visible. s’il est dirigé vers le sens inverse des aiguilles d’une représente, l’autre visage est visible.</span><span class="sxs-lookup"><span data-stu-id="e9e8a-118">After this projection, if the polygon's edges are directed clockwise, one of the faces is visible; if directed counterclockwise, the other face is visible.</span></span> <span data-ttu-id="e9e8a-119">Que le sens horaire corresponde à l’avant ou à l’arrière (et dans le sens inverse, à l’arrière ou à l’avant) est déterminé par le programmeur OpenGL.</span><span class="sxs-lookup"><span data-stu-id="e9e8a-119">Whether clockwise corresponds to front or back (and counterclockwise corresponds to back or front) is determined by the OpenGL programmer.</span></span>

</dd> <dt>

<span data-ttu-id="e9e8a-120"><span id="opengl_flat_shading"></span><span id="OPENGL_FLAT_SHADING"></span>**ombrage plat**</span><span class="sxs-lookup"><span data-stu-id="e9e8a-120"><span id="opengl_flat_shading"></span><span id="OPENGL_FLAT_SHADING"></span>**flat shading**</span></span>
</dt> <dd>

<span data-ttu-id="e9e8a-121">Fait référence à la coloration d’une primitive avec une couleur constante unique dans son étendue, plutôt que de lisser l’interpolation des couleurs sur l’ensemble de la primitive.</span><span class="sxs-lookup"><span data-stu-id="e9e8a-121">Refers to coloring a primitive with a single, constant color across its extent, rather than smoothly interpolating colors across the primitive.</span></span> <span data-ttu-id="e9e8a-122">Consultez l' [Ombrage Gouraud](g.md).</span><span class="sxs-lookup"><span data-stu-id="e9e8a-122">See [Gouraud shading](g.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9e8a-123"><span id="opengl_fog"></span><span id="OPENGL_FOG"></span>**vont**</span><span class="sxs-lookup"><span data-stu-id="e9e8a-123"><span id="opengl_fog"></span><span id="OPENGL_FOG"></span>**fog**</span></span>
</dt> <dd>

<span data-ttu-id="e9e8a-124">Technique de rendu qui peut être utilisée pour simuler des effets atmosphériques, tels que le trouble, le brouillard et les smog en confondant les couleurs des objets sur une couleur d’arrière-plan en fonction de la distance par rapport à la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="e9e8a-124">A rendering technique that can be used to simulate atmospheric effects such as haze, fog, and smog by fading object colors to a background color based on distance from the viewer.</span></span> <span data-ttu-id="e9e8a-125">Le brouillard facilite également la perception de la distance par rapport à la visionneuse, en donnant un repère de profondeur.</span><span class="sxs-lookup"><span data-stu-id="e9e8a-125">Fog also aids in the perception of distance from the viewer, giving a depth cue.</span></span> <span data-ttu-id="e9e8a-126">Voir aussi [profondeur-cueing](d.md).</span><span class="sxs-lookup"><span data-stu-id="e9e8a-126">See also [depth-cueing](d.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9e8a-127"><span id="opengl_font"></span><span id="OPENGL_FONT"></span>**son**</span><span class="sxs-lookup"><span data-stu-id="e9e8a-127"><span id="opengl_font"></span><span id="OPENGL_FONT"></span>**font**</span></span>
</dt> <dd>

<span data-ttu-id="e9e8a-128">Groupe de représentations de caractères graphiques généralement utilisé pour afficher des chaînes de texte.</span><span class="sxs-lookup"><span data-stu-id="e9e8a-128">A group of graphical character representations usually used to display strings of text.</span></span> <span data-ttu-id="e9e8a-129">Les caractères peuvent être des lettres latines, des symboles mathématiques, des idéogrammes asiatiques, des Hieroglyphs égyptiennes, etc.</span><span class="sxs-lookup"><span data-stu-id="e9e8a-129">The characters may be roman letters, mathematical symbols, Asian ideograms, Egyptian hieroglyphs, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="e9e8a-130"><span id="opengl_fragment"></span><span id="OPENGL_FRAGMENT"></span>**échantillon**</span><span class="sxs-lookup"><span data-stu-id="e9e8a-130"><span id="opengl_fragment"></span><span id="OPENGL_FRAGMENT"></span>**fragment**</span></span>
</dt> <dd>

<span data-ttu-id="e9e8a-131">Données graphiques générées par la pixellisation des primitives.</span><span class="sxs-lookup"><span data-stu-id="e9e8a-131">Graphic data generated by the rasterization of primitives.</span></span> <span data-ttu-id="e9e8a-132">Chaque fragment correspond à un pixel unique et comprend des valeurs de couleur, de profondeur et parfois de coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="e9e8a-132">Each fragment corresponds to a single pixel and includes color, depth, and sometimes texture-coordinate values.</span></span>

</dd> <dt>

<span data-ttu-id="e9e8a-133"><span id="opengl_framebuffer"></span><span id="OPENGL_FRAMEBUFFER"></span>**trame**</span><span class="sxs-lookup"><span data-stu-id="e9e8a-133"><span id="opengl_framebuffer"></span><span id="OPENGL_FRAMEBUFFER"></span>**framebuffer**</span></span>
</dt> <dd>

<span data-ttu-id="e9e8a-134">Pile de bitplanes.</span><span class="sxs-lookup"><span data-stu-id="e9e8a-134">A stack of bitplanes.</span></span> <span data-ttu-id="e9e8a-135">Toutes les mémoires tampons d’une fenêtre ou d’un contexte donnés.</span><span class="sxs-lookup"><span data-stu-id="e9e8a-135">All the buffers of a given window or context.</span></span> <span data-ttu-id="e9e8a-136">Comprend parfois la mémoire en pixels de l’accélérateur matériel Graphics.</span><span class="sxs-lookup"><span data-stu-id="e9e8a-136">Sometimes includes all the pixel memory of the graphics hardware accelerator.</span></span> <span data-ttu-id="e9e8a-137">Voir aussi [Bitplane](b.md).</span><span class="sxs-lookup"><span data-stu-id="e9e8a-137">See also [bitplane](b.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9e8a-138"><span id="opengl_front_face"></span><span id="OPENGL_FRONT_FACE"></span>**face avant**</span><span class="sxs-lookup"><span data-stu-id="e9e8a-138"><span id="opengl_front_face"></span><span id="OPENGL_FRONT_FACE"></span>**front face**</span></span>
</dt> <dd>

<span data-ttu-id="e9e8a-139">Consultez la section face.</span><span class="sxs-lookup"><span data-stu-id="e9e8a-139">See face.</span></span>

</dd> <dt>

<span data-ttu-id="e9e8a-140"><span id="opengl_frustum"></span><span id="OPENGL_FRUSTUM"></span>**frustum**</span><span class="sxs-lookup"><span data-stu-id="e9e8a-140"><span id="opengl_frustum"></span><span id="OPENGL_FRUSTUM"></span>**frustum**</span></span>
</dt> <dd>

<span data-ttu-id="e9e8a-141">Le volume de la vue déformé par la Division de perspective.</span><span class="sxs-lookup"><span data-stu-id="e9e8a-141">The view volume warped by perspective division.</span></span>

</dd> </dl>

 

 




