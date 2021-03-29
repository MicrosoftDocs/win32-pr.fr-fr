---
title: continuec (SM4-ASM)
description: Continue l’exécution de manière conditionnelle au début de la boucle en cours.
ms.assetid: 1A5B1951-CE1E-479C-AE0F-FC5FB93E0DE9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d480d8828f8f68af1f6a2ff4f52224041d5241df
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104971555"
---
# <a name="continuec-sm4---asm"></a><span data-ttu-id="1d491-103">continuec (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="1d491-103">continuec (sm4 - asm)</span></span>

<span data-ttu-id="1d491-104">Continue l’exécution de manière conditionnelle au début de la boucle en cours.</span><span class="sxs-lookup"><span data-stu-id="1d491-104">Conditionally continues execution at the beginning of the current loop.</span></span>



| <span data-ttu-id="1d491-105">continuec { \_ z </span><span class="sxs-lookup"><span data-stu-id="1d491-105">continuec{\_z</span></span>\|<span data-ttu-id="1d491-106">\_NZ} src0. sélectionner le \_ composant</span><span class="sxs-lookup"><span data-stu-id="1d491-106">\_nz} src0.select\_component</span></span> |
|---------------------------------------------|



 



| <span data-ttu-id="1d491-107">Terme</span><span class="sxs-lookup"><span data-stu-id="1d491-107">Term</span></span>                                                            | <span data-ttu-id="1d491-108">Description</span><span class="sxs-lookup"><span data-stu-id="1d491-108">Description</span></span>                                                          |
|-----------------------------------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="1d491-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="1d491-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="1d491-110">\[dans \] le composant sur lequel tester la condition.</span><span class="sxs-lookup"><span data-stu-id="1d491-110">\[in\] The component against which to test the condition.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1d491-111">Notes</span><span class="sxs-lookup"><span data-stu-id="1d491-111">Remarks</span></span>

<span data-ttu-id="1d491-112">**continuec** peut être utilisé uniquement à l’intérieur d’une [boucle](loop--sm4---asm-.md) ou d’un [ENDLOOP](endloop--sm4---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="1d491-112">**continuec** can be used only inside a [loop](loop--sm4---asm-.md) or [endloop](endloop--sm4---asm-.md).</span></span>

<span data-ttu-id="1d491-113">L’exemple suivant montre comment utiliser l’instruction **continuec** .</span><span class="sxs-lookup"><span data-stu-id="1d491-113">The following example shows how to use the **continuec** instruction.</span></span>


```
                loop
                    if_na r0.x
                        break
                    endif
                    continuec_z r1.x  // if all bits of r1.x are zero then
                                      // continue at beginning of loop.
                    ...
                    continuec_nz r3.y // if any bit in r3.y is set then
                                      // continue at beginning of loop.

                    ...
                endloop

```



<span data-ttu-id="1d491-114">Le format de jeton contient le décalage de l’instruction de boucle correspondante dans le nuanceur pour des raisons pratiques.</span><span class="sxs-lookup"><span data-stu-id="1d491-114">The token format contains the offset of the corresponding loop instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="1d491-115">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="1d491-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="1d491-116">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="1d491-116">Vertex Shader</span></span> | <span data-ttu-id="1d491-117">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="1d491-117">Geometry Shader</span></span> | <span data-ttu-id="1d491-118">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="1d491-118">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="1d491-119">x</span><span class="sxs-lookup"><span data-stu-id="1d491-119">x</span></span>             | <span data-ttu-id="1d491-120">x</span><span class="sxs-lookup"><span data-stu-id="1d491-120">x</span></span>               | <span data-ttu-id="1d491-121">x</span><span class="sxs-lookup"><span data-stu-id="1d491-121">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1d491-122">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="1d491-122">Minimum Shader Model</span></span>

<span data-ttu-id="1d491-123">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="1d491-123">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="1d491-124">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="1d491-124">Shader Model</span></span>                                              | <span data-ttu-id="1d491-125">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="1d491-125">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="1d491-126">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="1d491-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="1d491-127">Oui</span><span class="sxs-lookup"><span data-stu-id="1d491-127">yes</span></span>       |
| [<span data-ttu-id="1d491-128">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="1d491-128">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="1d491-129">Oui</span><span class="sxs-lookup"><span data-stu-id="1d491-129">yes</span></span>       |
| [<span data-ttu-id="1d491-130">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="1d491-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="1d491-131">Oui</span><span class="sxs-lookup"><span data-stu-id="1d491-131">yes</span></span>       |
| [<span data-ttu-id="1d491-132">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1d491-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1d491-133">non</span><span class="sxs-lookup"><span data-stu-id="1d491-133">no</span></span>        |
| [<span data-ttu-id="1d491-134">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1d491-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="1d491-135">non</span><span class="sxs-lookup"><span data-stu-id="1d491-135">no</span></span>        |
| [<span data-ttu-id="1d491-136">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1d491-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="1d491-137">non</span><span class="sxs-lookup"><span data-stu-id="1d491-137">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1d491-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1d491-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d491-139">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1d491-139">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





