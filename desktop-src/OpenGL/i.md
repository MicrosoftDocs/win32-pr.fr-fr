---
title: I (OpenGL)
description: Définitions des termes OpenGL qui commencent par la lettre I.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 2c78efce-9aed-4bcd-a254-7bff053b0acd
keywords:
- images
- primitives d’image
- mode immédiat
- index
- IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fe340cfbd7dbef3d93cc68ba310d863717225c0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104508233"
---
# <a name="i-opengl"></a><span data-ttu-id="fb886-108">I (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="fb886-108">I (OpenGL)</span></span>

<span data-ttu-id="fb886-109">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [e](e.md) [F](f.md) [G](g.md) [H](h.md) I [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="fb886-109">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) I [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="fb886-110"><span id="opengl_image"></span><span id="OPENGL_IMAGE"></span>**image**</span><span class="sxs-lookup"><span data-stu-id="fb886-110"><span id="opengl_image"></span><span id="OPENGL_IMAGE"></span>**image**</span></span>
</dt> <dd>

<span data-ttu-id="fb886-111">Tableau rectangulaire de pixels, dans la mémoire du client ou dans le trame.</span><span class="sxs-lookup"><span data-stu-id="fb886-111">A rectangular array of pixels, either in client memory or in the framebuffer.</span></span>

</dd> <dt>

<span data-ttu-id="fb886-112"><span id="opengl_image_primitive"></span><span id="OPENGL_IMAGE_PRIMITIVE"></span>**primitive d’image**</span><span class="sxs-lookup"><span data-stu-id="fb886-112"><span id="opengl_image_primitive"></span><span id="OPENGL_IMAGE_PRIMITIVE"></span>**image primitive**</span></span> 
</dt> <dd>

<span data-ttu-id="fb886-113">Bitmap ou image.</span><span class="sxs-lookup"><span data-stu-id="fb886-113">A bitmap or an image.</span></span>

</dd> <dt>

<span data-ttu-id="fb886-114"><span id="opengl_immediate_mode"></span><span id="OPENGL_IMMEDIATE_MODE"></span>**mode immédiat**</span><span class="sxs-lookup"><span data-stu-id="fb886-114"><span id="opengl_immediate_mode"></span><span id="OPENGL_IMMEDIATE_MODE"></span>**immediate mode**</span></span>
</dt> <dd>

<span data-ttu-id="fb886-115">Mode dans lequel une commande OpenGL est appelée directement, plutôt qu’à partir d’une liste d’affichage.</span><span class="sxs-lookup"><span data-stu-id="fb886-115">Mode in which an OpenGL command is called directly, rather than from a display list.</span></span> <span data-ttu-id="fb886-116">Aucun bit en mode immédiat n’existe ; le mode en mode immédiat fait référence à l’utilisation de OpenGL, plutôt qu’à un bit spécifique de l’État OpenGL.</span><span class="sxs-lookup"><span data-stu-id="fb886-116">No immediate-mode bit exists; the mode in immediate mode refers to usage of OpenGL, rather than to a specific bit of OpenGL state.</span></span>

</dd> <dt>

<span data-ttu-id="fb886-117"><span id="opengl_index"></span><span id="OPENGL_INDEX"></span>**évaluer**</span><span class="sxs-lookup"><span data-stu-id="fb886-117"><span id="opengl_index"></span><span id="OPENGL_INDEX"></span>**index**</span></span>
</dt> <dd>

<span data-ttu-id="fb886-118">Valeur unique qui est interprétée comme une valeur absolue, plutôt que comme une valeur normalisée dans une plage spécifiée (comme un composant).</span><span class="sxs-lookup"><span data-stu-id="fb886-118">A single value that is interpreted as an absolute value, rather than as a normalized value in a specified range (as is a component).</span></span> <span data-ttu-id="fb886-119">Les index de couleurs sont les noms des couleurs, qui sont déréférencées par le matériel d’affichage à l’aide de la carte des couleurs.</span><span class="sxs-lookup"><span data-stu-id="fb886-119">Color indexes are the names of colors, which are dereferenced by the display hardware using the color map.</span></span> <span data-ttu-id="fb886-120">Les index sont généralement masqués, plutôt que ancrés, lorsqu’ils sont hors limites.</span><span class="sxs-lookup"><span data-stu-id="fb886-120">Indexes are typically masked, rather than clamped, when out of range.</span></span> <span data-ttu-id="fb886-121">Par exemple, l’index 0xf7 est masqué en 0x7 lorsqu’il est écrit dans une mémoire tampon de 4 bits (couleur ou gabarit).</span><span class="sxs-lookup"><span data-stu-id="fb886-121">For example, the index 0xf7 is masked to 0x7 when written to a 4-bit buffer (color or stencil).</span></span> <span data-ttu-id="fb886-122">Les index de couleurs et les index de stencil sont toujours traités comme des index, jamais comme des composants.</span><span class="sxs-lookup"><span data-stu-id="fb886-122">Color indexes and stencil indexes are always treated as indexes, never as components.</span></span>

</dd> <dt>

<span data-ttu-id="fb886-123"><span id="opengl_iris_gl"></span><span id="OPENGL_IRIS_GL"></span>**IRIS GL**</span><span class="sxs-lookup"><span data-stu-id="fb886-123"><span id="opengl_iris_gl"></span><span id="OPENGL_IRIS_GL"></span>**IRIS GL**</span></span>
</dt> <dd>

<span data-ttu-id="fb886-124">La bibliothèque graphique propriétaire de Silicon Graphics, développée de 1982 à 1992.</span><span class="sxs-lookup"><span data-stu-id="fb886-124">Silicon Graphics' proprietary graphics library, developed from 1982 through 1992.</span></span> <span data-ttu-id="fb886-125">OpenGL a été conçu avec IRIS GL comme point de départ.</span><span class="sxs-lookup"><span data-stu-id="fb886-125">OpenGL was designed with IRIS GL as a starting point.</span></span>

</dd> </dl>

 

 




