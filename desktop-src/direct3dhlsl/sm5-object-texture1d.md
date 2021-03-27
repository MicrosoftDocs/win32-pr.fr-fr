---
title: Texture1D
description: Texture1D
ms.assetid: 5f6fd0e4-a73e-4d13-b3a0-c884b7912581
keywords:
- HLSL Texture1D
topic_type:
- apiref
api_name:
- Texture1D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8b8a60706ea2752109cdda9907ffe7c654efe531
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103940493"
---
# <a name="texture1d"></a><span data-ttu-id="28017-104">Texture1D</span><span class="sxs-lookup"><span data-stu-id="28017-104">Texture1D</span></span>

<span data-ttu-id="28017-105">Un type de texture 1D ([tel qu’il existe dans le nuanceur modèle 4](dx-graphics-hlsl-to-type.md)) et des variables de ressource.</span><span class="sxs-lookup"><span data-stu-id="28017-105">A 1D texture type ([as it exists in Shader Model 4](dx-graphics-hlsl-to-type.md)) plus resource variables.</span></span> <span data-ttu-id="28017-106">Cet objet texture prend en charge les méthodes suivantes en plus des méthodes dans le nuanceur modèle 4.</span><span class="sxs-lookup"><span data-stu-id="28017-106">This texture object supports the following methods in addition to the methods in Shader Model 4.</span></span>



