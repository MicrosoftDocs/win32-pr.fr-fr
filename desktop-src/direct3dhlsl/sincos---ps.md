---
title: SinCos,-PS
description: Calcule le sinus et le cosinus, en radians. | SinCos,-PS
ms.assetid: 639237ea-1b7a-4959-9093-78f134c11863
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1e7ccdca91af206862384ae14cf25a85d0817814
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991993"
---
# <a name="sincos---ps"></a><span data-ttu-id="5bc59-104">SinCos,-PS</span><span class="sxs-lookup"><span data-stu-id="5bc59-104">sincos - ps</span></span>

<span data-ttu-id="5bc59-105">Calcule le sinus et le cosinus, en radians.</span><span class="sxs-lookup"><span data-stu-id="5bc59-105">Computes sine and cosine, in radians.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bc59-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5bc59-106">Syntax</span></span>

### <a name="ps_2_0-and-ps_2_x"></a><span data-ttu-id="5bc59-107">PS \_ 2 \_ 0 et PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5bc59-107">ps\_2\_0 and ps\_2\_x</span></span>



| <span data-ttu-id="5bc59-108">SinCos, DST. x</span><span class="sxs-lookup"><span data-stu-id="5bc59-108">sincos dst.{x\</span></span>|<span data-ttu-id="5bc59-109">y</span><span class="sxs-lookup"><span data-stu-id="5bc59-109">y\</span></span>|<span data-ttu-id="5bc59-110">XY}, src0. x</span><span class="sxs-lookup"><span data-stu-id="5bc59-110">xy}, src0.{x\</span></span>|<span data-ttu-id="5bc59-111">y</span><span class="sxs-lookup"><span data-stu-id="5bc59-111">y\</span></span>|<span data-ttu-id="5bc59-112">Lettre</span><span class="sxs-lookup"><span data-stu-id="5bc59-112">z\</span></span>|<span data-ttu-id="5bc59-113">w}, src1, src2</span><span class="sxs-lookup"><span data-stu-id="5bc59-113">w}, src1, src2</span></span> |
|------------------------------------------------------|



 

<span data-ttu-id="5bc59-114">Où :</span><span class="sxs-lookup"><span data-stu-id="5bc59-114">Where:</span></span>

-   <span data-ttu-id="5bc59-115">l’heure d’été est le registre de destination et doit être un [Registre temporaire](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ).</span><span class="sxs-lookup"><span data-stu-id="5bc59-115">dst is the destination register and has to be a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#).</span></span> <span data-ttu-id="5bc59-116">Le registre de destination doit avoir exactement l’un des trois masques suivants :. x. \| y. \| XY.</span><span class="sxs-lookup"><span data-stu-id="5bc59-116">The destination register must have exactly one of the following three masks: .x \| .y \| .xy.</span></span>
-   <span data-ttu-id="5bc59-117">src0 est un registre source qui fournit l’angle d’entrée, qui doit être compris entre \[ -pi, + pi \] .</span><span class="sxs-lookup"><span data-stu-id="5bc59-117">src0 is a source register that provides the input angle, which must be within \[-pi, +pi\].</span></span> <span data-ttu-id="5bc59-118">{x \| y \| z \| w} est le Swizzle de réplication requis.</span><span class="sxs-lookup"><span data-stu-id="5bc59-118">{x\|y\|z\|w} is the required replicate swizzle.</span></span>
-   <span data-ttu-id="5bc59-119">src1 et src2 sont des registres sources et doivent être deux [registres de type flottant](dx9-graphics-reference-asm-ps-registers-constant-float.md)(c \# ) différents.</span><span class="sxs-lookup"><span data-stu-id="5bc59-119">src1 and src2 are source registers and must be two different [Constant Float Register](dx9-graphics-reference-asm-ps-registers-constant-float.md)s (c\#).</span></span> <span data-ttu-id="5bc59-120">Les valeurs de src1 et src2 doivent être celles des macros [**D3DSINCOSCONST1**](/windows/desktop/direct3d9/d3dsincosconst1) et [**D3DSINCOSCONST2**](/windows/desktop/direct3d9/d3dsincosconst2) , respectivement.</span><span class="sxs-lookup"><span data-stu-id="5bc59-120">The values of src1 and src2 must be that of the macros [**D3DSINCOSCONST1**](/windows/desktop/direct3d9/d3dsincosconst1) and [**D3DSINCOSCONST2**](/windows/desktop/direct3d9/d3dsincosconst2) respectively.</span></span>

### <a name="ps_3_0"></a><span data-ttu-id="5bc59-121">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5bc59-121">ps\_3\_0</span></span>



| <span data-ttu-id="5bc59-122">SinCos, DST. x</span><span class="sxs-lookup"><span data-stu-id="5bc59-122">sincos dst.{x\</span></span>|<span data-ttu-id="5bc59-123">y</span><span class="sxs-lookup"><span data-stu-id="5bc59-123">y\</span></span>|<span data-ttu-id="5bc59-124">XY}, src0. x</span><span class="sxs-lookup"><span data-stu-id="5bc59-124">xy}, src0.{x\</span></span>|<span data-ttu-id="5bc59-125">y</span><span class="sxs-lookup"><span data-stu-id="5bc59-125">y\</span></span>|<span data-ttu-id="5bc59-126">Lettre</span><span class="sxs-lookup"><span data-stu-id="5bc59-126">z\</span></span>|<span data-ttu-id="5bc59-127">s</span><span class="sxs-lookup"><span data-stu-id="5bc59-127">w}</span></span> |
|------------------------------------------|



 

