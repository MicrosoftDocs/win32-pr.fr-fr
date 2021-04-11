---
title: Expansion avancée
description: Expansion avancée
ms.assetid: 29db15a1-fa56-441a-af99-9e858d143804
keywords:
- Tactile Windows, expansion
- Windows Touch, développement avancé
- Tactile Windows, manipulations
- manipulations, expansion
- manipulations, expansion avancée
- expansion, avancé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b81a3a395da053b7d0e8f79a115a2489f3e63190
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190821"
---
# <a name="advanced-expansion"></a><span data-ttu-id="85ecb-109">Expansion avancée</span><span class="sxs-lookup"><span data-stu-id="85ecb-109">Advanced Expansion</span></span>

<span data-ttu-id="85ecb-110">L’illustration suivante montre deux façons d’étendre un objet.</span><span class="sxs-lookup"><span data-stu-id="85ecb-110">The following illustration shows two ways that an object can be expanded.</span></span>

![Illustration montrant une expansion simple autour du point central d’un objet et une expansion avancée autour du point central de la manipulation](images/expansion.png)

<span data-ttu-id="85ecb-112">Dans l’exemple A, l’exemple d’expansion simple, l’objet est développé autour de son point central.</span><span class="sxs-lookup"><span data-stu-id="85ecb-112">In example A, the simple expansion example, the object is expanded around its center point.</span></span> <span data-ttu-id="85ecb-113">Dans l’exemple B, l’objet est développé autour du point central de la manipulation.</span><span class="sxs-lookup"><span data-stu-id="85ecb-113">In example B, the object is expanded around the center point of the manipulation.</span></span> <span data-ttu-id="85ecb-114">Pour ce faire, vous devez traduire l’objet pendant son développement.</span><span class="sxs-lookup"><span data-stu-id="85ecb-114">To enable this, you must translate the object while it is being expanded.</span></span> <span data-ttu-id="85ecb-115">La valeur de conversion de l’objet est identique à la distance entre le centre de l’objet et le point central du mouvement.</span><span class="sxs-lookup"><span data-stu-id="85ecb-115">The amount that you will translate the object is the same as the distance from the center of the object to the center point of the gesture.</span></span> <span data-ttu-id="85ecb-116">Intuitivement, c’est comme si vous développiez l’objet à partir du point central de votre mouvement d’expansion, puis que vous le déplaciez de manière à ce qu’il se trouve toujours au même centre que sa position initiale.</span><span class="sxs-lookup"><span data-stu-id="85ecb-116">Intuitively, it is as though you are expanding the object from the center point of your expansion gesture and then moving it so that it is still at the same center as its initial position.</span></span> <span data-ttu-id="85ecb-117">Le code suivant illustre une façon dont ce concept peut être appliqué pour permettre l’expansion autour d’un point central.</span><span class="sxs-lookup"><span data-stu-id="85ecb-117">The following code shows one way that this concept can be applied to enable expansion around a center point.</span></span>


```C++
    if(m_fFactor != 1.0f)
    {
        // We represent our vectors as an array.
        // x: vx[0], y: vx[1]

        FLOAT v1[2];
        v1[0] = this->get_CenterX() - fOffset[0];
        v1[1] = this->get_CenterY() - fOffset[1];

        FLOAT v2[2];
        v2[0] = v1[0] * m_fFactor;
        v2[1] = v1[1] * m_fFactor;
        
        m_fdX += v2[0] - v1[0];
        m_fdY += v2[1] - v1[1];
    }
   
```



## <a name="related-topics"></a><span data-ttu-id="85ecb-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="85ecb-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85ecb-119">Manipulations</span><span class="sxs-lookup"><span data-stu-id="85ecb-119">Manipulations</span></span>](getting-started-with-manipulations.md)
</dt> </dl>

 

 




