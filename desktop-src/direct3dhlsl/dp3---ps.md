---
title: DP3-PS
description: Calcule le produit scalaire à trois composants des registres sources. | DP3-PS
ms.assetid: a365acd1-89c0-4340-8f51-8e478f84ddc0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 09e4178f6aedbfb5242f4c545d624f1d07796008
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974075"
---
# <a name="dp3---ps"></a><span data-ttu-id="bbcc6-104">DP3-PS</span><span class="sxs-lookup"><span data-stu-id="bbcc6-104">dp3 - ps</span></span>

<span data-ttu-id="bbcc6-105">Calcule le produit scalaire à trois composants des registres sources.</span><span class="sxs-lookup"><span data-stu-id="bbcc6-105">Computes the three-component dot product of the source registers.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbcc6-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bbcc6-106">Syntax</span></span>



| <span data-ttu-id="bbcc6-107">DP3 DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="bbcc6-107">dp3 dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="bbcc6-108">where</span><span class="sxs-lookup"><span data-stu-id="bbcc6-108">where</span></span>

-   <span data-ttu-id="bbcc6-109">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="bbcc6-109">dst is the destination register.</span></span>
-   <span data-ttu-id="bbcc6-110">src0 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="bbcc6-110">src0 is a source register.</span></span>
-   <span data-ttu-id="bbcc6-111">src1 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="bbcc6-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbcc6-112">Notes</span><span class="sxs-lookup"><span data-stu-id="bbcc6-112">Remarks</span></span>



| <span data-ttu-id="bbcc6-113">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="bbcc6-113">Pixel shader versions</span></span> | <span data-ttu-id="bbcc6-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="bbcc6-114">1\_1</span></span> | <span data-ttu-id="bbcc6-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="bbcc6-115">1\_2</span></span> | <span data-ttu-id="bbcc6-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="bbcc6-116">1\_3</span></span> | <span data-ttu-id="bbcc6-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="bbcc6-117">1\_4</span></span> | <span data-ttu-id="bbcc6-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bbcc6-118">2\_0</span></span> | <span data-ttu-id="bbcc6-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="bbcc6-119">2\_x</span></span> | <span data-ttu-id="bbcc6-120">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="bbcc6-120">2\_sw</span></span> | <span data-ttu-id="bbcc6-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bbcc6-121">3\_0</span></span> | <span data-ttu-id="bbcc6-122">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="bbcc6-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="bbcc6-123">dp3</span><span class="sxs-lookup"><span data-stu-id="bbcc6-123">dp3</span></span>                   | <span data-ttu-id="bbcc6-124">x</span><span class="sxs-lookup"><span data-stu-id="bbcc6-124">x</span></span>    | <span data-ttu-id="bbcc6-125">x</span><span class="sxs-lookup"><span data-stu-id="bbcc6-125">x</span></span>    | <span data-ttu-id="bbcc6-126">x</span><span class="sxs-lookup"><span data-stu-id="bbcc6-126">x</span></span>    | <span data-ttu-id="bbcc6-127">x</span><span class="sxs-lookup"><span data-stu-id="bbcc6-127">x</span></span>    | <span data-ttu-id="bbcc6-128">x</span><span class="sxs-lookup"><span data-stu-id="bbcc6-128">x</span></span>    | <span data-ttu-id="bbcc6-129">x</span><span class="sxs-lookup"><span data-stu-id="bbcc6-129">x</span></span>    | <span data-ttu-id="bbcc6-130">x</span><span class="sxs-lookup"><span data-stu-id="bbcc6-130">x</span></span>     | <span data-ttu-id="bbcc6-131">x</span><span class="sxs-lookup"><span data-stu-id="bbcc6-131">x</span></span>    | <span data-ttu-id="bbcc6-132">x</span><span class="sxs-lookup"><span data-stu-id="bbcc6-132">x</span></span>     |



 

<span data-ttu-id="bbcc6-133">L’extrait de code suivant montre les opérations effectuées :</span><span class="sxs-lookup"><span data-stu-id="bbcc6-133">The following code snippet shows the operations performed:</span></span>


```
dest.x = dest.y = dest.z = dest.w = 
  (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
```



<span data-ttu-id="bbcc6-134">Cette instruction s’exécute dans le pipeline vectoriel, en écrivant toujours sur les canaux de couleurs.</span><span class="sxs-lookup"><span data-stu-id="bbcc6-134">This instruction runs in the vector pipeline, always writing out to the color channels.</span></span> <span data-ttu-id="bbcc6-135">Pour la version 1 \_ 4, cette instruction utilise toujours le pipeline vectoriel, mais peut écrire dans n’importe quel canal.</span><span class="sxs-lookup"><span data-stu-id="bbcc6-135">For version 1\_4, this instruction still uses the vector pipeline but may write to any channel.</span></span>

<span data-ttu-id="bbcc6-136">Une instruction avec un masque d’écriture de destination. RGB (. xyz) peut être co-émise avec DP3, comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="bbcc6-136">An instruction with a destination register .rgb (.xyz) write mask may be co-issued with dp3 As shown below.</span></span>


```
dp3 r0.rgb, t0, v0            // Copy scalar result to color components
+mov r2.a, t0                 // Copy alpha component from t0 in parallel 
```



<span data-ttu-id="bbcc6-137">L’instruction dp3 peut être modifiée à l’aide du modificateur d’argument d’entrée de [mise à l’échelle signée du Registre source](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) ( \_ BX2) appliqué à ses arguments d’entrée s’ils ne sont pas déjà développés dans une plage dynamique signée.</span><span class="sxs-lookup"><span data-stu-id="bbcc6-137">The dp3 instruction can be modified using the [Source Register Signed Scaling](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) input argument modifier (\_bx2) applied to its input arguments if they are not already expanded to signed dynamic range.</span></span> <span data-ttu-id="bbcc6-138">Dans le cas d’un nuanceur d’éclairage, le modificateur d’instruction saturé ( \_ SAT) est souvent utilisé pour fixer les valeurs négatives au noir, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="bbcc6-138">For a lighting shader, the saturate instruction modifier (\_sat) is often used to clamp the negative values to black, as shown in the following example.</span></span>


```
dp3_sat r0, t0_bx2, v0_bx2    // t0 is a bump map, v0 contains the light direction
```



## <a name="related-topics"></a><span data-ttu-id="bbcc6-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bbcc6-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbcc6-140">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="bbcc6-140">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