<span data-ttu-id="5bc59-128">Où :</span><span class="sxs-lookup"><span data-stu-id="5bc59-128">Where:</span></span>

-   <span data-ttu-id="5bc59-129">l’heure d’été est un registre de destination et doit être un [Registre temporaire](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ).</span><span class="sxs-lookup"><span data-stu-id="5bc59-129">dst is a destination register and has to be a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#).</span></span> <span data-ttu-id="5bc59-130">Le registre de destination doit avoir exactement l’un des trois masques suivants :. x. \| y. \| XY.</span><span class="sxs-lookup"><span data-stu-id="5bc59-130">The destination register must have exactly one of the following three masks: .x \| .y \| .xy.</span></span>
-   <span data-ttu-id="5bc59-131">src0 est un registre source qui fournit l’angle d’entrée, qui doit être compris entre \[ -pi, + pi \] .</span><span class="sxs-lookup"><span data-stu-id="5bc59-131">src0 is a source register that provides the input angle, which must be within \[-pi, +pi\].</span></span> <span data-ttu-id="5bc59-132">{x \| y \| z \| w} est le Swizzle de réplication requis.</span><span class="sxs-lookup"><span data-stu-id="5bc59-132">{x\|y\|z\|w} is the required replicate swizzle.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bc59-133">Notes</span><span class="sxs-lookup"><span data-stu-id="5bc59-133">Remarks</span></span>



| <span data-ttu-id="5bc59-134">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="5bc59-134">Pixel shader versions</span></span> | <span data-ttu-id="5bc59-135">1\_1</span><span class="sxs-lookup"><span data-stu-id="5bc59-135">1\_1</span></span> | <span data-ttu-id="5bc59-136">1\_2</span><span class="sxs-lookup"><span data-stu-id="5bc59-136">1\_2</span></span> | <span data-ttu-id="5bc59-137">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="5bc59-137">1\_3</span></span> | <span data-ttu-id="5bc59-138">1\_4</span><span class="sxs-lookup"><span data-stu-id="5bc59-138">1\_4</span></span> | <span data-ttu-id="5bc59-139">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5bc59-139">2\_0</span></span> | <span data-ttu-id="5bc59-140">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5bc59-140">2\_x</span></span> | <span data-ttu-id="5bc59-141">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="5bc59-141">2\_sw</span></span> | <span data-ttu-id="5bc59-142">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5bc59-142">3\_0</span></span> | <span data-ttu-id="5bc59-143">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="5bc59-143">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="5bc59-144">SinCos,</span><span class="sxs-lookup"><span data-stu-id="5bc59-144">sincos</span></span>                |      |      |      |      | <span data-ttu-id="5bc59-145">x</span><span class="sxs-lookup"><span data-stu-id="5bc59-145">x</span></span>    | <span data-ttu-id="5bc59-146">x</span><span class="sxs-lookup"><span data-stu-id="5bc59-146">x</span></span>    | <span data-ttu-id="5bc59-147">x</span><span class="sxs-lookup"><span data-stu-id="5bc59-147">x</span></span>     | <span data-ttu-id="5bc59-148">x</span><span class="sxs-lookup"><span data-stu-id="5bc59-148">x</span></span>    | <span data-ttu-id="5bc59-149">x</span><span class="sxs-lookup"><span data-stu-id="5bc59-149">x</span></span>     |



 

### <a name="ps_2_0-and-ps_2_x"></a><span data-ttu-id="5bc59-150">PS \_ 2 \_ 0 et PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5bc59-150">ps\_2\_0 and ps\_2\_x</span></span>

