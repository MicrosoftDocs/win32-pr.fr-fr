---
title: A (OpenGL)
description: Définitions des termes OpenGL qui commencent par la lettre A.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: e583610f-37da-47bb-bbd6-41d353b88244
keywords:
- alias
- alpha
- animation
- anticrénelage
- découpage spécifique à l’application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d161832eb6d81738038e10564233f26920f0d60
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383703"
---
# <a name="a-opengl"></a><span data-ttu-id="e7ab8-108">A (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="e7ab8-108">A (OpenGL)</span></span>

<span data-ttu-id="e7ab8-109">A [B](b.md) [C](c.md) [D](d.md) [e](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="e7ab8-109">A [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="e7ab8-110"><span id="opengl_aliasing"></span><span id="OPENGL_ALIASING"></span>**alias**</span><span class="sxs-lookup"><span data-stu-id="e7ab8-110"><span id="opengl_aliasing"></span><span id="OPENGL_ALIASING"></span>**aliasing**</span></span>
</dt> <dd>

<span data-ttu-id="e7ab8-111">Technique de rendu qui attribue aux pixels la couleur de la primitive rendue, que cette primitive couvre tout ou partie de la zone du pixel.</span><span class="sxs-lookup"><span data-stu-id="e7ab8-111">A rendering technique that assigns to pixels the color of the primitive being rendered, whether that primitive covers all or part of the pixel's area.</span></span> <span data-ttu-id="e7ab8-112">L’alias génère des bords dentelés ou des escalier.</span><span class="sxs-lookup"><span data-stu-id="e7ab8-112">Aliasing results in jagged edges, or jaggies.</span></span> <span data-ttu-id="e7ab8-113">Voir aussi en [escalier](jk.md).</span><span class="sxs-lookup"><span data-stu-id="e7ab8-113">See also [jaggies](jk.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7ab8-114"><span id="opengl_alpha"></span><span id="OPENGL_ALPHA"></span>**lettres**</span><span class="sxs-lookup"><span data-stu-id="e7ab8-114"><span id="opengl_alpha"></span><span id="OPENGL_ALPHA"></span>**alpha**</span></span>
</dt> <dd>

<span data-ttu-id="e7ab8-115">Quatrième composant de couleur généralement utilisé pour contrôler la fusion des couleurs.</span><span class="sxs-lookup"><span data-stu-id="e7ab8-115">A fourth color component typically used to control color blending.</span></span> <span data-ttu-id="e7ab8-116">Le composant alpha n’est jamais affiché directement.</span><span class="sxs-lookup"><span data-stu-id="e7ab8-116">The alpha component is never displayed directly.</span></span> <span data-ttu-id="e7ab8-117">Par Convention, OpenGL alpha indique l’opacité et la transparence sur une échelle de 0,0 à 1,0.</span><span class="sxs-lookup"><span data-stu-id="e7ab8-117">By convention, OpenGL alpha indicates opacity and transparency on a scale of 0.0 to 1.0.</span></span> <span data-ttu-id="e7ab8-118">Une valeur alpha de 1,0 implique une opacité complète, une valeur alpha de 0,0 implique une transparence complète.</span><span class="sxs-lookup"><span data-stu-id="e7ab8-118">An alpha value of 1.0 implies complete opacity, an alpha value of 0.0 implies complete transparency.</span></span>

</dd> <dt>

<span data-ttu-id="e7ab8-119"><span id="opengl_animation"></span><span id="OPENGL_ANIMATION"></span>**Animation**</span><span class="sxs-lookup"><span data-stu-id="e7ab8-119"><span id="opengl_animation"></span><span id="OPENGL_ANIMATION"></span>**animation**</span></span>
</dt> <dd>

<span data-ttu-id="e7ab8-120">Génération d’un rendu répété d’une scène suffisamment rapidement, avec des positions de point de vue et d’objet en constante évolution, que l’illusion de mouvement est obtenue.</span><span class="sxs-lookup"><span data-stu-id="e7ab8-120">The generation of repeated renderings of a scene quickly enough, with smoothly changing viewpoint or object positions, that the illusion of motion is achieved.</span></span> <span data-ttu-id="e7ab8-121">L’animation OpenGL utilise presque toujours la double mise en mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="e7ab8-121">OpenGL animation almost always uses double-buffering.</span></span>

</dd> <dt>

<span data-ttu-id="e7ab8-122"><span id="opengl_antialiasing"></span><span id="OPENGL_ANTIALIASING"></span>**anticrénelage**</span><span class="sxs-lookup"><span data-stu-id="e7ab8-122"><span id="opengl_antialiasing"></span><span id="OPENGL_ANTIALIASING"></span>**antialiasing**</span></span>
</dt> <dd>

<span data-ttu-id="e7ab8-123">Technique de rendu qui assigne des couleurs aux pixels en fonction de la fraction de la zone de pixels couverte par la primitive rendue.</span><span class="sxs-lookup"><span data-stu-id="e7ab8-123">A rendering technique that assigns colors to pixels based on the fraction of the pixel area that is covered by the primitive being rendered.</span></span> <span data-ttu-id="e7ab8-124">Le rendu avec anticrénelage réduit ou élimine les escalier qui résultent d’un rendu avec alias.</span><span class="sxs-lookup"><span data-stu-id="e7ab8-124">Antialiased rendering reduces or eliminates the jaggies that result from aliased rendering.</span></span> <span data-ttu-id="e7ab8-125">Voir aussi [irrégularités](jk.md), [rendu](r.md).</span><span class="sxs-lookup"><span data-stu-id="e7ab8-125">See also [jaggies](jk.md), [rendering](r.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7ab8-126"><span id="opengl_application_specific_clipping"></span><span id="OPENGL_APPLICATION_SPECIFIC_CLIPPING"></span>**découpage spécifique à l’application**</span><span class="sxs-lookup"><span data-stu-id="e7ab8-126"><span id="opengl_application_specific_clipping"></span><span id="OPENGL_APPLICATION_SPECIFIC_CLIPPING"></span>**application-specific clipping**</span></span> 
</dt> <dd>

<span data-ttu-id="e7ab8-127">Découpage des primitives par rapport aux plans en coordonnées oculaires.</span><span class="sxs-lookup"><span data-stu-id="e7ab8-127">Clipping of primitives against planes in eye coordinates.</span></span> <span data-ttu-id="e7ab8-128">Les plans sont spécifiés par l’application à l’aide de [**glClipPlane**](glclipplane.md).</span><span class="sxs-lookup"><span data-stu-id="e7ab8-128">The planes are specified by the application using [**glClipPlane**](glclipplane.md).</span></span> <span data-ttu-id="e7ab8-129">Voir aussi [coordonnées oculaires](e.md).</span><span class="sxs-lookup"><span data-stu-id="e7ab8-129">See also [eye coordinates](e.md).</span></span>

</dd> </dl>

 

 




