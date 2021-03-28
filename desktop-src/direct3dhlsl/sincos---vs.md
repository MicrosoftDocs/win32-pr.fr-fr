---
title: SinCos,-vs
description: Calcule le sinus et le cosinus, en radians. | SinCos,-vs
ms.assetid: 733a3980-ceaf-43dc-a862-923c369e4a65
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ca70a319852346c6e75ba544489d033a861d4c3b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103953732"
---
# <a name="sincos---vs"></a><span data-ttu-id="a0097-104">SinCos,-vs</span><span class="sxs-lookup"><span data-stu-id="a0097-104">sincos - vs</span></span>

<span data-ttu-id="a0097-105">Calcule le sinus et le cosinus, en radians.</span><span class="sxs-lookup"><span data-stu-id="a0097-105">Computes sine and cosine, in radians.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0097-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a0097-106">Syntax</span></span>

### <a name="vs_2_0-and-vs_2_x"></a><span data-ttu-id="a0097-107">vs \_ 2 \_ 0 et vs \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a0097-107">vs\_2\_0 and vs\_2\_x</span></span>



| <span data-ttu-id="a0097-108">SinCos, DST. x</span><span class="sxs-lookup"><span data-stu-id="a0097-108">sincos dst.{x\</span></span>|<span data-ttu-id="a0097-109">y</span><span class="sxs-lookup"><span data-stu-id="a0097-109">y\</span></span>|<span data-ttu-id="a0097-110">XY}, src0. x</span><span class="sxs-lookup"><span data-stu-id="a0097-110">xy}, src0.{x\</span></span>|<span data-ttu-id="a0097-111">y</span><span class="sxs-lookup"><span data-stu-id="a0097-111">y\</span></span>|<span data-ttu-id="a0097-112">Lettre</span><span class="sxs-lookup"><span data-stu-id="a0097-112">z\</span></span>|<span data-ttu-id="a0097-113">w}, src1, src2</span><span class="sxs-lookup"><span data-stu-id="a0097-113">w}, src1, src2</span></span> |
|------------------------------------------------------|



 

<span data-ttu-id="a0097-114">Où :</span><span class="sxs-lookup"><span data-stu-id="a0097-114">Where:</span></span>

