---
title: Portage des fonctions v
description: Dans IRIS GL, vous utilisez des variations sur la fonction v pour spécifier des vertex. La fonction OpenGL équivalente est glVertex ci-dessous sont des exemples de glVertex.
ms.assetid: b4ac0c41-983a-4387-a69f-530c9094dc33
keywords:
- Portage de l’IRIS dans le GL, sommets
- Portage à partir de IRIS GL, vertex
- portage vers OpenGL à partir de IRIS GL, vertex
- Portage OpenGL à partir de IRIS GL, vertex
- fonctions de dessin, sommets
- vertex, Portage à partir de IRIS GL
- Portage de l’IRIS dans le GL, fonctions v
- Portage à partir de l’IRIS GL, fonctions v
- portage vers OpenGL à partir de l’IRIS GL, fonctions v
- Portage OpenGL depuis IRIS GL, fonctions v
- fonctions de dessin, fonctions v
- fonctions v
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfd5e40915f891817606ac8517c0b3b980b436be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309750"
---
# <a name="porting-v-functions"></a><span data-ttu-id="9c54e-116">Portage des fonctions v</span><span class="sxs-lookup"><span data-stu-id="9c54e-116">Porting v Functions</span></span>

<span data-ttu-id="9c54e-117">Dans IRIS GL, vous utilisez des variations sur la fonction **v** pour spécifier des vertex.</span><span class="sxs-lookup"><span data-stu-id="9c54e-117">In IRIS GL, you use variations on the **v** function to specify vertices.</span></span> <span data-ttu-id="9c54e-118">La fonction OpenGL équivalente est [glVertex](glvertex-functions.md): vous trouverez ci-dessous des exemples de **glVertex**.</span><span class="sxs-lookup"><span data-stu-id="9c54e-118">The equivalent OpenGL function is [glVertex](glvertex-functions.md): Below are examples of **glVertex**.</span></span>

``` syntax
glVertex2[d|f|i|s][v]( x, y ); 
glVertex3[d|f|i|s][v]( x, y, z); 
glVertex4[d|f|i|s][v]( x, y, z, w);
```

<span data-ttu-id="9c54e-119">La fonction **glVertex** prend des suffixes de la même façon que les autres appels OpenGL.</span><span class="sxs-lookup"><span data-stu-id="9c54e-119">The **glVertex** function takes suffixes the same way other OpenGL calls do.</span></span> <span data-ttu-id="9c54e-120">Les versions vectorielles de l’appel prennent des tableaux de la taille appropriée comme arguments.</span><span class="sxs-lookup"><span data-stu-id="9c54e-120">The vector versions of the call take arrays of the proper size as arguments.</span></span> <span data-ttu-id="9c54e-121">Dans la version 2D, z = 0 et w = 1.</span><span class="sxs-lookup"><span data-stu-id="9c54e-121">In the 2-D version, z=0 and w=1.</span></span> <span data-ttu-id="9c54e-122">Dans la version 3D, w = 1.</span><span class="sxs-lookup"><span data-stu-id="9c54e-122">In the 3-D version, w=1.</span></span>

 

 




