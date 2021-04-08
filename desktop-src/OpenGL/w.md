---
title: W (OpenGL)
description: Définitions des termes OpenGL qui commencent par la lettre W.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 7f8235a3-ea48-40eb-8957-e7a55a5778af
keywords:
- windows
- alignée sur la fenêtre
- coordonnées de la fenêtre
- Wireframe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1f6f1897af46c85ed48171d251ebe1b2de8c5e1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739276"
---
# <a name="w-opengl"></a><span data-ttu-id="94e59-107">W (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="94e59-107">W (OpenGL)</span></span>

<span data-ttu-id="94e59-108">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [e](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) W [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="94e59-108">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) W [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="94e59-109"><span id="opengl_window"></span><span id="OPENGL_WINDOW"></span>**fenetre**</span><span class="sxs-lookup"><span data-stu-id="94e59-109"><span id="opengl_window"></span><span id="OPENGL_WINDOW"></span>**window**</span></span>
</dt> <dd>

<span data-ttu-id="94e59-110">Sous-région du trame, généralement rectangulaire, dont les pixels ont tous la même configuration de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="94e59-110">A subregion of the framebuffer, usually rectangular, whose pixels all have the same buffer configuration.</span></span> <span data-ttu-id="94e59-111">Un contexte OpenGL est restitué dans une fenêtre à la fois.</span><span class="sxs-lookup"><span data-stu-id="94e59-111">An OpenGL context renders to one window at a time.</span></span>

</dd> <dt>

<span data-ttu-id="94e59-112"><span id="opengl_window_aligned"></span><span id="OPENGL_WINDOW_ALIGNED"></span>**alignée sur la fenêtre**</span><span class="sxs-lookup"><span data-stu-id="94e59-112"><span id="opengl_window_aligned"></span><span id="OPENGL_WINDOW_ALIGNED"></span>**window-aligned**</span></span>
</dt> <dd>

<span data-ttu-id="94e59-113">Lorsque vous faites référence à des segments de ligne ou à des arêtes de polygones, implique qu’ils sont parallèles aux limites de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="94e59-113">When referring to line segments or polygon edges, implies that these are parallel to the window boundaries.</span></span> <span data-ttu-id="94e59-114">(Dans OpenGL, la fenêtre est rectangulaire, avec des bords horizontaux et verticaux).</span><span class="sxs-lookup"><span data-stu-id="94e59-114">(In OpenGL, the window is rectangular, with horizontal and vertical edges).</span></span> <span data-ttu-id="94e59-115">Lorsque vous faites référence à un modèle de polygone, implique que le modèle est fixe par rapport à l’origine de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="94e59-115">When referring to a polygon pattern, implies that the pattern is fixed relative to the window origin.</span></span>

</dd> <dt>

<span data-ttu-id="94e59-116"><span id="opengl_window_coordinates"></span><span id="OPENGL_WINDOW_COORDINATES"></span>**coordonnées de la fenêtre**</span><span class="sxs-lookup"><span data-stu-id="94e59-116"><span id="opengl_window_coordinates"></span><span id="OPENGL_WINDOW_COORDINATES"></span>**window coordinates**</span></span>
</dt> <dd>

<span data-ttu-id="94e59-117">Système de coordonnées d’une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="94e59-117">The coordinate system of a window.</span></span> <span data-ttu-id="94e59-118">Il est important de faire la distinction entre les noms des pixels, qui sont discrets et le système de coordonnées de la fenêtre, qui est continu.</span><span class="sxs-lookup"><span data-stu-id="94e59-118">It's important to distinguish between the names of pixels, which are discrete, and the window-coordinate system, which is continuous.</span></span> <span data-ttu-id="94e59-119">Par exemple, le pixel situé dans le coin inférieur gauche d’une fenêtre est pixel (0,0); les coordonnées de la fenêtre du centre de ce pixel sont (0,5, 0,5, z).</span><span class="sxs-lookup"><span data-stu-id="94e59-119">For example, the pixel at the lower-left corner of a window is pixel (0, 0); the window coordinates of the center of this pixel are (0.5, 0.5, z).</span></span> <span data-ttu-id="94e59-120">Notez que les coordonnées des fenêtres incluent une profondeur, ou z, un composant et que ce composant est également continu.</span><span class="sxs-lookup"><span data-stu-id="94e59-120">Note that window coordinates include a depth, or z, component, and that this component is continuous as well.</span></span>

</dd> <dt>

<span data-ttu-id="94e59-121"><span id="opengl_wireframe"></span><span id="OPENGL_WIREFRAME"></span>**Wireframe**</span><span class="sxs-lookup"><span data-stu-id="94e59-121"><span id="opengl_wireframe"></span><span id="OPENGL_WIREFRAME"></span>**wireframe**</span></span>
</dt> <dd>

<span data-ttu-id="94e59-122">Représentation d’un objet qui contient uniquement des segments de ligne.</span><span class="sxs-lookup"><span data-stu-id="94e59-122">A representation of an object that contains line segments only.</span></span> <span data-ttu-id="94e59-123">En règle générale, les segments de ligne indiquent les bords de polygone.</span><span class="sxs-lookup"><span data-stu-id="94e59-123">Typically, the line segments indicate polygon edges.</span></span>

</dd> </dl>

 

 




