---
title: Texture1DArray
description: Texture1DArray
ms.assetid: 3d793423-3d79-48c1-aa78-f9d93b79e0b6
keywords:
- HLSL Texture1DArray
topic_type:
- apiref
api_name:
- Texture1DArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 39cea5692e29ead74ba20c4a35ab8d43a1b19d42
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030348"
---
# <a name="texture1darray"></a><span data-ttu-id="3a67b-104">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="3a67b-104">Texture1DArray</span></span>

<span data-ttu-id="3a67b-105">Type Texture1DArray ([tel qu’il existe dans Shader Model 4](dx-graphics-hlsl-to-type.md)) et variables de ressource.</span><span class="sxs-lookup"><span data-stu-id="3a67b-105">Texture1DArray type ([as it exists in Shader Model 4](dx-graphics-hlsl-to-type.md)) plus resource variables.</span></span> <span data-ttu-id="3a67b-106">Cet objet texture prend en charge les méthodes suivantes en plus des méthodes dans le nuanceur modèle 4.</span><span class="sxs-lookup"><span data-stu-id="3a67b-106">This texture object supports the following methods in addition to the methods in Shader Model 4.</span></span>



| <span data-ttu-id="3a67b-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="3a67b-107">Method</span></span>                                                                       | <span data-ttu-id="3a67b-108">Description</span><span class="sxs-lookup"><span data-stu-id="3a67b-108">Description</span></span>                                                                                |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3a67b-109">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="3a67b-109">**GetDimensions**</span></span>](sm5-object-texture1darray-getdimensions.md)             | <span data-ttu-id="3a67b-110">Obtient les dimensions de ressource.</span><span class="sxs-lookup"><span data-stu-id="3a67b-110">Gets the resource dimensions.</span></span>                                                              |
| [<span data-ttu-id="3a67b-111">**Load**</span><span class="sxs-lookup"><span data-stu-id="3a67b-111">**Load**</span></span>](texture1darray-load.md)                                          | <span data-ttu-id="3a67b-112">Lit les données de texture.</span><span class="sxs-lookup"><span data-stu-id="3a67b-112">Reads texture data.</span></span>                                                                        |
| <span data-ttu-id="3a67b-113">[**mips. And\[\]\[\]**](sm5-object-texture1darray-mipsoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="3a67b-113">[**mips.Operator\[\]\[\]**](sm5-object-texture1darray-mipsoperatorindex.md)</span></span> | <span data-ttu-id="3a67b-114">Obtient une variable de ressource en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3a67b-114">Gets a read-only resource variable.</span></span>                                                        |
| <span data-ttu-id="3a67b-115">[**Opérateur\[\]**](sm5-object-texture1darray-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="3a67b-115">[**Operator\[\]**](sm5-object-texture1darray-operatorindex.md)</span></span>              | <span data-ttu-id="3a67b-116">Obtient une variable de ressource en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3a67b-116">Gets a read-only resource variable.</span></span>                                                        |
| [<span data-ttu-id="3a67b-117">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="3a67b-117">**Sample**</span></span>](texture1darray-sample.md)                                      | <span data-ttu-id="3a67b-118">Échantillonne une texture.</span><span class="sxs-lookup"><span data-stu-id="3a67b-118">Samples a texture.</span></span>                                                                         |
| [<span data-ttu-id="3a67b-119">**SampleBias**</span><span class="sxs-lookup"><span data-stu-id="3a67b-119">**SampleBias**</span></span>](texture1darray-samplebias.md)                              | <span data-ttu-id="3a67b-120">Échantillonne une texture après avoir appliqué la valeur de biais au niveau de mipmap.</span><span class="sxs-lookup"><span data-stu-id="3a67b-120">Samples a texture, after applying the bias value to the mipmap level.</span></span>                      |
| [<span data-ttu-id="3a67b-121">**SampleCmp**</span><span class="sxs-lookup"><span data-stu-id="3a67b-121">**SampleCmp**</span></span>](texture1darray-samplecmp.md)                                | <span data-ttu-id="3a67b-122">Échantillonne une texture en utilisant une valeur de comparaison pour rejeter des exemples.</span><span class="sxs-lookup"><span data-stu-id="3a67b-122">Samples a texture, using a comparison value to reject samples.</span></span>                             |
| [<span data-ttu-id="3a67b-123">**SampleCmpLevelZero**</span><span class="sxs-lookup"><span data-stu-id="3a67b-123">**SampleCmpLevelZero**</span></span>](texture1darray-samplecmplevelzero.md)              | <span data-ttu-id="3a67b-124">Échantillonne une texture (mipmap niveau 0 uniquement), en utilisant une valeur de comparaison pour rejeter les exemples.</span><span class="sxs-lookup"><span data-stu-id="3a67b-124">Samples a texture (mipmap level 0 only), using a comparison value to reject samples.</span></span>       |
| [<span data-ttu-id="3a67b-125">**SampleGrad**</span><span class="sxs-lookup"><span data-stu-id="3a67b-125">**SampleGrad**</span></span>](texture1darray-samplegrad.md)                              | <span data-ttu-id="3a67b-126">Échantillonne une texture à l’aide d’un dégradé pour influencer la façon dont l’emplacement de l’échantillon est calculé.</span><span class="sxs-lookup"><span data-stu-id="3a67b-126">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span> |
| [<span data-ttu-id="3a67b-127">**SampleLevel**</span><span class="sxs-lookup"><span data-stu-id="3a67b-127">**SampleLevel**</span></span>](texture1darray-samplelevel.md)                            | <span data-ttu-id="3a67b-128">Échantillonne une texture au niveau du mipmap spécifié.</span><span class="sxs-lookup"><span data-stu-id="3a67b-128">Samples a texture on the specified mipmap level.</span></span>                                           |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="3a67b-129">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="3a67b-129">Minimum Shader Model</span></span>

<span data-ttu-id="3a67b-130">Cet objet est pris en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="3a67b-130">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="3a67b-131">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="3a67b-131">Shader Model</span></span>                                                                | <span data-ttu-id="3a67b-132">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="3a67b-132">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="3a67b-133">[Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="3a67b-133">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="3a67b-134">Oui</span><span class="sxs-lookup"><span data-stu-id="3a67b-134">yes</span></span>       |



 

<span data-ttu-id="3a67b-135">Cet objet est pris en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="3a67b-135">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="3a67b-136">Sommet</span><span class="sxs-lookup"><span data-stu-id="3a67b-136">Vertex</span></span> | <span data-ttu-id="3a67b-137">Forme</span><span class="sxs-lookup"><span data-stu-id="3a67b-137">Hull</span></span> | <span data-ttu-id="3a67b-138">Domain</span><span class="sxs-lookup"><span data-stu-id="3a67b-138">Domain</span></span> | <span data-ttu-id="3a67b-139">Géométrie</span><span class="sxs-lookup"><span data-stu-id="3a67b-139">Geometry</span></span> | <span data-ttu-id="3a67b-140">Pixel</span><span class="sxs-lookup"><span data-stu-id="3a67b-140">Pixel</span></span> | <span data-ttu-id="3a67b-141">Compute</span><span class="sxs-lookup"><span data-stu-id="3a67b-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="3a67b-142">x</span><span class="sxs-lookup"><span data-stu-id="3a67b-142">x</span></span>      | <span data-ttu-id="3a67b-143">x</span><span class="sxs-lookup"><span data-stu-id="3a67b-143">x</span></span>    | <span data-ttu-id="3a67b-144">x</span><span class="sxs-lookup"><span data-stu-id="3a67b-144">x</span></span>      | <span data-ttu-id="3a67b-145">x</span><span class="sxs-lookup"><span data-stu-id="3a67b-145">x</span></span>        | <span data-ttu-id="3a67b-146">x</span><span class="sxs-lookup"><span data-stu-id="3a67b-146">x</span></span>     | <span data-ttu-id="3a67b-147">x</span><span class="sxs-lookup"><span data-stu-id="3a67b-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="3a67b-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a67b-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a67b-149">Objets Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="3a67b-149">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




