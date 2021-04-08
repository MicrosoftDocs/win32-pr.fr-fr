---
title: Traduction avancée
description: Traduction avancée
ms.assetid: 48a1bdd5-8b7b-4460-9b7b-1ab8969a28f8
keywords:
- Tactile Windows, traduction
- Tactile Windows, traduction avancée
- Tactile Windows, manipulations
- manipulations, traduction
- manipulations, traduction avancée
- translation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc383c71e1f1417d30b64db18aa627039602b942
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839386"
---
# <a name="advanced-translation"></a><span data-ttu-id="6f4e0-109">Traduction avancée</span><span class="sxs-lookup"><span data-stu-id="6f4e0-109">Advanced Translation</span></span>

<span data-ttu-id="6f4e0-110">L’illustration suivante montre deux interprétations de la traduction.</span><span class="sxs-lookup"><span data-stu-id="6f4e0-110">The following illustration shows two interpretations of translation.</span></span>

![Illustration montrant tout d’abord une traduction simple, dans laquelle un objet est déplacé sans rotation, puis affiche une traduction avancée, qui implique le déplacement avec la rotation](images/translation.png)

<span data-ttu-id="6f4e0-112">Dans l’exemple A, l’exemple de traduction simple, l’objet est déplacé sans rotation.</span><span class="sxs-lookup"><span data-stu-id="6f4e0-112">In example A, the simple translation example, the object is moved without rotation.</span></span> <span data-ttu-id="6f4e0-113">Dans l’exemple B, l’objet est pivoté pendant la traduction, en fonction de l’emplacement du point de contact de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6f4e0-113">In example B, the object is rotated during the translation, depending on where the object contact point is.</span></span> <span data-ttu-id="6f4e0-114">Si vous activez la rotation à un seul doigt comme décrit dans [rotation à un seul doigt](single-finger-rotation.md), vous pouvez activer la traduction complexe.</span><span class="sxs-lookup"><span data-stu-id="6f4e0-114">If you enable single-finger rotation as described in [Single-Finger Rotation](single-finger-rotation.md), you can enable complex translation.</span></span> <span data-ttu-id="6f4e0-115">Le diagramme suivant montre les différents composants de la rotation à un seul doigt lorsque vous effectuez une traduction.</span><span class="sxs-lookup"><span data-stu-id="6f4e0-115">The following diagram shows the various components of single-finger rotation when you are performing translation.</span></span>

![Illustration montrant les composants de rotation à un seul doigt : pivotpointx, pivotpointy et pivotradius](images/translation-complex-components.png)

<span data-ttu-id="6f4e0-117">Lorsque l’objet est déplacé, le rayon est recalculé et le point pivot est déplacé.</span><span class="sxs-lookup"><span data-stu-id="6f4e0-117">As the object is moved, the radius is recalculated and the pivot point is moved.</span></span>

<span data-ttu-id="6f4e0-118">Le code suivant illustre une méthode permettant d’effectuer cette opération dans une implémentation de [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta) qui permet une traduction complexe.</span><span class="sxs-lookup"><span data-stu-id="6f4e0-118">The following code shows one way that you can do this in an implementation of [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta) that enables complex translation.</span></span>


```C++
    //Apply transformation based on rotationDelta (in radians)
    FLOAT rads = 180.0f / 3.14159f;
    m_dObj->Rotate(rotationDelta*rads, x, y);

    // Apply translation based on scaleDelta
    m_dObj->Scale(scaleDelta);

    // Apply translation based on translationDelta
    m_dObj->Translate(translationDeltaX, translationDeltaY);

    // Set values for one finger rotations
    FLOAT fPivotRadius = (FLOAT)(m_dObj->get_Width() + m_dObj->get_Height())/8.0f;
    FLOAT fPivotPtX = m_dObj->get_CenterX();
    FLOAT fPivotPtY = m_dObj->get_CenterY();
        
    m_manip->put_PivotPointX(fPivotPtX);
    m_manip->put_PivotPointY(fPivotPtY);
    m_manip->put_PivotRadius(fPivotRadius);       
   
```



> [!Note]  
> <span data-ttu-id="6f4e0-119">Les transformations d’objet se produisent avant le calcul des points pivot et du rayon.</span><span class="sxs-lookup"><span data-stu-id="6f4e0-119">Object transformations occur before the pivot points and radius are calculated.</span></span> <span data-ttu-id="6f4e0-120">De cette façon, l’objet se déplace correctement si l’utilisateur effectue une expansion sur l’objet pendant son déplacement.</span><span class="sxs-lookup"><span data-stu-id="6f4e0-120">In this manner the object will move correctly if the user performs expansion on the object while it is moving.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6f4e0-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6f4e0-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f4e0-122">Manipulations</span><span class="sxs-lookup"><span data-stu-id="6f4e0-122">Manipulations</span></span>](getting-started-with-manipulations.md)
</dt> </dl>

 

 




