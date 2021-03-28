---
title: callc (SM4-ASM)
description: Appelle de manière conditionnelle une sous-routine marquée par où l’étiquette l \ apparaît dans le programme.
ms.assetid: 7F6E81CE-0C38-499B-B83E-FA76FA154451
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6bc8c9d1e4a99ce25f99253518482181cdb74d8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990760"
---
# <a name="callc-sm4---asm"></a><span data-ttu-id="5af49-103">callc (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="5af49-103">callc (sm4 - asm)</span></span>

<span data-ttu-id="5af49-104">Appelle de manière conditionnelle une sous-routine marquée par où l’étiquette **l \#** apparaît dans le programme.</span><span class="sxs-lookup"><span data-stu-id="5af49-104">Conditionally calls a subroutine marked by where the label **l\#** appears in the program.</span></span>



| <span data-ttu-id="5af49-105">callc { \_ z </span><span class="sxs-lookup"><span data-stu-id="5af49-105">callc{\_z</span></span>\|<span data-ttu-id="5af49-106">\_NZ} src0. Sélectionnez le \_ composant, l\#</span><span class="sxs-lookup"><span data-stu-id="5af49-106">\_nz} src0.select\_component, l\#</span></span> |
|----------------------------------------------|



 



| <span data-ttu-id="5af49-107">Élément</span><span class="sxs-lookup"><span data-stu-id="5af49-107">Item</span></span>                                                            | <span data-ttu-id="5af49-108">Description</span><span class="sxs-lookup"><span data-stu-id="5af49-108">Description</span></span>                                                     |
|-----------------------------------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="5af49-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="5af49-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="5af49-110">\[dans \] le composant sur lequel tester la condition.</span><span class="sxs-lookup"><span data-stu-id="5af49-110">\[in\] The component on which to test the condition.</span></span><br/> |
| <span data-ttu-id="5af49-111"><span id="l_"></span><span id="L_"></span>*budget\#*</span><span class="sxs-lookup"><span data-stu-id="5af49-111"><span id="l_"></span><span id="L_"></span>*l\#*</span></span><br/>      | <span data-ttu-id="5af49-112">\[dans \] l’étiquette de la sous-routine.</span><span class="sxs-lookup"><span data-stu-id="5af49-112">\[in\] The label of the subroutine.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="5af49-113">Notes</span><span class="sxs-lookup"><span data-stu-id="5af49-113">Remarks</span></span>

<span data-ttu-id="5af49-114">Quand un [RET](ret--sm4---asm-.md) est rencontré, retourne l’exécution à l’instruction après cet appel.</span><span class="sxs-lookup"><span data-stu-id="5af49-114">When a [ret](ret--sm4---asm-.md) is encountered, return execution to the instruction after this call.</span></span>

<span data-ttu-id="5af49-115">Le format de jeton contient le décalage de l’étiquette correspondante dans le nuanceur pour des raisons pratiques.</span><span class="sxs-lookup"><span data-stu-id="5af49-115">The token format contains the offset of the corresponding label in the Shader as a convenience.</span></span>

<span data-ttu-id="5af49-116">L’exemple suivant illustre l’instruction call.</span><span class="sxs-lookup"><span data-stu-id="5af49-116">The following example shows the call instruction.</span></span>


```
                ...
                callc_z  r1.y, l3 // if all bits in r0.x are 0, call l3
                callc_nz r2.z, l3 // if any bit in r0.x is nonzero, call l3
                ...
                ret
                label l3
                    ...
                    retc_nz r0.x
                    ...
                ret

```



### <a name="restrictions"></a><span data-ttu-id="5af49-117">Restrictions</span><span class="sxs-lookup"><span data-stu-id="5af49-117">Restrictions</span></span>

-   <span data-ttu-id="5af49-118">Les sous-routines peuvent imbriquer 32 en profondeur.</span><span class="sxs-lookup"><span data-stu-id="5af49-118">Subroutines can nest 32 deep.</span></span>
-   <span data-ttu-id="5af49-119">La pile d’adresses de retour est gérée de façon transparente par l’implémentation de.</span><span class="sxs-lookup"><span data-stu-id="5af49-119">The return address stack is managed transparently by the implementation.</span></span>
-   <span data-ttu-id="5af49-120">S’il existe déjà 32 entrées sur la pile d’adresses de retour et qu’un **appel** est émis, l’appel est ignoré.</span><span class="sxs-lookup"><span data-stu-id="5af49-120">If there are already 32 entries on the return address stack and a **call** is issued, the call is skipped over.</span></span>
-   <span data-ttu-id="5af49-121">Il n’existe pas de pile de paramètres automatique.</span><span class="sxs-lookup"><span data-stu-id="5af49-121">There is no automatic parameter stack.</span></span> <span data-ttu-id="5af49-122">L’application peut utiliser un tableau de registres temporaire indexable (x \# \[ \] ) pour implémenter manuellement une pile.</span><span class="sxs-lookup"><span data-stu-id="5af49-122">The application can use an indexable temporary register array (x\#\[\]) to manually implement a stack.</span></span> <span data-ttu-id="5af49-123">Toutefois, les adresses de retour d’appel de sous-routine ne sont pas visibles et sont orthogonales à toute gestion de pile manuelle effectuée par l’application.</span><span class="sxs-lookup"><span data-stu-id="5af49-123">However, the subroutine call return addresses are not visible and are orthogonal to any manual stack management done by the application.</span></span>
-   <span data-ttu-id="5af49-124">L’indexation du paramètre *l \#* n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="5af49-124">Indexing of the *l\#* parameter is not permitted.</span></span>
-   <span data-ttu-id="5af49-125">Le registre 32 bits fourni par *src0* est testé à un niveau binaire.</span><span class="sxs-lookup"><span data-stu-id="5af49-125">The 32-bit register supplied by *src0* is tested at a bit level.</span></span> <span data-ttu-id="5af49-126">Si un bit est différent de zéro, **callc \_ NZ** effectue l’appel.</span><span class="sxs-lookup"><span data-stu-id="5af49-126">If any bit is nonzero, **callc\_nz** will perform the call.</span></span> <span data-ttu-id="5af49-127">Si tous les bits sont nuls, **callc \_ z** effectue l’appel.</span><span class="sxs-lookup"><span data-stu-id="5af49-127">If all bits are zero, **callc\_z** will perform the call.</span></span>
-   <span data-ttu-id="5af49-128">La récursivité n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="5af49-128">Recursion is not permitted.</span></span>

<span data-ttu-id="5af49-129">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="5af49-129">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="5af49-130">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="5af49-130">Vertex Shader</span></span> | <span data-ttu-id="5af49-131">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="5af49-131">Geometry Shader</span></span> | <span data-ttu-id="5af49-132">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="5af49-132">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="5af49-133">x</span><span class="sxs-lookup"><span data-stu-id="5af49-133">x</span></span>             | <span data-ttu-id="5af49-134">x</span><span class="sxs-lookup"><span data-stu-id="5af49-134">x</span></span>               | <span data-ttu-id="5af49-135">x</span><span class="sxs-lookup"><span data-stu-id="5af49-135">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5af49-136">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="5af49-136">Minimum Shader Model</span></span>

<span data-ttu-id="5af49-137">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="5af49-137">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="5af49-138">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="5af49-138">Shader Model</span></span>                                              | <span data-ttu-id="5af49-139">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="5af49-139">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="5af49-140">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="5af49-140">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="5af49-141">Oui</span><span class="sxs-lookup"><span data-stu-id="5af49-141">yes</span></span>       |
| [<span data-ttu-id="5af49-142">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="5af49-142">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="5af49-143">Oui</span><span class="sxs-lookup"><span data-stu-id="5af49-143">yes</span></span>       |
| [<span data-ttu-id="5af49-144">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="5af49-144">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="5af49-145">Oui</span><span class="sxs-lookup"><span data-stu-id="5af49-145">yes</span></span>       |
| [<span data-ttu-id="5af49-146">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5af49-146">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5af49-147">non</span><span class="sxs-lookup"><span data-stu-id="5af49-147">no</span></span>        |
| [<span data-ttu-id="5af49-148">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5af49-148">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="5af49-149">non</span><span class="sxs-lookup"><span data-stu-id="5af49-149">no</span></span>        |
| [<span data-ttu-id="5af49-150">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5af49-150">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="5af49-151">non</span><span class="sxs-lookup"><span data-stu-id="5af49-151">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="5af49-152">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5af49-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5af49-153">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5af49-153">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