| <span data-ttu-id="28017-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="28017-107">Method</span></span>                                                                  | <span data-ttu-id="28017-108">Description</span><span class="sxs-lookup"><span data-stu-id="28017-108">Description</span></span>                                                                                |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="28017-109">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="28017-109">**GetDimensions**</span></span>](sm5-object-texture1d-getdimensions.md)             | <span data-ttu-id="28017-110">Obtient les dimensions de ressource.</span><span class="sxs-lookup"><span data-stu-id="28017-110">Gets the resource dimensions.</span></span>                                                              |
| [<span data-ttu-id="28017-111">**Load**</span><span class="sxs-lookup"><span data-stu-id="28017-111">**Load**</span></span>](texture1d-load.md)                                          | <span data-ttu-id="28017-112">Lit les données de texture.</span><span class="sxs-lookup"><span data-stu-id="28017-112">Reads texture data.</span></span>                                                                        |
| <span data-ttu-id="28017-113">[**Opérateur\[\]**](sm5-object-texture1d-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="28017-113">[**Operator\[\]**](sm5-object-texture1d-operatorindex.md)</span></span>              | <span data-ttu-id="28017-114">Obtient une variable de ressource en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="28017-114">Gets a read-only resource variable.</span></span>                                                        |
| <span data-ttu-id="28017-115">[**mips. And\[\]\[\]**](sm5-object-texture1d-mipsoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="28017-115">[**mips.Operator\[\]\[\]**](sm5-object-texture1d-mipsoperatorindex.md)</span></span> | <span data-ttu-id="28017-116">Obtient une variable de ressource en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="28017-116">Gets a read-only resource variable.</span></span>                                                        |
| [<span data-ttu-id="28017-117">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="28017-117">**Sample**</span></span>](texture1d-sample.md)                                      | <span data-ttu-id="28017-118">Échantillonne une texture.</span><span class="sxs-lookup"><span data-stu-id="28017-118">Samples a texture.</span></span>                                                                         |
| [<span data-ttu-id="28017-119">**SampleBias**</span><span class="sxs-lookup"><span data-stu-id="28017-119">**SampleBias**</span></span>](texture1d-samplebias.md)                              | <span data-ttu-id="28017-120">Échantillonne une texture après avoir appliqué la valeur de biais au niveau de mipmap.</span><span class="sxs-lookup"><span data-stu-id="28017-120">Samples a texture, after applying the bias value to the mipmap level.</span></span>                      |
| [<span data-ttu-id="28017-121">**SampleCmp**</span><span class="sxs-lookup"><span data-stu-id="28017-121">**SampleCmp**</span></span>](texture1d-samplecmp.md)                                | <span data-ttu-id="28017-122">Échantillonne une texture en utilisant une valeur de comparaison pour rejeter des exemples.</span><span class="sxs-lookup"><span data-stu-id="28017-122">Samples a texture, using a comparison value to reject samples.</span></span>                             |
| [<span data-ttu-id="28017-123">**SampleCmpLevelZero**</span><span class="sxs-lookup"><span data-stu-id="28017-123">**SampleCmpLevelZero**</span></span>](texture1d-samplecmplevelzero.md)              | <span data-ttu-id="28017-124">Échantillonne une texture (mipmap niveau 0 uniquement), en utilisant une valeur de comparaison pour rejeter les exemples.</span><span class="sxs-lookup"><span data-stu-id="28017-124">Samples a texture (mipmap level 0 only), using a comparison value to reject samples.</span></span>       |
| [<span data-ttu-id="28017-125">**SampleGrad**</span><span class="sxs-lookup"><span data-stu-id="28017-125">**SampleGrad**</span></span>](texture1d-samplegrad.md)                              | <span data-ttu-id="28017-126">Échantillonne une texture à l’aide d’un dégradé pour influencer la façon dont l’emplacement de l’échantillon est calculé.</span><span class="sxs-lookup"><span data-stu-id="28017-126">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span> |
| [<span data-ttu-id="28017-127">**SampleLevel**</span><span class="sxs-lookup"><span data-stu-id="28017-127">**SampleLevel**</span></span>](texture1d-samplelevel.md)                            | <span data-ttu-id="28017-128">Échantillonne une texture au niveau du mipmap spécifié.</span><span class="sxs-lookup"><span data-stu-id="28017-128">Samples a texture on the specified mipmap level.</span></span>                                           |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="28017-129">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="28017-129">Minimum Shader Model</span></span>

<span data-ttu-id="28017-130">Cet objet est pris en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="28017-130">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="28017-131">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="28017-131">Shader Model</span></span>                                                                | <span data-ttu-id="28017-132">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="28017-132">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="28017-133">[Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="28017-133">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="28017-134">Oui</span><span class="sxs-lookup"><span data-stu-id="28017-134">yes</span></span>       |



 

<span data-ttu-id="28017-135">Cet objet est pris en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="28017-135">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="28017-136">Sommet</span><span class="sxs-lookup"><span data-stu-id="28017-136">Vertex</span></span> | <span data-ttu-id="28017-137">Forme</span><span class="sxs-lookup"><span data-stu-id="28017-137">Hull</span></span> | <span data-ttu-id="28017-138">Domain</span><span class="sxs-lookup"><span data-stu-id="28017-138">Domain</span></span> | <span data-ttu-id="28017-139">Géométrie</span><span class="sxs-lookup"><span data-stu-id="28017-139">Geometry</span></span> | <span data-ttu-id="28017-140">Pixel</span><span class="sxs-lookup"><span data-stu-id="28017-140">Pixel</span></span> | <span data-ttu-id="28017-141">Compute</span><span class="sxs-lookup"><span data-stu-id="28017-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="28017-142">x</span><span class="sxs-lookup"><span data-stu-id="28017-142">x</span></span>      | <span data-ttu-id="28017-143">x</span><span class="sxs-lookup"><span data-stu-id="28017-143">x</span></span>    | <span data-ttu-id="28017-144">x</span><span class="sxs-lookup"><span data-stu-id="28017-144">x</span></span>      | <span data-ttu-id="28017-145">x</span><span class="sxs-lookup"><span data-stu-id="28017-145">x</span></span>        | <span data-ttu-id="28017-146">x</span><span class="sxs-lookup"><span data-stu-id="28017-146">x</span></span>     | <span data-ttu-id="28017-147">x</span><span class="sxs-lookup"><span data-stu-id="28017-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="28017-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28017-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28017-149">Objets Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="28017-149">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




