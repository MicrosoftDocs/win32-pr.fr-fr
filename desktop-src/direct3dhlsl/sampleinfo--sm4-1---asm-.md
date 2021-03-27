---
title: sampleinfo (SM 4.1-ASM)
description: Interroge le nombre d’échantillons dans une vue de ressource de nuanceur donnée ou dans le rastériseur.
ms.assetid: 1F0968D7-01E9-4213-9F83-172B88374C3C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d307dbc8c79618a6401737874a9f6e060a899ccc
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103841698"
---
# <a name="sampleinfo-sm41---asm"></a><span data-ttu-id="6a2d5-103">sampleinfo (SM 4.1-ASM)</span><span class="sxs-lookup"><span data-stu-id="6a2d5-103">sampleinfo (sm4.1 - asm)</span></span>

<span data-ttu-id="6a2d5-104">Interroge le nombre d’échantillons dans une vue de ressource de nuanceur donnée ou dans le rastériseur.</span><span class="sxs-lookup"><span data-stu-id="6a2d5-104">Queries the number of samples in a given shader resource view or in the rasterizer.</span></span>



| <span data-ttu-id="6a2d5-105">\[\_uint \] dest \[ . Mask \] , srcResource \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="6a2d5-105">\[\_uint\] dest\[.mask\], srcResource\[.swizzle\]</span></span> |
|---------------------------------------------------|



 



| <span data-ttu-id="6a2d5-106">Élément</span><span class="sxs-lookup"><span data-stu-id="6a2d5-106">Item</span></span>                                                                                                               | <span data-ttu-id="6a2d5-107">Description</span><span class="sxs-lookup"><span data-stu-id="6a2d5-107">Description</span></span>                                                    |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="6a2d5-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="6a2d5-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="6a2d5-109">\[dans \] l’adresse des résultats de l’opération.</span><span class="sxs-lookup"><span data-stu-id="6a2d5-109">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="6a2d5-110"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="6a2d5-110"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="6a2d5-111">\[dans \] la ressource de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="6a2d5-111">\[in\] The shader resource.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="6a2d5-112">Notes</span><span class="sxs-lookup"><span data-stu-id="6a2d5-112">Remarks</span></span>

<span data-ttu-id="6a2d5-113">Cette instruction retourne le nombre d’échantillons pour la ressource donnée ou le rastériseur.</span><span class="sxs-lookup"><span data-stu-id="6a2d5-113">This instruction returns the number of samples for the given resource or the rasterizer.</span></span> <span data-ttu-id="6a2d5-114">Elle est valide uniquement pour les ressources qui peuvent être chargées à l’aide de [**ld2dms**](ld2dms--sm4-1---asm-.md) , sauf si le rastériseur est spécifié en tant que *srcResource*.</span><span class="sxs-lookup"><span data-stu-id="6a2d5-114">It is valid only for resources that can be loaded using [**ld2dms**](ld2dms--sm4-1---asm-.md) unless the rasterizer is specified as *srcResource*.</span></span> <span data-ttu-id="6a2d5-115">*srcResource* peut être un \# Registre t (affichage des ressources du nuanceur) ou un registre de rastérisation.</span><span class="sxs-lookup"><span data-stu-id="6a2d5-115">*srcResource* could be a t\# register (a shader resource view) or a rasterizer register.</span></span>

<span data-ttu-id="6a2d5-116">L’instruction calcule le vecteur (SampleCount, 0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="6a2d5-116">The instruction computes the vector (SampleCount,0,0,0).</span></span>

<span data-ttu-id="6a2d5-117">Swizzle sur *srcResource* permet aux valeurs retournées d’être swizzled arbitrairement avant d’être écrites dans la destination.</span><span class="sxs-lookup"><span data-stu-id="6a2d5-117">The swizzle on *srcResource* allows the returned values to be swizzled arbitrarily before they are written to the destination.</span></span> <span data-ttu-id="6a2d5-118">La valeur retournée est à virgule flottante, à moins que le \_ modificateur uint soit utilisé, auquel cas la valeur retournée est un entier.</span><span class="sxs-lookup"><span data-stu-id="6a2d5-118">The returned value is floating point, unless the \_uint modifier is used, in which case the returned value is integer.</span></span> <span data-ttu-id="6a2d5-119">Si aucune ressource n’est liée à l’emplacement spécifié, la valeur 0 est retournée.</span><span class="sxs-lookup"><span data-stu-id="6a2d5-119">If there is no resource bound to the specified slot, 0 is returned.</span></span>

<span data-ttu-id="6a2d5-120">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="6a2d5-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="6a2d5-121">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="6a2d5-121">Vertex Shader</span></span> | <span data-ttu-id="6a2d5-122">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="6a2d5-122">Geometry Shader</span></span> | <span data-ttu-id="6a2d5-123">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="6a2d5-123">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="6a2d5-124">X</span><span class="sxs-lookup"><span data-stu-id="6a2d5-124">X</span></span>             | <span data-ttu-id="6a2d5-125">X</span><span class="sxs-lookup"><span data-stu-id="6a2d5-125">X</span></span>               | <span data-ttu-id="6a2d5-126">x</span><span class="sxs-lookup"><span data-stu-id="6a2d5-126">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6a2d5-127">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="6a2d5-127">Minimum Shader Model</span></span>

<span data-ttu-id="6a2d5-128">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="6a2d5-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="6a2d5-129">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="6a2d5-129">Shader Model</span></span>                                              | <span data-ttu-id="6a2d5-130">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="6a2d5-130">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6a2d5-131">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="6a2d5-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6a2d5-132">Oui</span><span class="sxs-lookup"><span data-stu-id="6a2d5-132">yes</span></span>       |
| [<span data-ttu-id="6a2d5-133">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="6a2d5-133">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6a2d5-134">Oui</span><span class="sxs-lookup"><span data-stu-id="6a2d5-134">yes</span></span>       |
| [<span data-ttu-id="6a2d5-135">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="6a2d5-135">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6a2d5-136">non</span><span class="sxs-lookup"><span data-stu-id="6a2d5-136">no</span></span>        |
| [<span data-ttu-id="6a2d5-137">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6a2d5-137">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6a2d5-138">non</span><span class="sxs-lookup"><span data-stu-id="6a2d5-138">no</span></span>        |
| [<span data-ttu-id="6a2d5-139">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6a2d5-139">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6a2d5-140">non</span><span class="sxs-lookup"><span data-stu-id="6a2d5-140">no</span></span>        |
| [<span data-ttu-id="6a2d5-141">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6a2d5-141">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6a2d5-142">non</span><span class="sxs-lookup"><span data-stu-id="6a2d5-142">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="6a2d5-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6a2d5-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a2d5-144">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6a2d5-144">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





