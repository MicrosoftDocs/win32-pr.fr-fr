---
title: dmovc (SM5-ASM)
description: Déplacement conditionnel au niveau du composant. | dmovc (SM5-ASM)
ms.assetid: E376FE08-E251-4BE5-9F15-99B3B67A29C8
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e364e6340733c42ae69412db726851329eb2809d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104393931"
---
# <a name="dmovc-sm5---asm"></a><span data-ttu-id="4f987-104">dmovc (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="4f987-104">dmovc (sm5 - asm)</span></span>

<span data-ttu-id="4f987-105">Déplacement conditionnel au niveau du composant.</span><span class="sxs-lookup"><span data-stu-id="4f987-105">Component-wise conditional move.</span></span>



| <span data-ttu-id="4f987-106">dmovc \[ \_ SAT \] dest \[ . Mask \] , src0 \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src2 \[ \_ ABS \] \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="4f987-106">dmovc\[\_sat\] dest\[.mask\], src0\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\], \[-\]src2\[\_abs\]\[.swizzle\],</span></span> |
|-----------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="4f987-107">Élément</span><span class="sxs-lookup"><span data-stu-id="4f987-107">Item</span></span>                                                            | <span data-ttu-id="4f987-108">Description</span><span class="sxs-lookup"><span data-stu-id="4f987-108">Description</span></span>                                                                                              |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f987-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="4f987-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="4f987-110">\[dans \] la destination de déplacement.</span><span class="sxs-lookup"><span data-stu-id="4f987-110">\[in\] The move destination.</span></span><br/> <span data-ttu-id="4f987-111">Si *src0*, puis *dest*  =  *src1* else *dest*  =  *src2*.</span><span class="sxs-lookup"><span data-stu-id="4f987-111">If *src0*, then *dest* = *src1* else *dest* = *src2*.</span></span><br/> |
| <span data-ttu-id="4f987-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="4f987-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="4f987-113">\[dans \] les composants pour tester la condition.</span><span class="sxs-lookup"><span data-stu-id="4f987-113">\[in\] The components to test the condition against.</span></span><br/>                                          |
| <span data-ttu-id="4f987-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="4f987-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="4f987-115">\[dans \] les composants à déplacer si la condition a la valeur true.</span><span class="sxs-lookup"><span data-stu-id="4f987-115">\[in\] The components to move if the condition is true.</span></span><br/>                                       |
| <span data-ttu-id="4f987-116"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="4f987-116"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="4f987-117">\[dans \] les composants à déplacer si la condition est false.</span><span class="sxs-lookup"><span data-stu-id="4f987-117">\[in\] The components to move if the condition is false.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="4f987-118">Notes</span><span class="sxs-lookup"><span data-stu-id="4f987-118">Remarks</span></span>

<span data-ttu-id="4f987-119">L’exemple suivant montre comment utiliser cette instruction.</span><span class="sxs-lookup"><span data-stu-id="4f987-119">The following example shows how to use this instruction.</span></span>

``` syntax
                if(the dest mask contains .xy)
                {
                    if(the first 32-bit component of src0, post-swizzle, 
                       has any bit set)
                    {
                        copy the first double from src1 (post swizzle)
                        into dest.xy
                    }
                    else
                    {
                        copy the first double from src2 (post swizzle)
                        into dest.xy
                    }
                }
                if(the dest mask contains .zw)
                {
                    if(the second 32-bit component of src0, post-swizzle, 
                       has any bit set)
                    {
                        copy the second double from src1 (post swizzle)
                        into dest.zw
                    }
                    else
                    {
                        copy the second double from src2 (post swizzle)
                        into dest.zw
                    }
                }
```

<span data-ttu-id="4f987-120">Les masques valides pour dest sont. XY,. ZW,. XYZW.</span><span class="sxs-lookup"><span data-stu-id="4f987-120">The valid masks for dest are .xy, .zw, .xyzw.</span></span>

<span data-ttu-id="4f987-121">Le Swizzles valide pour *src0* est n’importe quoi.</span><span class="sxs-lookup"><span data-stu-id="4f987-121">The valid swizzles for *src0* are anything.</span></span> <span data-ttu-id="4f987-122">Les deux premiers composants Swizzle sont utilisés pour faciliteront son identification les valeurs de condition de 2 32 bits.</span><span class="sxs-lookup"><span data-stu-id="4f987-122">The first two components post-swizzle are used to indentify two 32-bit condition values.</span></span>

<span data-ttu-id="4f987-123">Le Swizzles valide pour *src1* et *src2* contenant des doubles sont. XYZW,. Xyxy,. zwxy,. zwzw.</span><span class="sxs-lookup"><span data-stu-id="4f987-123">The valid swizzles for *src1* and *src2* containing doubles are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="4f987-124">sont. XY,. ZW et. XYZW.</span><span class="sxs-lookup"><span data-stu-id="4f987-124">are .xy, .zw, and .xyzw.</span></span>

