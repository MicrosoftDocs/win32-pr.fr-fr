---
title: breakc (SM4-ASM)
description: Déplace de manière conditionnelle le point d’exécution vers l’instruction après le prochain ENDLOOP ou endswitch.
ms.assetid: 5735EF88-1E8C-4142-8442-9328D78999A7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 019a1c859f7d1e0ee6368f5b9984775ef9bfaba1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381185"
---
# <a name="breakc-sm4---asm"></a><span data-ttu-id="ddd69-103">breakc (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="ddd69-103">breakc (sm4 - asm)</span></span>

<span data-ttu-id="ddd69-104">Déplace de manière conditionnelle le point d’exécution vers l’instruction après le prochain [ENDLOOP](endloop--sm4---asm-.md) ou [endswitch](endswitch--sm4---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="ddd69-104">Conditionally moves the point of execution to the instruction after the next [endloop](endloop--sm4---asm-.md) or [endswitch](endswitch--sm4---asm-.md).</span></span>



| <span data-ttu-id="ddd69-105">breakc { \_ z </span><span class="sxs-lookup"><span data-stu-id="ddd69-105">breakc{\_z</span></span>\|<span data-ttu-id="ddd69-106">\_NZ} src0. sélectionner le \_ composant</span><span class="sxs-lookup"><span data-stu-id="ddd69-106">\_nz} src0.select\_component</span></span> |
|------------------------------------------|



 



| <span data-ttu-id="ddd69-107">Élément</span><span class="sxs-lookup"><span data-stu-id="ddd69-107">Item</span></span>                                                            | <span data-ttu-id="ddd69-108">Description</span><span class="sxs-lookup"><span data-stu-id="ddd69-108">Description</span></span>                                                     |
|-----------------------------------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="ddd69-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="ddd69-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="ddd69-110">\[dans \] le composant sur lequel tester la condition.</span><span class="sxs-lookup"><span data-stu-id="ddd69-110">\[in\] The component on which to test the condition.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ddd69-111">Notes</span><span class="sxs-lookup"><span data-stu-id="ddd69-111">Remarks</span></span>

<span data-ttu-id="ddd69-112">Le format de jeton contient le décalage de l’instruction **ENDLOOP** correspondante dans le nuanceur pour des raisons pratiques.</span><span class="sxs-lookup"><span data-stu-id="ddd69-112">The token format contains the offset of the corresponding **endloop** instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="ddd69-113">L’exemple suivant illustre l’instruction **breakc** .</span><span class="sxs-lookup"><span data-stu-id="ddd69-113">The following example shows the **breakc** instruction.</span></span>


```
                loop
                    // example of termination condition
                    breakc_z  r0.x // break if all bits in r0.x are 0
                    breakc_nz r1.x // break if any bit in r1.x is nonzero
                    ...
                endloop

```



<span data-ttu-id="ddd69-114">Cette instruction doit apparaître dans une **boucle** / **ENDLOOP** ou **switch** / **endswitch**.</span><span class="sxs-lookup"><span data-stu-id="ddd69-114">This instruction must appear within a **loop**/**endloop** or **switch**/**endswitch**.</span></span>

<span data-ttu-id="ddd69-115">Le registre 32 bits fourni par *src0* est testé à un niveau binaire.</span><span class="sxs-lookup"><span data-stu-id="ddd69-115">The 32-bit register supplied by *src0* is tested at a bit level.</span></span> <span data-ttu-id="ddd69-116">Si un bit est différent de zéro, **breakc \_ NZ** effectuera l’arrêt.</span><span class="sxs-lookup"><span data-stu-id="ddd69-116">If any bit is nonzero, **breakc\_nz** will perform the break.</span></span> <span data-ttu-id="ddd69-117">Si tous les bits sont nuls, **breakc \_ z** effectue l’arrêt.</span><span class="sxs-lookup"><span data-stu-id="ddd69-117">If all bits are zero, **breakc\_z** will perform the break.</span></span>

<span data-ttu-id="ddd69-118">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="ddd69-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ddd69-119">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="ddd69-119">Vertex Shader</span></span> | <span data-ttu-id="ddd69-120">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="ddd69-120">Geometry Shader</span></span> | <span data-ttu-id="ddd69-121">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="ddd69-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="ddd69-122">x</span><span class="sxs-lookup"><span data-stu-id="ddd69-122">x</span></span>             | <span data-ttu-id="ddd69-123">x</span><span class="sxs-lookup"><span data-stu-id="ddd69-123">x</span></span>               | <span data-ttu-id="ddd69-124">x</span><span class="sxs-lookup"><span data-stu-id="ddd69-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ddd69-125">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="ddd69-125">Minimum Shader Model</span></span>

<span data-ttu-id="ddd69-126">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="ddd69-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ddd69-127">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="ddd69-127">Shader Model</span></span>                                              | <span data-ttu-id="ddd69-128">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="ddd69-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ddd69-129">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="ddd69-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ddd69-130">Oui</span><span class="sxs-lookup"><span data-stu-id="ddd69-130">yes</span></span>       |
| [<span data-ttu-id="ddd69-131">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="ddd69-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ddd69-132">Oui</span><span class="sxs-lookup"><span data-stu-id="ddd69-132">yes</span></span>       |
| [<span data-ttu-id="ddd69-133">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="ddd69-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ddd69-134">Oui</span><span class="sxs-lookup"><span data-stu-id="ddd69-134">yes</span></span>       |
| [<span data-ttu-id="ddd69-135">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ddd69-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ddd69-136">non</span><span class="sxs-lookup"><span data-stu-id="ddd69-136">no</span></span>        |
| [<span data-ttu-id="ddd69-137">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ddd69-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ddd69-138">non</span><span class="sxs-lookup"><span data-stu-id="ddd69-138">no</span></span>        |
| [<span data-ttu-id="ddd69-139">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ddd69-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ddd69-140">non</span><span class="sxs-lookup"><span data-stu-id="ddd69-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ddd69-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ddd69-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ddd69-142">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ddd69-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