<span data-ttu-id="5bc59-151">Pour PS \_ 2 \_ 0 et PS \_ 2 \_ x, SinCos, peut être utilisé avec un prédicat, mais avec une seule restriction au Swizzle du [Registre de prédicats](dx9-graphics-reference-asm-ps-registers-predicate.md) (P0) : la seule réplication de Swizzle (. x.y. \| \| z \| ) est autorisée.</span><span class="sxs-lookup"><span data-stu-id="5bc59-151">For ps\_2\_0 and ps\_2\_x, sincos can be used with predication, but with one restriction to the swizzle of the [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md) (p0): only replicate swizzle (.x \| .y \| .z \| .w) is allowed.</span></span>

<span data-ttu-id="5bc59-152">Pour PS \_ 2 \_ 0 et PS \_ 2 \_ x, l’instruction fonctionne comme suit (V = la valeur scalaire de src0 avec un Swizzle de réplication) :</span><span class="sxs-lookup"><span data-stu-id="5bc59-152">For ps\_2\_0 and ps\_2\_x, the instruction operates as follows (V = the scalar value from src0 with a replicate swizzle):</span></span>

-   <span data-ttu-id="5bc59-153">Si le masque d’écriture est. x :</span><span class="sxs-lookup"><span data-stu-id="5bc59-153">If the write mask is .x:</span></span>
    ```
    dest.x = cos(V)
    dest.y is undefined when the instruction completes
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="5bc59-154">Si le masque d’écriture est. y :</span><span class="sxs-lookup"><span data-stu-id="5bc59-154">If the write mask is .y:</span></span>
    ```
    dest.x is undefined when the instruction completes
    dest.y = sin(V)
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="5bc59-155">Si le masque d’écriture est. XY :</span><span class="sxs-lookup"><span data-stu-id="5bc59-155">If the write mask is .xy:</span></span>
    ```
    dest.x = cos(V)
    dest.y = sin(V)
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

### <a name="ps_3_0"></a><span data-ttu-id="5bc59-156">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5bc59-156">ps\_3\_0</span></span>

<span data-ttu-id="5bc59-157">Pour PS \_ 3 \_ 0, SinCos, peut être utilisé avec un prédicat sans aucune restriction.</span><span class="sxs-lookup"><span data-stu-id="5bc59-157">For ps\_3\_0, sincos can be used with predication without any restriction.</span></span> <span data-ttu-id="5bc59-158">Consultez [Registre de prédicat](dx9-graphics-reference-asm-ps-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="5bc59-158">See [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).</span></span>

<span data-ttu-id="5bc59-159">Pour PS \_ 3 \_ 0, l’instruction fonctionne comme suit (V = la valeur scalaire de src0 avec un Swizzle de réplication) :</span><span class="sxs-lookup"><span data-stu-id="5bc59-159">For ps\_3\_0, the instruction operates as follows (V = the scalar value from src0 with a replicate swizzle):</span></span>

-   <span data-ttu-id="5bc59-160">Si le masque d’écriture est. x :</span><span class="sxs-lookup"><span data-stu-id="5bc59-160">If the write mask is .x:</span></span>
    ```
    dest.x = cos(V)
    dest.y is not touched by the instruction
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="5bc59-161">Si le masque d’écriture est. y :</span><span class="sxs-lookup"><span data-stu-id="5bc59-161">If the write mask is .y:</span></span>
    ```
    dest.x is not touched by the instruction
    dest.y = sin(V)
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="5bc59-162">Si le masque d’écriture est. XY :</span><span class="sxs-lookup"><span data-stu-id="5bc59-162">If the write mask is .xy:</span></span>
    ```
    dest.x = cos(V)
    dest.y = sin(V)
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

<span data-ttu-id="5bc59-163">L’application peut mapper un angle arbitraire (en radians) à la plage \[ -pi, + pi \] en utilisant le pseudocode de nuanceur suivant :</span><span class="sxs-lookup"><span data-stu-id="5bc59-163">The application can map an arbitrary angle (in radians) to the range \[-pi, +pi\] using the following shader pseudocode:</span></span>


```
def c0, pi, 0.5, 2*pi, 1/(2*pi)
mad r0.x, input_angle, c0.w, c0.y
frc r0.x, r0.x
mad r0.x, r0.x, c0.z, -c0.x
```



## <a name="related-topics"></a><span data-ttu-id="5bc59-164">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5bc59-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5bc59-165">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="5bc59-165">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 
