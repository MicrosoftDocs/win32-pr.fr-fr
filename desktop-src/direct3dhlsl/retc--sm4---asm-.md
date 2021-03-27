---
title: RETC (SM4-ASM)
description: Retour conditionnel.
ms.assetid: D936099D-4A75-4AE2-9FE3-70ED213DF4D9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e394bc6b947d91fafb09dbfdc075b0c60be2cf8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104971594"
---
# <a name="retc-sm4---asm"></a><span data-ttu-id="b8258-103">RETC (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="b8258-103">retc (sm4 - asm)</span></span>

<span data-ttu-id="b8258-104">Retour conditionnel.</span><span class="sxs-lookup"><span data-stu-id="b8258-104">Conditional return.</span></span>



| <span data-ttu-id="b8258-105">RETC { \_ z </span><span class="sxs-lookup"><span data-stu-id="b8258-105">retc{\_z</span></span>\|<span data-ttu-id="b8258-106">\_NZ} src0. sélectionner le \_ composant</span><span class="sxs-lookup"><span data-stu-id="b8258-106">\_nz} src0.select\_component</span></span> |
|----------------------------------------|



 



| <span data-ttu-id="b8258-107">Élément</span><span class="sxs-lookup"><span data-stu-id="b8258-107">Item</span></span>                                                            | <span data-ttu-id="b8258-108">Description</span><span class="sxs-lookup"><span data-stu-id="b8258-108">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="b8258-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="b8258-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="b8258-110">\[dans \] le registre pour tester la condition.</span><span class="sxs-lookup"><span data-stu-id="b8258-110">\[in\] The register to test the condition against.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b8258-111">Notes</span><span class="sxs-lookup"><span data-stu-id="b8258-111">Remarks</span></span>

<span data-ttu-id="b8258-112">Si, dans une sous-routine, cette instruction retourne de manière conditionnelle à l’instruction après l’appel.</span><span class="sxs-lookup"><span data-stu-id="b8258-112">If within a subroutine, this instruction conditionally returns to the instruction after the call.</span></span> <span data-ttu-id="b8258-113">Si elle ne se trouve pas à l’intérieur d’une sous-routine, cette instruction termine l’exécution du programme.</span><span class="sxs-lookup"><span data-stu-id="b8258-113">If not inside a subroutine, this instruction terminates program execution.</span></span>

<span data-ttu-id="b8258-114">L’exemple suivant montre comment utiliser cette instruction.</span><span class="sxs-lookup"><span data-stu-id="b8258-114">The following example shows how to use this instruction.</span></span>

``` syntax
           ...
           call l3
           ...
           ret
           label l3
               ...
               retc_nz r0.x  // If any bit in r0.x is nonzero, then return
               retc_z  r1.x  // If all bits in r0.x are zero, then return.
               ...
           ret
```

### <a name="restrictions"></a><span data-ttu-id="b8258-115">Restrictions</span><span class="sxs-lookup"><span data-stu-id="b8258-115">Restrictions</span></span>

-   <span data-ttu-id="b8258-116">**RETC** peut apparaître n’importe où dans un programme, un nombre quelconque de fois.</span><span class="sxs-lookup"><span data-stu-id="b8258-116">**retc** can appear anywhere in a program, any number of times.</span></span>
-   <span data-ttu-id="b8258-117">La dernière instruction d’un programme ou d’une sous-routine principale ne peut pas être un **RETC \_ z** ou **RETC \_ NZ**.</span><span class="sxs-lookup"><span data-stu-id="b8258-117">The last instruction in a main program or subroutine cannot be a **retc\_z** or **retc\_nz**.</span></span> <span data-ttu-id="b8258-118">Au lieu de cela, la [RET](ret--sm4---asm-.md) inconditionnelle peut être utilisée.</span><span class="sxs-lookup"><span data-stu-id="b8258-118">Instead, the unconditional [ret](ret--sm4---asm-.md) can be used.</span></span>
-   <span data-ttu-id="b8258-119">Le registre 32 bits fourni par *src0* est testé à un niveau binaire.</span><span class="sxs-lookup"><span data-stu-id="b8258-119">The 32-bit register supplied by *src0* is tested at a bit level.</span></span> <span data-ttu-id="b8258-120">Si un bit est différent de zéro, la valeur **RET \_ NZ** retourne.</span><span class="sxs-lookup"><span data-stu-id="b8258-120">If any bit is nonzero, **ret\_nz** will return.</span></span> <span data-ttu-id="b8258-121">Si tous les bits sont nuls, **RETC \_ z** retourne.</span><span class="sxs-lookup"><span data-stu-id="b8258-121">If all bits are zero, **retc\_z** will return.</span></span>

<span data-ttu-id="b8258-122">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="b8258-122">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="b8258-123">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="b8258-123">Vertex Shader</span></span> | <span data-ttu-id="b8258-124">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="b8258-124">Geometry Shader</span></span> | <span data-ttu-id="b8258-125">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="b8258-125">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="b8258-126">x</span><span class="sxs-lookup"><span data-stu-id="b8258-126">x</span></span>             | <span data-ttu-id="b8258-127">x</span><span class="sxs-lookup"><span data-stu-id="b8258-127">x</span></span>               | <span data-ttu-id="b8258-128">x</span><span class="sxs-lookup"><span data-stu-id="b8258-128">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b8258-129">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="b8258-129">Minimum Shader Model</span></span>

<span data-ttu-id="b8258-130">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="b8258-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b8258-131">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="b8258-131">Shader Model</span></span>                                              | <span data-ttu-id="b8258-132">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="b8258-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b8258-133">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="b8258-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="b8258-134">Oui</span><span class="sxs-lookup"><span data-stu-id="b8258-134">yes</span></span>       |
| [<span data-ttu-id="b8258-135">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="b8258-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="b8258-136">Oui</span><span class="sxs-lookup"><span data-stu-id="b8258-136">yes</span></span>       |
| [<span data-ttu-id="b8258-137">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="b8258-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b8258-138">Oui</span><span class="sxs-lookup"><span data-stu-id="b8258-138">yes</span></span>       |
| [<span data-ttu-id="b8258-139">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b8258-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b8258-140">non</span><span class="sxs-lookup"><span data-stu-id="b8258-140">no</span></span>        |
| [<span data-ttu-id="b8258-141">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b8258-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b8258-142">non</span><span class="sxs-lookup"><span data-stu-id="b8258-142">no</span></span>        |
| [<span data-ttu-id="b8258-143">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b8258-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b8258-144">non</span><span class="sxs-lookup"><span data-stu-id="b8258-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b8258-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b8258-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8258-146">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b8258-146">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





