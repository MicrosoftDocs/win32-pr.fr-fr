---
title: D (OpenGL)
description: Définitions des termes OpenGL qui commencent par la lettre D.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: f97470e7-a500-47d7-84f0-b3045d04b8fc
keywords:
- depth
- profondeur cueing
- afficher les listes
- tramage
- doubles tampons
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97cb068f06135c6ba29e8a61f472d98907090a78
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739500"
---
# <a name="d-opengl"></a><span data-ttu-id="8b9a0-108">D (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="8b9a0-108">D (OpenGL)</span></span>

<span data-ttu-id="8b9a0-109">[A](a.md) [B](b.md) [C](c.md) D [e](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="8b9a0-109">[A](a.md) [B](b.md) [C](c.md) D [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="8b9a0-110"><span id="opengl_depth"></span><span id="OPENGL_DEPTH"></span>**profondeur**</span><span class="sxs-lookup"><span data-stu-id="8b9a0-110"><span id="opengl_depth"></span><span id="OPENGL_DEPTH"></span>**depth**</span></span>
</dt> <dd>

<span data-ttu-id="8b9a0-111">Fait généralement référence à la coordonnée de la fenêtre z.</span><span class="sxs-lookup"><span data-stu-id="8b9a0-111">Generally refers to the z window coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="8b9a0-112"><span id="opengl_depth_cueing"></span><span id="OPENGL_DEPTH_CUEING"></span>**profondeur cueing**</span><span class="sxs-lookup"><span data-stu-id="8b9a0-112"><span id="opengl_depth_cueing"></span><span id="OPENGL_DEPTH_CUEING"></span>**depth cueing**</span></span>
</dt> <dd>

<span data-ttu-id="8b9a0-113">Technique de rendu qui assigne une couleur en fonction de la distance par rapport au point de vue.</span><span class="sxs-lookup"><span data-stu-id="8b9a0-113">A rendering technique that assigns color based on distance from the viewpoint.</span></span>

</dd> <dt>

<span data-ttu-id="8b9a0-114"><span id="opengl_display_list"></span><span id="OPENGL_DISPLAY_LIST"></span>**afficher la liste**</span><span class="sxs-lookup"><span data-stu-id="8b9a0-114"><span id="opengl_display_list"></span><span id="OPENGL_DISPLAY_LIST"></span>**display list**</span></span>
</dt> <dd>

<span data-ttu-id="8b9a0-115">Liste nommée de commandes OpenGL.</span><span class="sxs-lookup"><span data-stu-id="8b9a0-115">A named list of OpenGL commands.</span></span> <span data-ttu-id="8b9a0-116">Les listes d’affichage étant toujours stockées sur le serveur, vous pouvez utiliser des listes d’affichage pour réduire le trafic réseau dans les environnements client/serveur.</span><span class="sxs-lookup"><span data-stu-id="8b9a0-116">Display lists are always stored on the server, so display lists can be used to reduce the network traffic in client/server environments.</span></span> <span data-ttu-id="8b9a0-117">Le contenu d’une liste d’affichage peut être prétraité et peut donc s’exécuter plus efficacement que le même jeu de commandes OpenGL exécuté en mode immédiat.</span><span class="sxs-lookup"><span data-stu-id="8b9a0-117">The contents of a display list may be preprocessed, and might therefore execute more efficiently than the same set of OpenGL commands executed in immediate mode.</span></span> <span data-ttu-id="8b9a0-118">Ce prétraitement est particulièrement important pour le calcul de commandes intensives telles que [**glTexImage**](glteximage1d.md).</span><span class="sxs-lookup"><span data-stu-id="8b9a0-118">Such preprocessing is especially important for computing intensive commands such as [**glTexImage**](glteximage1d.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b9a0-119"><span id="opengl_dithering"></span><span id="OPENGL_DITHERING"></span>**tramage**</span><span class="sxs-lookup"><span data-stu-id="8b9a0-119"><span id="opengl_dithering"></span><span id="OPENGL_DITHERING"></span>**dithering**</span></span>
</dt> <dd>

<span data-ttu-id="8b9a0-120">Technique pour l’amélioration de la plage de couleurs perçue dans une image au détriment de la résolution spatiale.</span><span class="sxs-lookup"><span data-stu-id="8b9a0-120">A technique for increasing the perceived range of colors in an image at the cost of spatial resolution.</span></span> <span data-ttu-id="8b9a0-121">Des valeurs de couleur différentes sont affectées aux pixels adjacents.</span><span class="sxs-lookup"><span data-stu-id="8b9a0-121">Adjacent pixels are assigned differing color values.</span></span> <span data-ttu-id="8b9a0-122">Lorsqu’ils sont affichés à distance, ces couleurs semblent fusionner en une seule couleur intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="8b9a0-122">When viewed from a distance, these colors seem to blend into a single intermediate color.</span></span> <span data-ttu-id="8b9a0-123">La technique est similaire au demi-virage utilisé dans les publications en noir et blanc pour obtenir des nuances de gris.</span><span class="sxs-lookup"><span data-stu-id="8b9a0-123">The technique is similar to the half-toning used in black-and-white publications to achieve shades of gray.</span></span>

</dd> <dt>

<span data-ttu-id="8b9a0-124"><span id="opengl_double_buffering"></span><span id="OPENGL_DOUBLE_BUFFERING"></span>**double mise en mémoire tampon**</span><span class="sxs-lookup"><span data-stu-id="8b9a0-124"><span id="opengl_double_buffering"></span><span id="OPENGL_DOUBLE_BUFFERING"></span>**double buffering**</span></span>
</dt> <dd>

<span data-ttu-id="8b9a0-125">À l’aide de contextes OpenGL dans lesquels les deux mémoires tampons de couleur d’arrière-plan et d’arrière-plan sont double mise en mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="8b9a0-125">Using OpenGL contexts in which both front and back color buffers are double-buffered.</span></span> <span data-ttu-id="8b9a0-126">L’animation lisse s’effectue en rendant uniquement la mémoire tampon d’arrière-plan (qui n’est pas affichée), puis en provoquant l’échange des mémoires tampons avant et arrière.</span><span class="sxs-lookup"><span data-stu-id="8b9a0-126">Smooth animation is accomplished by rendering into only the back buffer (which isn't displayed), then causing the front and back buffers to be swapped.</span></span>

</dd> </dl>

 

 




