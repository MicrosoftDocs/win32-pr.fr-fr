---
title: if (SM4-ASM)
description: Branche basée sur le ou le résultat logique.
ms.assetid: 9F4CF9E0-4D9D-4300-B432-432C560F34BB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 653c84be0d30a036bf93d852268e44bcca08bbcb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990705"
---
# <a name="if-sm4---asm"></a><span data-ttu-id="0ce79-103">if (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="0ce79-103">if (sm4 - asm)</span></span>

<span data-ttu-id="0ce79-104">Branche basée sur le ou le résultat logique.</span><span class="sxs-lookup"><span data-stu-id="0ce79-104">Branch based on logical OR result.</span></span>



| <span data-ttu-id="0ce79-105">Si { \_ z </span><span class="sxs-lookup"><span data-stu-id="0ce79-105">if{\_z</span></span>\|<span data-ttu-id="0ce79-106">\_NZ} src0. sélectionner le \_ composant</span><span class="sxs-lookup"><span data-stu-id="0ce79-106">\_nz} src0.select\_component</span></span> |
|--------------------------------------|



 



| <span data-ttu-id="0ce79-107">Élément</span><span class="sxs-lookup"><span data-stu-id="0ce79-107">Item</span></span>                                                            | <span data-ttu-id="0ce79-108">Description</span><span class="sxs-lookup"><span data-stu-id="0ce79-108">Description</span></span>                                                              |
|-----------------------------------------------------------------|--------------------------------------------------------------------------|
| <span data-ttu-id="0ce79-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="0ce79-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="0ce79-110">\[dans \] contient le composant sur lequel tester la condition.</span><span class="sxs-lookup"><span data-stu-id="0ce79-110">\[in\] Contains the component on which to test the condition.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0ce79-111">Notes</span><span class="sxs-lookup"><span data-stu-id="0ce79-111">Remarks</span></span>

<span data-ttu-id="0ce79-112">Le format de jeton contient le décalage de l’instruction ENDIF correspondante dans le nuanceur pour des raisons pratiques.</span><span class="sxs-lookup"><span data-stu-id="0ce79-112">The token format contains the offset of the corresponding endif instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="0ce79-113">L’exemple suivant montre comment utiliser cette instruction.</span><span class="sxs-lookup"><span data-stu-id="0ce79-113">The following example shows how to use this instruction.</span></span>

``` syntax
                if_z r0.x // if all bits in r0.x are zero
                   ...
                else // (optional)
                   ...
                endif
                if_nz r1.x // if any bit in r0.x is nonzero
                   ...
                else // (optional)
                   ...
                endif
```

### <a name="restrictions"></a><span data-ttu-id="0ce79-114">Restrictions</span><span class="sxs-lookup"><span data-stu-id="0ce79-114">Restrictions</span></span>

-   <span data-ttu-id="0ce79-115">Les opérandes sources (si 4 vecteurs de composant) doivent utiliser un sélecteur de composant unique.</span><span class="sxs-lookup"><span data-stu-id="0ce79-115">The source operands (if 4 component vectors) must use a single component selector.</span></span>
-   <span data-ttu-id="0ce79-116">Le registre 32 bits fourni par *src0* est testé à un niveau binaire.</span><span class="sxs-lookup"><span data-stu-id="0ce79-116">The 32-bit register supplied by *src0* is tested at a bit level.</span></span> <span data-ttu-id="0ce79-117">Si un bit est différent de zéro, **si \_ z** est true.</span><span class="sxs-lookup"><span data-stu-id="0ce79-117">If any bit is nonzero, **if\_z** will be true.</span></span> <span data-ttu-id="0ce79-118">Si tous les bits sont nuls, si la valeur **\_ NZ** est true.</span><span class="sxs-lookup"><span data-stu-id="0ce79-118">If all bits are zero, **if\_nz** will be true.</span></span>
-   <span data-ttu-id="0ce79-119">Les blocs de contrôle de Flow peuvent imbriquer jusqu’à 64 de profondeur par sous-routine (et main).</span><span class="sxs-lookup"><span data-stu-id="0ce79-119">Flow control blocks can nest up to 64 deep per subroutine (and main).</span></span> <span data-ttu-id="0ce79-120">Le compilateur HLSL ne génère pas de sous-routines qui dépassent cette limite.</span><span class="sxs-lookup"><span data-stu-id="0ce79-120">The HLSL compiler will not generate subroutines that exceed this limit.</span></span> <span data-ttu-id="0ce79-121">Le comportement des instructions de workflow de contrôle au-delà de 64 niveaux de profondeur (par sous-routine) n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="0ce79-121">Behavior of control flow instructions beyond 64 levels deep (per subroutine) is undefined.</span></span>

<span data-ttu-id="0ce79-122">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="0ce79-122">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="0ce79-123">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="0ce79-123">Vertex Shader</span></span> | <span data-ttu-id="0ce79-124">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="0ce79-124">Geometry Shader</span></span> | <span data-ttu-id="0ce79-125">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="0ce79-125">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="0ce79-126">x</span><span class="sxs-lookup"><span data-stu-id="0ce79-126">x</span></span>             | <span data-ttu-id="0ce79-127">x</span><span class="sxs-lookup"><span data-stu-id="0ce79-127">x</span></span>               | <span data-ttu-id="0ce79-128">x</span><span class="sxs-lookup"><span data-stu-id="0ce79-128">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0ce79-129">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="0ce79-129">Minimum Shader Model</span></span>

<span data-ttu-id="0ce79-130">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="0ce79-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0ce79-131">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="0ce79-131">Shader Model</span></span>                                              | <span data-ttu-id="0ce79-132">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="0ce79-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="0ce79-133">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="0ce79-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="0ce79-134">Oui</span><span class="sxs-lookup"><span data-stu-id="0ce79-134">yes</span></span>       |
| [<span data-ttu-id="0ce79-135">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="0ce79-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="0ce79-136">Oui</span><span class="sxs-lookup"><span data-stu-id="0ce79-136">yes</span></span>       |
| [<span data-ttu-id="0ce79-137">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="0ce79-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0ce79-138">Oui</span><span class="sxs-lookup"><span data-stu-id="0ce79-138">yes</span></span>       |
| [<span data-ttu-id="0ce79-139">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0ce79-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0ce79-140">non</span><span class="sxs-lookup"><span data-stu-id="0ce79-140">no</span></span>        |
| [<span data-ttu-id="0ce79-141">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0ce79-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0ce79-142">non</span><span class="sxs-lookup"><span data-stu-id="0ce79-142">no</span></span>        |
| [<span data-ttu-id="0ce79-143">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0ce79-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0ce79-144">non</span><span class="sxs-lookup"><span data-stu-id="0ce79-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="0ce79-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0ce79-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ce79-146">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0ce79-146">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





