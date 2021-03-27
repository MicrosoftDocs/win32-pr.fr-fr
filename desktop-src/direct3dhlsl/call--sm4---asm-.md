---
title: appel (SM4-ASM)
description: Appelle une sous-routine marquée par où l’étiquette l \ apparaît dans le programme.
ms.assetid: D6B7C52D-2CF7-44DB-81E3-2945477EF94A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dac86fa52140968443f01050cebc57718fea420
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679133"
---
# <a name="call-sm4---asm"></a><span data-ttu-id="7d83b-103">appel (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="7d83b-103">call (sm4 - asm)</span></span>

<span data-ttu-id="7d83b-104">Appelle une sous-routine marquée par l’emplacement où l’étiquette **l \#** apparaît dans le programme.</span><span class="sxs-lookup"><span data-stu-id="7d83b-104">Calls a subroutine marked by where the label **l\#** appears in the program.</span></span>



| <span data-ttu-id="7d83b-105">appeler l\#</span><span class="sxs-lookup"><span data-stu-id="7d83b-105">call l\#</span></span> |
|----------|



 



| <span data-ttu-id="7d83b-106">Élément</span><span class="sxs-lookup"><span data-stu-id="7d83b-106">Item</span></span>                                                       | <span data-ttu-id="7d83b-107">Description</span><span class="sxs-lookup"><span data-stu-id="7d83b-107">Description</span></span>                                    |
|------------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="7d83b-108"><span id="l_"></span><span id="L_"></span>*budget\#*</span><span class="sxs-lookup"><span data-stu-id="7d83b-108"><span id="l_"></span><span id="L_"></span>*l\#*</span></span><br/> | <span data-ttu-id="7d83b-109">\[dans \] l’étiquette de la sous-routine.</span><span class="sxs-lookup"><span data-stu-id="7d83b-109">\[in\] The label of the subroutine.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7d83b-110">Notes</span><span class="sxs-lookup"><span data-stu-id="7d83b-110">Remarks</span></span>

<span data-ttu-id="7d83b-111">Quand un [RET](ret--sm4---asm-.md) est rencontré, retourne l’exécution à l’instruction après cet appel.</span><span class="sxs-lookup"><span data-stu-id="7d83b-111">When a [ret](ret--sm4---asm-.md) is encountered, return execution to the instruction after this call.</span></span>

<span data-ttu-id="7d83b-112">Le format de jeton contient le décalage de l’étiquette correspondante dans le nuanceur pour des raisons pratiques.</span><span class="sxs-lookup"><span data-stu-id="7d83b-112">The token format contains the offset of the corresponding label in the Shader as a convenience.</span></span>

<span data-ttu-id="7d83b-113">L’exemple suivant illustre l’instruction call.</span><span class="sxs-lookup"><span data-stu-id="7d83b-113">The following example shows the call instruction.</span></span>


```
                ...
                call l3
                ...
                ret
                label l3
                    ...
                    retc_nz r0.x
                    ...
                ret
```



### <a name="restrictions"></a><span data-ttu-id="7d83b-114">Restrictions</span><span class="sxs-lookup"><span data-stu-id="7d83b-114">Restrictions</span></span>

-   <span data-ttu-id="7d83b-115">Les sous-routines peuvent imbriquer 32 en profondeur.</span><span class="sxs-lookup"><span data-stu-id="7d83b-115">Subroutines can nest 32 deep.</span></span>
-   <span data-ttu-id="7d83b-116">La pile d’adresses de retour est gérée de façon transparente par l’implémentation de.</span><span class="sxs-lookup"><span data-stu-id="7d83b-116">The return address stack is managed transparently by the implementation.</span></span>
-   <span data-ttu-id="7d83b-117">S’il existe déjà 32 entrées sur la pile d’adresses de retour et qu’un **appel** est émis, l’appel est ignoré.</span><span class="sxs-lookup"><span data-stu-id="7d83b-117">If there are already 32 entries on the return address stack and a **call** is issued, the call is skipped over.</span></span>
-   <span data-ttu-id="7d83b-118">Il n’existe pas de pile de paramètres automatique.</span><span class="sxs-lookup"><span data-stu-id="7d83b-118">There is no automatic parameter stack.</span></span> <span data-ttu-id="7d83b-119">L’application peut utiliser un tableau de registres temporaire indexable (x \# \[ \] ) pour implémenter manuellement une pile.</span><span class="sxs-lookup"><span data-stu-id="7d83b-119">The application can use an indexable temporary register array (x\#\[\]) to manually implement a stack.</span></span> <span data-ttu-id="7d83b-120">Toutefois, les adresses de retour d’appel de sous-routine ne sont pas visibles et sont orthogonales à toute gestion de pile manuelle effectuée par l’application.</span><span class="sxs-lookup"><span data-stu-id="7d83b-120">However, the subroutine call return addresses are not visible and are orthogonal to any manual stack management done by the application.</span></span>
-   <span data-ttu-id="7d83b-121">L’indexation du paramètre *l \#* n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="7d83b-121">Indexing of the *l\#* parameter is not permitted.</span></span>
-   <span data-ttu-id="7d83b-122">La récursivité n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="7d83b-122">Recursion is not permitted.</span></span>

<span data-ttu-id="7d83b-123">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="7d83b-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="7d83b-124">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="7d83b-124">Vertex Shader</span></span> | <span data-ttu-id="7d83b-125">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="7d83b-125">Geometry Shader</span></span> | <span data-ttu-id="7d83b-126">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="7d83b-126">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="7d83b-127">x</span><span class="sxs-lookup"><span data-stu-id="7d83b-127">x</span></span>             | <span data-ttu-id="7d83b-128">x</span><span class="sxs-lookup"><span data-stu-id="7d83b-128">x</span></span>               | <span data-ttu-id="7d83b-129">x</span><span class="sxs-lookup"><span data-stu-id="7d83b-129">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7d83b-130">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="7d83b-130">Minimum Shader Model</span></span>

<span data-ttu-id="7d83b-131">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="7d83b-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="7d83b-132">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="7d83b-132">Shader Model</span></span>                                              | <span data-ttu-id="7d83b-133">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="7d83b-133">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="7d83b-134">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="7d83b-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="7d83b-135">Oui</span><span class="sxs-lookup"><span data-stu-id="7d83b-135">yes</span></span>       |
| [<span data-ttu-id="7d83b-136">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="7d83b-136">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="7d83b-137">Oui</span><span class="sxs-lookup"><span data-stu-id="7d83b-137">yes</span></span>       |
| [<span data-ttu-id="7d83b-138">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="7d83b-138">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="7d83b-139">Oui</span><span class="sxs-lookup"><span data-stu-id="7d83b-139">yes</span></span>       |
| [<span data-ttu-id="7d83b-140">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7d83b-140">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="7d83b-141">non</span><span class="sxs-lookup"><span data-stu-id="7d83b-141">no</span></span>        |
| [<span data-ttu-id="7d83b-142">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7d83b-142">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="7d83b-143">non</span><span class="sxs-lookup"><span data-stu-id="7d83b-143">no</span></span>        |
| [<span data-ttu-id="7d83b-144">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7d83b-144">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="7d83b-145">non</span><span class="sxs-lookup"><span data-stu-id="7d83b-145">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="7d83b-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7d83b-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d83b-147">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7d83b-147">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





