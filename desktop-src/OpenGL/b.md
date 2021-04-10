---
title: B (OpenGL)
description: Définitions des termes OpenGL qui commencent par la lettre B.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 053fa15a-fbda-43a7-a740-b4477ad9c946
keywords:
- face arrière
- bits
- bitmaps
- bitplanes
- mélanger
- mémoires tampons
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5081fa4d1742f2c8dad0a6ef7ef3368135bf0d23
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103941602"
---
# <a name="b-opengl"></a><span data-ttu-id="ef678-109">B (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="ef678-109">B (OpenGL)</span></span>

<span data-ttu-id="ef678-110">[A](a.md) B [C](c.md) [D](d.md) [e](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="ef678-110">[A](a.md) B [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="ef678-111"><span id="opengl_back_face"></span><span id="OPENGL_BACK_FACE"></span>**face arrière**</span><span class="sxs-lookup"><span data-stu-id="ef678-111"><span id="opengl_back_face"></span><span id="OPENGL_BACK_FACE"></span>**back face**</span></span>
</dt> <dd>

<span data-ttu-id="ef678-112">Consultez la section [face](f.md).</span><span class="sxs-lookup"><span data-stu-id="ef678-112">See [face](f.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef678-113"><span id="opengl_bit"></span><span id="OPENGL_BIT"></span>**64bits**</span><span class="sxs-lookup"><span data-stu-id="ef678-113"><span id="opengl_bit"></span><span id="OPENGL_BIT"></span>**bit**</span></span>
</dt> <dd>

<span data-ttu-id="ef678-114">Chiffre binaire.</span><span class="sxs-lookup"><span data-stu-id="ef678-114">Binary digit.</span></span> <span data-ttu-id="ef678-115">Une variable d’État qui n’a que deux valeurs possibles : 0 ou 1.</span><span class="sxs-lookup"><span data-stu-id="ef678-115">A state variable that has only two possible values: 0 or 1.</span></span> <span data-ttu-id="ef678-116">Les nombres binaires sont des constructions d’un ou plusieurs bits.</span><span class="sxs-lookup"><span data-stu-id="ef678-116">Binary numbers are constructions of one or more bits.</span></span>

</dd> <dt>

<span data-ttu-id="ef678-117"><span id="opengl_bitmap"></span><span id="OPENGL_BITMAP"></span>**pixels**</span><span class="sxs-lookup"><span data-stu-id="ef678-117"><span id="opengl_bitmap"></span><span id="OPENGL_BITMAP"></span>**bitmap**</span></span>
</dt> <dd>

<span data-ttu-id="ef678-118">Tableau rectangulaire de bits.</span><span class="sxs-lookup"><span data-stu-id="ef678-118">A rectangular array of bits.</span></span> <span data-ttu-id="ef678-119">En outre, la primitive rendue par la commande [**glBitmap**](glbitmap.md) , qui utilise son paramètre bitmap comme masque.</span><span class="sxs-lookup"><span data-stu-id="ef678-119">Also, the primitive rendered by the [**glBitmap**](glbitmap.md) command, which uses its bitmap parameter as a mask.</span></span>

</dd> <dt>

<span data-ttu-id="ef678-120"><span id="opengl_bitplane"></span><span id="OPENGL_BITPLANE"></span>**bitplane**</span><span class="sxs-lookup"><span data-stu-id="ef678-120"><span id="opengl_bitplane"></span><span id="OPENGL_BITPLANE"></span>**bitplane**</span></span>
</dt> <dd>

<span data-ttu-id="ef678-121">Tableau rectangulaire de bits mappé un-à-un avec pixels.</span><span class="sxs-lookup"><span data-stu-id="ef678-121">A rectangular array of bits mapped one-to-one with pixels.</span></span>

</dd> <dt>

<span data-ttu-id="ef678-122"><span id="opengl_blending"></span><span id="OPENGL_BLENDING"></span>**fusion**</span><span class="sxs-lookup"><span data-stu-id="ef678-122"><span id="opengl_blending"></span><span id="OPENGL_BLENDING"></span>**blending**</span></span>
</dt> <dd>

<span data-ttu-id="ef678-123">Réduction de deux composants de couleur à un composant, généralement sous la forme d’une interpolation linéaire entre les deux composants.</span><span class="sxs-lookup"><span data-stu-id="ef678-123">Reducing two color components to one component, usually as a linear interpolation between the two components.</span></span>

</dd> <dt>

<span data-ttu-id="ef678-124"><span id="opengl_buffer"></span><span id="OPENGL_BUFFER"></span>**mémoire tampon**</span><span class="sxs-lookup"><span data-stu-id="ef678-124"><span id="opengl_buffer"></span><span id="OPENGL_BUFFER"></span>**buffer**</span></span>
</dt> <dd>

<span data-ttu-id="ef678-125">Groupe de bitplanes qui stocke un seul composant (par exemple, profondeur ou vert) ou un index unique (tel que l’index de couleur ou l’index de stencil).</span><span class="sxs-lookup"><span data-stu-id="ef678-125">A group of bitplanes that stores a single component (such as depth or green) or a single index (such as the color index or the stencil index).</span></span> <span data-ttu-id="ef678-126">Parfois, les mémoires tampons rouge, vert, bleu et alpha sont désignées collectivement comme mémoire tampon de couleur (et non en tant que tampons de couleur).</span><span class="sxs-lookup"><span data-stu-id="ef678-126">Sometimes the red, green, blue, and alpha buffers are referred to collectively as the color buffer (rather than as the color buffers).</span></span>

</dd> </dl>

 

 




