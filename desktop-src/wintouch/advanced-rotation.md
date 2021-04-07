---
title: Rotation avancée
description: Cette section explique comment faire pivoter un objet en fonction de l’endroit où l’utilisateur effectue la manipulation de rotation.
ms.assetid: 56b339b1-a062-4c0e-91c8-aec08a17bc65
keywords:
- Tactile Windows, rotation
- Tactile Windows, rotation avancée
- Tactile Windows, manipulations
- manipulations, rotation
- manipulations, rotation avancée
- rotation, avancé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc3a84679f4189d28941262cda2585887b0932c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939681"
---
# <a name="advanced-rotation"></a><span data-ttu-id="17563-109">Rotation avancée</span><span class="sxs-lookup"><span data-stu-id="17563-109">Advanced Rotation</span></span>

<span data-ttu-id="17563-110">Cette section explique comment faire pivoter un objet en fonction de l’endroit où l’utilisateur effectue la manipulation de rotation.</span><span class="sxs-lookup"><span data-stu-id="17563-110">This section explains how to rotate an object based on where the user is performing the rotation manipulation.</span></span>

<span data-ttu-id="17563-111">L’illustration suivante montre deux façons différentes de faire pivoter un objet.</span><span class="sxs-lookup"><span data-stu-id="17563-111">The following image illustrates two different ways that an object can be rotated.</span></span>

![Illustration montrant deux types de rotation à un seul doigt : autour du centre ou autour du bord, avec la périphérie qui implique à la fois la rotation et la translation](images/rotation.png)

<span data-ttu-id="17563-113">Dans l’exemple A, l’objet est manipulé autour du point central de l’objet.</span><span class="sxs-lookup"><span data-stu-id="17563-113">In example A, the object is manipulated around the center point of the object.</span></span> <span data-ttu-id="17563-114">Dans l’exemple B, l’objet pivote autour du point central de la manipulation.</span><span class="sxs-lookup"><span data-stu-id="17563-114">In example B, the object is rotated around the center point of the manipulation.</span></span> <span data-ttu-id="17563-115">Pour prendre en charge la manipulation autour d’un point autre que le point central de l’objet, vous devez effectuer une manipulation composée qui effectue à la fois la rotation et la translation.</span><span class="sxs-lookup"><span data-stu-id="17563-115">To support manipulation around a point other than the center point of the object, you must perform a compound manipulation that performs both rotation and translation.</span></span> <span data-ttu-id="17563-116">Le code suivant montre comment cette manipulation est effectuée et calculée.</span><span class="sxs-lookup"><span data-stu-id="17563-116">The following code shows how this manipulation is performed and calculated.</span></span>


```C++
RotateVector(FLOAT *vector, FLOAT *tVector, FLOAT fAngle) {
    FLOAT fAngleRads = fAngle / 180.0f * 3.14159f;
    FLOAT fSin = sin(fAngleRads);
    FLOAT fCos = cos(fAngleRads);

    FLOAT fNewX = (vector[0]*fCos) - (vector[1]*fSin);
    FLOAT fNewY = (vector[0]*fSin) + (vector[1]*fCos);

    tVector[0] = fNewX;
    tVector[1] = fNewY;
}
     
```



## <a name="related-topics"></a><span data-ttu-id="17563-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="17563-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17563-118">Manipulations avancées</span><span class="sxs-lookup"><span data-stu-id="17563-118">Advanced Manipulations</span></span>](advanced-manipulations.md)
</dt> <dt>

[<span data-ttu-id="17563-119">Manipulations</span><span class="sxs-lookup"><span data-stu-id="17563-119">Manipulations</span></span>](getting-started-with-manipulations.md)
</dt> </dl>

 

 