-   <span data-ttu-id="a0097-115">l’heure d’été est le registre de destination et doit être un [Registre temporaire](dx9-graphics-reference-asm-vs-registers-temporary.md) (r \# ).</span><span class="sxs-lookup"><span data-stu-id="a0097-115">dst is the destination register and has to be a [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md) (r\#).</span></span> <span data-ttu-id="a0097-116">Le registre de destination doit avoir exactement l’un des trois masques suivants :. x. \| y. \| XY.</span><span class="sxs-lookup"><span data-stu-id="a0097-116">The destination register must have exactly one of the following three masks: .x \| .y \| .xy.</span></span>
-   <span data-ttu-id="a0097-117">src0 est un registre source qui fournit l’angle d’entrée, qui doit être compris entre \[ -pi, + pi \] .</span><span class="sxs-lookup"><span data-stu-id="a0097-117">src0 is a source register that provides the input angle, which must be within \[-pi, +pi\].</span></span> <span data-ttu-id="a0097-118">{x \| y \| z \| w} est le Swizzle de réplication requis.</span><span class="sxs-lookup"><span data-stu-id="a0097-118">{x\|y\|z\|w} is the required replicate swizzle.</span></span>
-   <span data-ttu-id="a0097-119">src1 et src2 sont des registres sources et doivent être des registres à [virgule flottante constantes](dx9-graphics-reference-asm-vs-registers-constant-float.md) différents (c \# ).</span><span class="sxs-lookup"><span data-stu-id="a0097-119">src1 and src2 are source registers and must be two different [Constant Float Register](dx9-graphics-reference-asm-vs-registers-constant-float.md) (c\#).</span></span> <span data-ttu-id="a0097-120">Les valeurs de src1 et src2 doivent être celles des macros [**D3DSINCOSCONST1**](/windows/desktop/direct3d9/d3dsincosconst1) et [**D3DSINCOSCONST2**](/windows/desktop/direct3d9/d3dsincosconst2) , respectivement.</span><span class="sxs-lookup"><span data-stu-id="a0097-120">The values of src1 and src2 must be that of the macros [**D3DSINCOSCONST1**](/windows/desktop/direct3d9/d3dsincosconst1) and [**D3DSINCOSCONST2**](/windows/desktop/direct3d9/d3dsincosconst2) respectively.</span></span>

### <a name="vs_3_0"></a><span data-ttu-id="a0097-121">vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a0097-121">vs\_3\_0</span></span>



| <span data-ttu-id="a0097-122">SinCos, DST. x</span><span class="sxs-lookup"><span data-stu-id="a0097-122">sincos dst.{x\</span></span>|<span data-ttu-id="a0097-123">y</span><span class="sxs-lookup"><span data-stu-id="a0097-123">y\</span></span>|<span data-ttu-id="a0097-124">XY}, src0. x</span><span class="sxs-lookup"><span data-stu-id="a0097-124">xy}, src0.{x\</span></span>|<span data-ttu-id="a0097-125">y</span><span class="sxs-lookup"><span data-stu-id="a0097-125">y\</span></span>|<span data-ttu-id="a0097-126">Lettre</span><span class="sxs-lookup"><span data-stu-id="a0097-126">z\</span></span>|<span data-ttu-id="a0097-127">s</span><span class="sxs-lookup"><span data-stu-id="a0097-127">w}</span></span> |
|------------------------------------------|



 

<span data-ttu-id="a0097-128">Où :</span><span class="sxs-lookup"><span data-stu-id="a0097-128">Where:</span></span>

-   <span data-ttu-id="a0097-129">l’heure d’été est un registre de destination et doit être un [Registre temporaire](dx9-graphics-reference-asm-vs-registers-temporary.md) (r \# ).</span><span class="sxs-lookup"><span data-stu-id="a0097-129">dst is a destination register and has to be a [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md) (r\#).</span></span> <span data-ttu-id="a0097-130">Le registre de destination doit avoir exactement l’un des trois masques suivants :. x. \| y. \| XY.</span><span class="sxs-lookup"><span data-stu-id="a0097-130">The destination register must have exactly one of the following three masks: .x \| .y \| .xy.</span></span>
-   <span data-ttu-id="a0097-131">src0 est un registre source qui fournit l’angle d’entrée, qui doit être compris entre \[ -pi, + pi \] .</span><span class="sxs-lookup"><span data-stu-id="a0097-131">src0 is a source register that provides the input angle, which must be within \[-pi, +pi\].</span></span> <span data-ttu-id="a0097-132">{x \| y \| z \| w} est le Swizzle de réplication requis.</span><span class="sxs-lookup"><span data-stu-id="a0097-132">{x\|y\|z\|w} is the required replicate swizzle.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0097-133">Notes</span><span class="sxs-lookup"><span data-stu-id="a0097-133">Remarks</span></span>



| <span data-ttu-id="a0097-134">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="a0097-134">Vertex shader versions</span></span> | <span data-ttu-id="a0097-135">1\_1</span><span class="sxs-lookup"><span data-stu-id="a0097-135">1\_1</span></span> | <span data-ttu-id="a0097-136">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a0097-136">2\_0</span></span> | <span data-ttu-id="a0097-137">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a0097-137">2\_x</span></span> | <span data-ttu-id="a0097-138">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="a0097-138">2\_sw</span></span> | <span data-ttu-id="a0097-139">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a0097-139">3\_0</span></span> | <span data-ttu-id="a0097-140">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="a0097-140">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="a0097-141">SinCos,</span><span class="sxs-lookup"><span data-stu-id="a0097-141">sincos</span></span>                 |      | <span data-ttu-id="a0097-142">x</span><span class="sxs-lookup"><span data-stu-id="a0097-142">x</span></span>    | <span data-ttu-id="a0097-143">x</span><span class="sxs-lookup"><span data-stu-id="a0097-143">x</span></span>    | <span data-ttu-id="a0097-144">x</span><span class="sxs-lookup"><span data-stu-id="a0097-144">x</span></span>     | <span data-ttu-id="a0097-145">x</span><span class="sxs-lookup"><span data-stu-id="a0097-145">x</span></span>    | <span data-ttu-id="a0097-146">x</span><span class="sxs-lookup"><span data-stu-id="a0097-146">x</span></span>     |



 

### <a name="vs_2_0-and-vs_2_x-remarks"></a><span data-ttu-id="a0097-147">Remarques sur vs \_ 2 \_ 0 et vs \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a0097-147">vs\_2\_0 and vs\_2\_x Remarks</span></span>

<span data-ttu-id="a0097-148">Pour vs \_ 2 \_ 0 et vs \_ 2 \_ x, SinCos, peut être utilisé avec un prédicat, mais avec une restriction au Swizzle du registre de [prédicats](dx9-graphics-reference-asm-vs-registers-predicate.md) (P0) : seule la réplication de Swizzle (. x.y. \| \| z \| ) est autorisée.</span><span class="sxs-lookup"><span data-stu-id="a0097-148">For vs\_2\_0 and vs\_2\_x, sincos can be used with predication, but with one restriction to the swizzle of the [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md) (p0): only replicate swizzle (.x \| .y \| .z \| .w) is allowed.</span></span>

<span data-ttu-id="a0097-149">Pour vs \_ 2 \_ 0 et vs \_ 2 \_ x, l’instruction fonctionne comme suit : (V = la valeur scalaire de src0 avec un Swizzle de réplication) :</span><span class="sxs-lookup"><span data-stu-id="a0097-149">For vs\_2\_0 and vs\_2\_x, the instruction operates as follows: (V = the scalar value from src0 with a replicate swizzle):</span></span>

-   <span data-ttu-id="a0097-150">Si le masque d’écriture est. x :</span><span class="sxs-lookup"><span data-stu-id="a0097-150">If the write mask is .x:</span></span>
    ```
    dest.x = cos( V )
    dest.y is undefined when the instruction completes
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="a0097-151">Si le masque d’écriture est. y :</span><span class="sxs-lookup"><span data-stu-id="a0097-151">If the write mask is .y:</span></span>
    ```
    dest.x is undefined when the instruction completes
    dest.y = sin( V )
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="a0097-152">Si le masque d’écriture est. XY :</span><span class="sxs-lookup"><span data-stu-id="a0097-152">If the write mask is .xy:</span></span>
    ```
    dest.x = cos( V )
    dest.y = sin( V )
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

### <a name="vs_3_0-remarks"></a><span data-ttu-id="a0097-153">Remarques sur vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a0097-153">vs\_3\_0 Remarks</span></span>

<span data-ttu-id="a0097-154">Pour vs \_ 3 \_ 0, SinCos, peut être utilisé avec un prédicat sans aucune restriction.</span><span class="sxs-lookup"><span data-stu-id="a0097-154">For vs\_3\_0, sincos can be used with predication without any restriction.</span></span> <span data-ttu-id="a0097-155">Consultez [Registre de prédicat](dx9-graphics-reference-asm-vs-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="a0097-155">See [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md).</span></span>

<span data-ttu-id="a0097-156">Pour vs \_ 3 \_ 0, l’instruction fonctionne comme suit : (V = la valeur scalaire de src0 avec un Swizzle de réplication)</span><span class="sxs-lookup"><span data-stu-id="a0097-156">For vs\_3\_0, the instruction operates as follows: (V = the scalar value from src0 with a replicate swizzle)</span></span>

-   <span data-ttu-id="a0097-157">Si le masque d’écriture est. x :</span><span class="sxs-lookup"><span data-stu-id="a0097-157">If the write mask is .x:</span></span>
    ```
    dest.x = cos( V )
    dest.y is not touched by the instruction
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="a0097-158">Si le masque d’écriture est. y :</span><span class="sxs-lookup"><span data-stu-id="a0097-158">If the write mask is .y:</span></span>
    ```
    dest.x is not touched by the instruction
    dest.y = sin( V )
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="a0097-159">Si le masque d’écriture est. XY :</span><span class="sxs-lookup"><span data-stu-id="a0097-159">If the write mask is .xy:</span></span>
    ```
    dest.x = cos( V )
    dest.y = sin( V )
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

<span data-ttu-id="a0097-160">L’application peut mapper un angle arbitraire (en radians) à la plage \[ -pi, + pi \] en utilisant le pseudocode de nuanceur suivant :</span><span class="sxs-lookup"><span data-stu-id="a0097-160">The application can map an arbitrary angle (in radians) to the range \[-pi, +pi\] using the following shader pseudocode:</span></span>


```
def c0, pi, 0.5, 2*pi, 1/(2*pi)
mad r0.x, input_angle, c0.w, c0.y
frc r0.x, r0.x
mad r0.x, r0.x, c0.z, -c0.x
```



## <a name="related-topics"></a><span data-ttu-id="a0097-161">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a0097-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0097-162">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="a0097-162">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