<span data-ttu-id="4f987-125">Les mappages *src* ci-dessous sont postérieurs à Swizzle :</span><span class="sxs-lookup"><span data-stu-id="4f987-125">The following *src* mappings below are post-swizzle:</span></span>

-   <span data-ttu-id="4f987-126">*dest* est un double vec2 entre (x 32LSB, y 32MSB) et (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="4f987-126">*dest* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="4f987-127">*src0* est un vec2 de composant/32 bits sur x et y (ZW ignoré).</span><span class="sxs-lookup"><span data-stu-id="4f987-127">*src0* is a 32bit/component vec2 across x and y (zw ignored).</span></span>
-   <span data-ttu-id="4f987-128">*src1* est un double vec2 entre (x 32LSB, y 32MSB) et (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="4f987-128">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="4f987-129">*src2* est un double vec2 entre (x 32LSB, y 32MSB) et (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="4f987-129">*src2* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="4f987-130">Les modificateurs sur *src1* et *src2*, à l’exception de Swizzle, supposent que les données sont de type double.</span><span class="sxs-lookup"><span data-stu-id="4f987-130">The modifiers on *src1* and *src2*, other than swizzle, assume the data is double.</span></span> <span data-ttu-id="4f987-131">L’absence de modificateurs déplace les données sans modifier les bits.</span><span class="sxs-lookup"><span data-stu-id="4f987-131">The absence of modifiers moves data without altering bits.</span></span>

<span data-ttu-id="4f987-132">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="4f987-132">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="4f987-133">Sommet</span><span class="sxs-lookup"><span data-stu-id="4f987-133">Vertex</span></span> | <span data-ttu-id="4f987-134">Forme</span><span class="sxs-lookup"><span data-stu-id="4f987-134">Hull</span></span> | <span data-ttu-id="4f987-135">Domain</span><span class="sxs-lookup"><span data-stu-id="4f987-135">Domain</span></span> | <span data-ttu-id="4f987-136">Géométrie</span><span class="sxs-lookup"><span data-stu-id="4f987-136">Geometry</span></span> | <span data-ttu-id="4f987-137">Pixel</span><span class="sxs-lookup"><span data-stu-id="4f987-137">Pixel</span></span> | <span data-ttu-id="4f987-138">Compute</span><span class="sxs-lookup"><span data-stu-id="4f987-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="4f987-139">X</span><span class="sxs-lookup"><span data-stu-id="4f987-139">X</span></span>      | <span data-ttu-id="4f987-140">X</span><span class="sxs-lookup"><span data-stu-id="4f987-140">X</span></span>    | <span data-ttu-id="4f987-141">X</span><span class="sxs-lookup"><span data-stu-id="4f987-141">X</span></span>      | <span data-ttu-id="4f987-142">X</span><span class="sxs-lookup"><span data-stu-id="4f987-142">X</span></span>        | <span data-ttu-id="4f987-143">X</span><span class="sxs-lookup"><span data-stu-id="4f987-143">X</span></span>     | <span data-ttu-id="4f987-144">X</span><span class="sxs-lookup"><span data-stu-id="4f987-144">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4f987-145">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="4f987-145">Minimum Shader Model</span></span>

<span data-ttu-id="4f987-146">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="4f987-146">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="4f987-147">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="4f987-147">Shader Model</span></span>                                              | <span data-ttu-id="4f987-148">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="4f987-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="4f987-149">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="4f987-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="4f987-150">Oui</span><span class="sxs-lookup"><span data-stu-id="4f987-150">yes</span></span>       |
| [<span data-ttu-id="4f987-151">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="4f987-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="4f987-152">non</span><span class="sxs-lookup"><span data-stu-id="4f987-152">no</span></span>        |
| [<span data-ttu-id="4f987-153">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="4f987-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="4f987-154">non</span><span class="sxs-lookup"><span data-stu-id="4f987-154">no</span></span>        |
| [<span data-ttu-id="4f987-155">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4f987-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="4f987-156">non</span><span class="sxs-lookup"><span data-stu-id="4f987-156">no</span></span>        |
| [<span data-ttu-id="4f987-157">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4f987-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="4f987-158">non</span><span class="sxs-lookup"><span data-stu-id="4f987-158">no</span></span>        |
| [<span data-ttu-id="4f987-159">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4f987-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="4f987-160">non</span><span class="sxs-lookup"><span data-stu-id="4f987-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="4f987-161">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4f987-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f987-162">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4f987-162">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





