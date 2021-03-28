---
title: Texture3D
description: Texture3D
ms.assetid: a3640aac-b503-4716-8bc6-105e96bea03c
keywords:
- HLSL Texture3D
topic_type:
- apiref
api_name:
- Texture3D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50b12f2184f6eca0fd7a68feb3e96d8d6fc65a61
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030118"
---
# <a name="texture3d"></a><span data-ttu-id="0604c-104">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0604c-104">Texture3D</span></span>

<span data-ttu-id="0604c-105">Type Texture3D ([tel qu’il existe dans Shader Model 4](dx-graphics-hlsl-to-type.md)) et variables de ressource.</span><span class="sxs-lookup"><span data-stu-id="0604c-105">Texture3D type ([as it exists in Shader Model 4](dx-graphics-hlsl-to-type.md)) plus resource variables.</span></span> <span data-ttu-id="0604c-106">Cet objet texture prend en charge les méthodes suivantes en plus des méthodes dans le nuanceur modèle 4.</span><span class="sxs-lookup"><span data-stu-id="0604c-106">This texture object supports the following methods in addition to the methods in Shader Model 4.</span></span>



| <span data-ttu-id="0604c-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="0604c-107">Method</span></span>                                                                  | <span data-ttu-id="0604c-108">Description</span><span class="sxs-lookup"><span data-stu-id="0604c-108">Description</span></span>                                                                                |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0604c-109">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="0604c-109">**GetDimensions**</span></span>](sm5-object-texture3d-getdimensions.md)             | <span data-ttu-id="0604c-110">Obtient les dimensions de ressource.</span><span class="sxs-lookup"><span data-stu-id="0604c-110">Gets the resource dimensions.</span></span>                                                              |
| [<span data-ttu-id="0604c-111">**Load**</span><span class="sxs-lookup"><span data-stu-id="0604c-111">**Load**</span></span>](texture3d-load.md)                                          | <span data-ttu-id="0604c-112">Lit les données de texture.</span><span class="sxs-lookup"><span data-stu-id="0604c-112">Reads texture data.</span></span>                                                                        |
| <span data-ttu-id="0604c-113">[**mips. And\[\]\[\]**](sm5-object-texture3d-mipsoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="0604c-113">[**mips.Operator\[\]\[\]**](sm5-object-texture3d-mipsoperatorindex.md)</span></span> | <span data-ttu-id="0604c-114">Obtient une variable de ressource en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="0604c-114">Gets a read-only resource variable.</span></span>                                                        |
| <span data-ttu-id="0604c-115">[**Opérateur\[\]**](sm5-object-texture3d-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="0604c-115">[**Operator\[\]**](sm5-object-texture3d-operatorindex.md)</span></span>              | <span data-ttu-id="0604c-116">Obtient une variable de ressource en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="0604c-116">Gets a read-only resource variable.</span></span>                                                        |
| [<span data-ttu-id="0604c-117">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="0604c-117">**Sample**</span></span>](texture3d-sample.md)                                      | <span data-ttu-id="0604c-118">Échantillonne une texture.</span><span class="sxs-lookup"><span data-stu-id="0604c-118">Samples a texture.</span></span>                                                                         |
| [<span data-ttu-id="0604c-119">**SampleBias**</span><span class="sxs-lookup"><span data-stu-id="0604c-119">**SampleBias**</span></span>](texture3d-samplebias.md)                              | <span data-ttu-id="0604c-120">Échantillonne une texture après avoir appliqué la valeur de biais au niveau de mipmap.</span><span class="sxs-lookup"><span data-stu-id="0604c-120">Samples a texture, after applying the bias value to the mipmap level.</span></span>                      |
| [<span data-ttu-id="0604c-121">**SampleGrad**</span><span class="sxs-lookup"><span data-stu-id="0604c-121">**SampleGrad**</span></span>](texture3d-samplegrad.md)                              | <span data-ttu-id="0604c-122">Échantillonne une texture à l’aide d’un dégradé pour influencer la façon dont l’emplacement de l’échantillon est calculé.</span><span class="sxs-lookup"><span data-stu-id="0604c-122">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span> |
| [<span data-ttu-id="0604c-123">**SampleLevel**</span><span class="sxs-lookup"><span data-stu-id="0604c-123">**SampleLevel**</span></span>](texture3d-samplelevel.md)                            | <span data-ttu-id="0604c-124">Échantillonne une texture au niveau du mipmap spécifié.</span><span class="sxs-lookup"><span data-stu-id="0604c-124">Samples a texture on the specified mipmap level.</span></span>                                           |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0604c-125">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="0604c-125">Minimum Shader Model</span></span>

<span data-ttu-id="0604c-126">Cet objet est pris en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="0604c-126">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="0604c-127">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="0604c-127">Shader Model</span></span>                                                                | <span data-ttu-id="0604c-128">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="0604c-128">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="0604c-129">[Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="0604c-129">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="0604c-130">Oui</span><span class="sxs-lookup"><span data-stu-id="0604c-130">yes</span></span>       |



 

<span data-ttu-id="0604c-131">Cet objet est pris en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="0604c-131">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="0604c-132">Sommet</span><span class="sxs-lookup"><span data-stu-id="0604c-132">Vertex</span></span> | <span data-ttu-id="0604c-133">Forme</span><span class="sxs-lookup"><span data-stu-id="0604c-133">Hull</span></span> | <span data-ttu-id="0604c-134">Domain</span><span class="sxs-lookup"><span data-stu-id="0604c-134">Domain</span></span> | <span data-ttu-id="0604c-135">Géométrie</span><span class="sxs-lookup"><span data-stu-id="0604c-135">Geometry</span></span> | <span data-ttu-id="0604c-136">Pixel</span><span class="sxs-lookup"><span data-stu-id="0604c-136">Pixel</span></span> | <span data-ttu-id="0604c-137">Compute</span><span class="sxs-lookup"><span data-stu-id="0604c-137">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="0604c-138">x</span><span class="sxs-lookup"><span data-stu-id="0604c-138">x</span></span>      | <span data-ttu-id="0604c-139">x</span><span class="sxs-lookup"><span data-stu-id="0604c-139">x</span></span>    | <span data-ttu-id="0604c-140">x</span><span class="sxs-lookup"><span data-stu-id="0604c-140">x</span></span>      | <span data-ttu-id="0604c-141">x</span><span class="sxs-lookup"><span data-stu-id="0604c-141">x</span></span>        | <span data-ttu-id="0604c-142">x</span><span class="sxs-lookup"><span data-stu-id="0604c-142">x</span></span>     | <span data-ttu-id="0604c-143">x</span><span class="sxs-lookup"><span data-stu-id="0604c-143">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="0604c-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0604c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0604c-145">Objets Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="0604c-145">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




