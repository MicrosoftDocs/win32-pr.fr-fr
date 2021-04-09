---
description: Pour améliorer les performances de rendu, vous pouvez supprimer (ou supprimer) une primitive qui s’éloigne de l’appareil photo.
ms.assetid: b4b8ff3f-aa20-4422-8f6f-34cae25de0e6
title: État d’élimination (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad86e71fd7c6543f0d232e32a630d73e0ebbadae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111010"
---
# <a name="culling-state-direct3d-9"></a><span data-ttu-id="63fdd-103">État d’élimination (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="63fdd-103">Culling State (Direct3D 9)</span></span>

<span data-ttu-id="63fdd-104">Pour améliorer les performances de rendu, vous pouvez supprimer (ou supprimer) une primitive qui s’éloigne de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="63fdd-104">To improve rendering performance, you can cull out (or remove) a primitive that faces away from the camera.</span></span> <span data-ttu-id="63fdd-105">Pour les primitives à un seul côté, Cela économise l’heure de rendu, car une face arrière n’est pas visible.</span><span class="sxs-lookup"><span data-stu-id="63fdd-105">For single-sided primitives, this saves rendering time because a back-face is not visible.</span></span> <span data-ttu-id="63fdd-106">Pour activer l’élimination, vous devez connaître l’ordre d’enroulement des vertex (généralement dans le sens inverse des aiguilles d’une montre).</span><span class="sxs-lookup"><span data-stu-id="63fdd-106">To enable culling, you need to know the winding order of the vertices (typically counter-clockwise).</span></span> <span data-ttu-id="63fdd-107">Cet exemple supprime toutes les primitives dont la face arrière est dirigée vers l’avant (selon un sens dans le sens inverse des aiguilles d’une montre) :</span><span class="sxs-lookup"><span data-stu-id="63fdd-107">This example will remove any primitive whose back face is facing forward (given a counter-clockwise winding order):</span></span>


```
SetRenderState(D3DRS_CULLMODE, D3DCULL_CCW);
```



## <a name="related-topics"></a><span data-ttu-id="63fdd-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="63fdd-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63fdd-109">États de rendu</span><span class="sxs-lookup"><span data-stu-id="63fdd-109">Render States</span></span>](render-states.md)
</dt> </dl>

 

 



