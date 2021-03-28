---
title: samplepos (SM 4.1-ASM)
description: Interroge la position d’un exemple dans une vue de ressource de nuanceur donnée ou dans le rastériseur.
ms.assetid: 5A53B342-3A1D-4016-ABF2-CA6236D562C9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 910a542dafddb8b855e218f8702c746220780d6e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381218"
---
# <a name="samplepos-sm41---asm"></a><span data-ttu-id="9e129-103">samplepos (SM 4.1-ASM)</span><span class="sxs-lookup"><span data-stu-id="9e129-103">samplepos (sm4.1 - asm)</span></span>

<span data-ttu-id="9e129-104">Interroge la position d’un exemple dans une vue de ressource de nuanceur donnée ou dans le rastériseur.</span><span class="sxs-lookup"><span data-stu-id="9e129-104">Queries the position of a sample in a given shader resource view or in the rasterizer.</span></span>



| <span data-ttu-id="9e129-105">samplepos dest \[ . Mask \] , srcResource \[ . Swizzle \] , sampleIndex (opérande scalaire)</span><span class="sxs-lookup"><span data-stu-id="9e129-105">samplepos dest\[.mask\], srcResource\[.swizzle\], sampleIndex (scalar operand)</span></span> |
|--------------------------------------------------------------------------------|



 



| <span data-ttu-id="9e129-106">Élément</span><span class="sxs-lookup"><span data-stu-id="9e129-106">Item</span></span>                                                                                                               | <span data-ttu-id="9e129-107">Description</span><span class="sxs-lookup"><span data-stu-id="9e129-107">Description</span></span>                                                    |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="9e129-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="9e129-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="9e129-109">\[dans \] l’adresse des résultats de l’opération.</span><span class="sxs-lookup"><span data-stu-id="9e129-109">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="9e129-110"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="9e129-110"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="9e129-111">\[dans \] la ressource de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="9e129-111">\[in\] The shader resource.</span></span><br/>                         |
| <span data-ttu-id="9e129-112"><span id="sampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*sampleIndex*</span><span class="sxs-lookup"><span data-stu-id="9e129-112"><span id="sampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*sampleIndex*</span></span><br/> | <span data-ttu-id="9e129-113">\[dans \] l’index de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="9e129-113">\[in\] The index of the sample.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="9e129-114">Notes</span><span class="sxs-lookup"><span data-stu-id="9e129-114">Remarks</span></span>

<span data-ttu-id="9e129-115">Cette instruction retourne la position d’échantillon 2D de l’exemple de *sampleIndex* pour la ressource donnée.</span><span class="sxs-lookup"><span data-stu-id="9e129-115">This instruction returns the 2D sample position of sample *sampleIndex* for the given resource.</span></span> <span data-ttu-id="9e129-116">Elle est valide uniquement pour les ressources qui peuvent être chargées à l’aide de [**ld2dms**](ld2dms--sm4-1---asm-.md) , sauf si le rastériseur est spécifié en tant que *srcResource*.</span><span class="sxs-lookup"><span data-stu-id="9e129-116">It is valid only for resources that can be loaded using [**ld2dms**](ld2dms--sm4-1---asm-.md) unless the rasterizer is specified as *srcResource*.</span></span>

<span data-ttu-id="9e129-117">*srcResource* peut être un \# Registre t (affichage des ressources de nuanceur) ou un registre de rastérisation.</span><span class="sxs-lookup"><span data-stu-id="9e129-117">*srcResource* can be a t\# register (a shader resource view) or a rasterizer register.</span></span>

<span data-ttu-id="9e129-118">L’instruction calcule le vecteur à virgule flottante (XPosition, YPosition, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="9e129-118">The instruction computes the floating point vector (Xposition, Yposition, 0, 0).</span></span>

<span data-ttu-id="9e129-119">Swizzle sur *srcResource* permet aux valeurs retournées d’être swizzled arbitrairement avant d’être écrites dans la destination.</span><span class="sxs-lookup"><span data-stu-id="9e129-119">The swizzle on *srcResource* allows the returned values to be swizzled arbitrarily before they are written to the destination.</span></span> <span data-ttu-id="9e129-120">La position de l’échantillon est relative au centre du pixel, en fonction du système de coordonnées en pixels.</span><span class="sxs-lookup"><span data-stu-id="9e129-120">The sample position is relative to the pixel's center, based on the Pixel Coordinate System.</span></span>

<span data-ttu-id="9e129-121">Si *sampleIndex* est hors limites, un vecteur zéro est retourné.</span><span class="sxs-lookup"><span data-stu-id="9e129-121">If *sampleIndex* is out of bounds a zero vector is returned.</span></span> <span data-ttu-id="9e129-122">Si aucune ressource n’est liée à l’emplacement spécifié, la valeur 0 est retournée.</span><span class="sxs-lookup"><span data-stu-id="9e129-122">If there is no resource bound to the specified slot, 0 is returned.</span></span>

<span data-ttu-id="9e129-123">**samplepos** peut être utilisé pour des tâches telles que des résolutions personnalisées dans le code du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="9e129-123">**samplepos** can be used for things like custom resolves in shader code.</span></span>

<span data-ttu-id="9e129-124">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="9e129-124">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9e129-125">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="9e129-125">Vertex Shader</span></span> | <span data-ttu-id="9e129-126">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="9e129-126">Geometry Shader</span></span> | <span data-ttu-id="9e129-127">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="9e129-127">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="9e129-128">x</span><span class="sxs-lookup"><span data-stu-id="9e129-128">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9e129-129">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="9e129-129">Minimum Shader Model</span></span>

<span data-ttu-id="9e129-130">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="9e129-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9e129-131">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="9e129-131">Shader Model</span></span>                                              | <span data-ttu-id="9e129-132">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="9e129-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9e129-133">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="9e129-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9e129-134">Oui</span><span class="sxs-lookup"><span data-stu-id="9e129-134">yes</span></span>       |
| [<span data-ttu-id="9e129-135">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="9e129-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9e129-136">Oui</span><span class="sxs-lookup"><span data-stu-id="9e129-136">yes</span></span>       |
| [<span data-ttu-id="9e129-137">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="9e129-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9e129-138">non</span><span class="sxs-lookup"><span data-stu-id="9e129-138">no</span></span>        |
| [<span data-ttu-id="9e129-139">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9e129-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9e129-140">non</span><span class="sxs-lookup"><span data-stu-id="9e129-140">no</span></span>        |
| [<span data-ttu-id="9e129-141">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9e129-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9e129-142">non</span><span class="sxs-lookup"><span data-stu-id="9e129-142">no</span></span>        |
| [<span data-ttu-id="9e129-143">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9e129-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9e129-144">non</span><span class="sxs-lookup"><span data-stu-id="9e129-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9e129-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9e129-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e129-146">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9e129-146">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





