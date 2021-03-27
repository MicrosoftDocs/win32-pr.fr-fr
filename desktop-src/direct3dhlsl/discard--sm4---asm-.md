---
title: ignorer (SM4-ASM)
description: Marquez de manière conditionnelle les résultats du nuanceur de pixels à ignorer lorsque la fin du programme est atteinte.
ms.assetid: 566C4A9A-B32A-4AA6-A888-70F6965B1B5A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57d98365ae6d80710f15cf7204f98d810be30a13
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103940563"
---
# <a name="discard-sm4---asm"></a><span data-ttu-id="6e6c3-103">ignorer (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="6e6c3-103">discard (sm4 - asm)</span></span>

<span data-ttu-id="6e6c3-104">Marquez de manière conditionnelle les résultats du nuanceur de pixels à ignorer lorsque la fin du programme est atteinte.</span><span class="sxs-lookup"><span data-stu-id="6e6c3-104">Conditionally flag results of Pixel Shader to be discarded when the end of the program is reached.</span></span>



| <span data-ttu-id="6e6c3-105">ignorer { \_ z </span><span class="sxs-lookup"><span data-stu-id="6e6c3-105">discard{\_z</span></span>\|<span data-ttu-id="6e6c3-106">\_NZ} src0. sélectionner le \_ composant</span><span class="sxs-lookup"><span data-stu-id="6e6c3-106">\_nz} src0.select\_component</span></span> |
|-------------------------------------------|



 



| <span data-ttu-id="6e6c3-107">Élément</span><span class="sxs-lookup"><span data-stu-id="6e6c3-107">Item</span></span>                                                            | <span data-ttu-id="6e6c3-108">Description</span><span class="sxs-lookup"><span data-stu-id="6e6c3-108">Description</span></span>                                                                                       |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e6c3-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="6e6c3-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="6e6c3-110">\[\]valeur qui détermine s’il faut ignorer le pixel actuel en cours de traitement.</span><span class="sxs-lookup"><span data-stu-id="6e6c3-110">\[in\] The value that determines whether to discard the current pixel being processed.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6e6c3-111">Notes</span><span class="sxs-lookup"><span data-stu-id="6e6c3-111">Remarks</span></span>

<span data-ttu-id="6e6c3-112">Cette instruction marque le pixel actuel comme terminé, tout en continuant son exécution, afin que les autres pixels s’exécutant en parallèle peuvent obtenir des dérivées si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="6e6c3-112">This instruction flags the current pixel as terminated, while continuing execution, so that other pixels executing in parallel may obtain derivatives if necessary.</span></span> <span data-ttu-id="6e6c3-113">Même si l’exécution se poursuit, toute la sortie du nuanceur de pixels écrit avant ou après l’instruction **ignorée** .</span><span class="sxs-lookup"><span data-stu-id="6e6c3-113">Even though execution continues, all Pixel Shader output writes before or after the **discard** instruction are discarded.</span></span>

<span data-ttu-id="6e6c3-114">Pour **Ignorer \_ z**, si tous les bits dans *src0. Select \_ Component* sont nuls, le pixel est ignoré.</span><span class="sxs-lookup"><span data-stu-id="6e6c3-114">For **discard\_z**, if all bits in *src0.select\_component* are zero, then the pixel is discarded.</span></span>

<span data-ttu-id="6e6c3-115">Pour **ignorer la \_ NZ**, si des bits dans *src0. Select \_ Component* sont différent de zéro, le pixel est ignoré.</span><span class="sxs-lookup"><span data-stu-id="6e6c3-115">For **discard\_nz**, if any bits in *src0.select\_component* are nonzero, then the pixel is discarded.</span></span>

<span data-ttu-id="6e6c3-116">En outre, l’instruction **Discard** peut être présente à l’intérieur d’une construction de contrôle de Flow.</span><span class="sxs-lookup"><span data-stu-id="6e6c3-116">In addition, the **discard** instruction can be present inside any flow control construct.</span></span>

<span data-ttu-id="6e6c3-117">Plusieurs instructions **ignorées** peuvent être présentes dans un nuanceur et, si un est exécuté, le pixel est arrêté.</span><span class="sxs-lookup"><span data-stu-id="6e6c3-117">Multiple **discard** instructions may be present in a Shader, and if any is executed, the pixel is terminated.</span></span>

<span data-ttu-id="6e6c3-118">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="6e6c3-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="6e6c3-119">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="6e6c3-119">Vertex Shader</span></span> | <span data-ttu-id="6e6c3-120">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="6e6c3-120">Geometry Shader</span></span> | <span data-ttu-id="6e6c3-121">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="6e6c3-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="6e6c3-122">x</span><span class="sxs-lookup"><span data-stu-id="6e6c3-122">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6e6c3-123">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="6e6c3-123">Minimum Shader Model</span></span>

<span data-ttu-id="6e6c3-124">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="6e6c3-124">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="6e6c3-125">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="6e6c3-125">Shader Model</span></span>                                              | <span data-ttu-id="6e6c3-126">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="6e6c3-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6e6c3-127">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="6e6c3-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6e6c3-128">Oui</span><span class="sxs-lookup"><span data-stu-id="6e6c3-128">yes</span></span>       |
| [<span data-ttu-id="6e6c3-129">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="6e6c3-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6e6c3-130">Oui</span><span class="sxs-lookup"><span data-stu-id="6e6c3-130">yes</span></span>       |
| [<span data-ttu-id="6e6c3-131">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="6e6c3-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6e6c3-132">Oui</span><span class="sxs-lookup"><span data-stu-id="6e6c3-132">yes</span></span>       |
| [<span data-ttu-id="6e6c3-133">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6e6c3-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6e6c3-134">non</span><span class="sxs-lookup"><span data-stu-id="6e6c3-134">no</span></span>        |
| [<span data-ttu-id="6e6c3-135">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6e6c3-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6e6c3-136">non</span><span class="sxs-lookup"><span data-stu-id="6e6c3-136">no</span></span>        |
| [<span data-ttu-id="6e6c3-137">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6e6c3-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6e6c3-138">non</span><span class="sxs-lookup"><span data-stu-id="6e6c3-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="6e6c3-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6e6c3-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e6c3-140">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6e6c3-140">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





