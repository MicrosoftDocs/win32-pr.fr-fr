---
title: Portage des arcs et des cercles
description: Avec OpenGL, les arcs remplis et les cercles sont dessinés avec les mêmes appels que des arcs et des cercles sans remplissage. Le tableau suivant répertorie les fonctions arc et Circle de l’IRIS GL et leurs fonctions OpenGL équivalentes (GLU).
ms.assetid: b3458192-9cb6-4376-8136-45467584d3d4
keywords:
- Portage du grand livre de l’IRIS, arcs
- Portage à partir de IRIS GL, arcs
- portage vers OpenGL à partir de IRIS GL, arcs
- Portage OpenGL à partir de IRIS GL, arcs
- fonctions de dessin, arcs
- Portage de l’IRIS dans le GL, cercles
- Portage à partir de IRIS GL, cercles
- portage vers OpenGL à partir de IRIS GL, cercles
- Portage OpenGL à partir de IRIS GL, cercles
- fonctions de dessin, cercles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce17546ce17f24adf80641549d8843a473c8754
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380367"
---
# <a name="porting-arcs-and-circles"></a><span data-ttu-id="60cb4-114">Portage des arcs et des cercles</span><span class="sxs-lookup"><span data-stu-id="60cb4-114">Porting Arcs and Circles</span></span>

<span data-ttu-id="60cb4-115">Avec OpenGL, les arcs remplis et les cercles sont dessinés avec les mêmes appels que des arcs et des cercles sans remplissage.</span><span class="sxs-lookup"><span data-stu-id="60cb4-115">With OpenGL, filled arcs and circles are drawn with the same calls as unfilled arcs and circles.</span></span> <span data-ttu-id="60cb4-116">Le tableau suivant répertorie les fonctions arc et Circle de l’IRIS GL et leurs fonctions OpenGL équivalentes (GLU).</span><span class="sxs-lookup"><span data-stu-id="60cb4-116">The following table lists the IRIS GL arc and circle functions and their equivalent OpenGL (GLU) functions.</span></span>



| <span data-ttu-id="60cb4-117">Fonction IRIS GL</span><span class="sxs-lookup"><span data-stu-id="60cb4-117">IRIS GL function</span></span> | <span data-ttu-id="60cb4-118">Fonction OpenGL</span><span class="sxs-lookup"><span data-stu-id="60cb4-118">OpenGL function</span></span>                          | <span data-ttu-id="60cb4-119">Signification</span><span class="sxs-lookup"><span data-stu-id="60cb4-119">Meaning</span></span>                 |
|------------------|------------------------------------------|-------------------------|
| <span data-ttu-id="60cb4-120">**arcarcf**</span><span class="sxs-lookup"><span data-stu-id="60cb4-120">**arcarcf**</span></span>      | [<span data-ttu-id="60cb4-121">**gluPartialDisk**</span><span class="sxs-lookup"><span data-stu-id="60cb4-121">**gluPartialDisk**</span></span>](glupartialdisk.md) | <span data-ttu-id="60cb4-122">Dessine un arc.</span><span class="sxs-lookup"><span data-stu-id="60cb4-122">Draws an arc.</span></span>           |
| <span data-ttu-id="60cb4-123">**circcircf**</span><span class="sxs-lookup"><span data-stu-id="60cb4-123">**circcircf**</span></span>    | [<span data-ttu-id="60cb4-124">**gluDisk**</span><span class="sxs-lookup"><span data-stu-id="60cb4-124">**gluDisk**</span></span>](gludisk.md)               | <span data-ttu-id="60cb4-125">Dessine un cercle ou un disque.</span><span class="sxs-lookup"><span data-stu-id="60cb4-125">Draws a circle or disk.</span></span> |



 

<span data-ttu-id="60cb4-126">Vous pouvez effectuer quelques opérations avec des arcs et cercles OpenGL que vous ne pouvez pas faire avec IRIS GL.</span><span class="sxs-lookup"><span data-stu-id="60cb4-126">You can do some things with OpenGL arcs and circles that you can't do with IRIS GL.</span></span> <span data-ttu-id="60cb4-127">OpenGL appelle les courbes et les cercles, les disques et les disques partiels, respectivement.</span><span class="sxs-lookup"><span data-stu-id="60cb4-127">OpenGL calls arcs and circles, disks and partial disks respectively.</span></span>

<span data-ttu-id="60cb4-128">Lorsque vous portez des arcs et des cercles, gardez à l’esprit les points suivants sur OpenGL :</span><span class="sxs-lookup"><span data-stu-id="60cb4-128">When porting arcs and circles, keep the following points about OpenGL in mind:</span></span>

-   <span data-ttu-id="60cb4-129">Les angles sont mesurés en degrés, et non en dixièmes de degrés.</span><span class="sxs-lookup"><span data-stu-id="60cb4-129">Angles are measured in degrees, and not in tenths of degrees.</span></span>
-   <span data-ttu-id="60cb4-130">L’angle de début est mesuré à partir de l’axe y positif, et non à partir de l’axe x.</span><span class="sxs-lookup"><span data-stu-id="60cb4-130">The start angle is measured from the positive y-axis, and not from the x-axis.</span></span>
-   <span data-ttu-id="60cb4-131">L’angle de balayage est désormais dans le sens inverse des aiguilles d’une montre.</span><span class="sxs-lookup"><span data-stu-id="60cb4-131">The sweep angle is now clockwise instead of counterclockwise.</span></span>

<span data-ttu-id="60cb4-132">??</span><span class="sxs-lookup"><span data-stu-id="60cb4-132">??</span></span>

 

 




