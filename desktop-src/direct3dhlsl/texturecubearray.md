---
title: TextureCubeArray, objet
description: Type TextureCubeArray (tel qu’il existe dans Shader Model 4) et variables de ressource. Cet objet texture prend en charge ces méthodes en plus des méthodes dans le nuanceur modèle 4.
ms.assetid: 62AAF0F9-D552-4FFA-B681-749D6DC205BD
keywords:
- TextureCubeArray, objet HLSL
- Objet TextureCubeArray HLSL, décrit
topic_type:
- apiref
api_name:
- TextureCubeArray
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e559214626fadbc08b8e9cd4d5568358f130779c
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/14/2021
ms.locfileid: "104991845"
---
# <a name="texturecubearray-object"></a><span data-ttu-id="663f4-106">TextureCubeArray, objet</span><span class="sxs-lookup"><span data-stu-id="663f4-106">TextureCubeArray object</span></span>

<span data-ttu-id="663f4-107">Type **TextureCubeArray** ([tel qu’il existe dans Shader Model 4](dx-graphics-hlsl-to-type.md)) et variables de ressource.</span><span class="sxs-lookup"><span data-stu-id="663f4-107">**TextureCubeArray** type ([as it exists in Shader Model 4](dx-graphics-hlsl-to-type.md)) plus resource variables.</span></span> <span data-ttu-id="663f4-108">Cet objet texture prend en charge ces méthodes en plus des méthodes dans le nuanceur modèle 4.</span><span class="sxs-lookup"><span data-stu-id="663f4-108">This texture object supports these methods in addition to the methods in Shader Model 4.</span></span>

-   [<span data-ttu-id="663f4-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="663f4-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="663f4-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="663f4-110">Methods</span></span>

<span data-ttu-id="663f4-111">L’objet **TextureCubeArray** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="663f4-111">The **TextureCubeArray** object has these methods.</span></span>



| <span data-ttu-id="663f4-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="663f4-112">Method</span></span>                                                           | <span data-ttu-id="663f4-113">Description</span><span class="sxs-lookup"><span data-stu-id="663f4-113">Description</span></span>                                                                                                                                              |
|:-----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="663f4-114">**Gather**</span><span class="sxs-lookup"><span data-stu-id="663f4-114">**Gather**</span></span>](texturecubearray-gather.md)                         | <span data-ttu-id="663f4-115">Retourne les quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="663f4-115">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                                                |
| [<span data-ttu-id="663f4-116">**GatherAlpha**</span><span class="sxs-lookup"><span data-stu-id="663f4-116">**GatherAlpha**</span></span>](texturecubearray-gatheralpha.md)               | <span data-ttu-id="663f4-117">Retourne les composants alpha des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="663f4-117">Returns the alpha components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                        |
| [<span data-ttu-id="663f4-118">**GatherBlue**</span><span class="sxs-lookup"><span data-stu-id="663f4-118">**GatherBlue**</span></span>](texturecubearray-gatherblue.md)                 | <span data-ttu-id="663f4-119">Retourne les composants bleus des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="663f4-119">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                         |
| [<span data-ttu-id="663f4-120">**GatherCmp**</span><span class="sxs-lookup"><span data-stu-id="663f4-120">**GatherCmp**</span></span>](texturecubearray-gathercmp.md)                   | <span data-ttu-id="663f4-121">Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne leur comparaison par rapport à une valeur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="663f4-121">For four texel values that would be used in a bi-linear filtering operation, returns their comparison against a compare value.</span></span><br/>                      |
| [<span data-ttu-id="663f4-122">**GatherCmpAlpha**</span><span class="sxs-lookup"><span data-stu-id="663f4-122">**GatherCmpAlpha**</span></span>](texturecubearray-gathercmpalpha.md)         | <span data-ttu-id="663f4-123">Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant alpha par rapport à une valeur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="663f4-123">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their alpha component against a compare value.</span></span><br/> |
| [<span data-ttu-id="663f4-124">**GatherCmpBlue**</span><span class="sxs-lookup"><span data-stu-id="663f4-124">**GatherCmpBlue**</span></span>](texturecubearray-gathercmpblue.md)           | <span data-ttu-id="663f4-125">Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant bleu par rapport à une valeur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="663f4-125">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their blue component against a compare value.</span></span><br/>  |
| [<span data-ttu-id="663f4-126">**GatherCmpGreen**</span><span class="sxs-lookup"><span data-stu-id="663f4-126">**GatherCmpGreen**</span></span>](texturecubearray-gathercmpgreen.md)         | <span data-ttu-id="663f4-127">Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant vert par rapport à une valeur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="663f4-127">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their green component against a compare value.</span></span><br/> |
| [<span data-ttu-id="663f4-128">**GatherCmpRed**</span><span class="sxs-lookup"><span data-stu-id="663f4-128">**GatherCmpRed**</span></span>](texturecubearray-gathercmpred.md)             | <span data-ttu-id="663f4-129">Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant rouge par rapport à une valeur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="663f4-129">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value.</span></span><br/>   |
| [<span data-ttu-id="663f4-130">**GatherGreen**</span><span class="sxs-lookup"><span data-stu-id="663f4-130">**GatherGreen**</span></span>](texturecubearray-gathergreen.md)               | <span data-ttu-id="663f4-131">Retourne les composants verts des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="663f4-131">Returns the green components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                        |
| [<span data-ttu-id="663f4-132">**GatherRed**</span><span class="sxs-lookup"><span data-stu-id="663f4-132">**GatherRed**</span></span>](texturecubearray-gatherred.md)                   | <span data-ttu-id="663f4-133">Retourne les composants rouges des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="663f4-133">Returns the red components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                          |
| [<span data-ttu-id="663f4-134">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="663f4-134">**Sample**</span></span>](texturecubearray-sample.md)                         | <span data-ttu-id="663f4-135">Échantillonne une texture.</span><span class="sxs-lookup"><span data-stu-id="663f4-135">Samples a texture.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="663f4-136">**SampleBias**</span><span class="sxs-lookup"><span data-stu-id="663f4-136">**SampleBias**</span></span>](texturecubearray-samplebias.md)                 | <span data-ttu-id="663f4-137">Échantillonne une texture après avoir appliqué la valeur de biais au niveau de mipmap.</span><span class="sxs-lookup"><span data-stu-id="663f4-137">Samples a texture, after applying the bias value to the mipmap level.</span></span><br/>                                                                               |
| [<span data-ttu-id="663f4-138">**SampleCmp**</span><span class="sxs-lookup"><span data-stu-id="663f4-138">**SampleCmp**</span></span>](texturecubearray-samplecmp.md)                   | <span data-ttu-id="663f4-139">Échantillonne une texture en utilisant une valeur de comparaison pour rejeter des exemples.</span><span class="sxs-lookup"><span data-stu-id="663f4-139">Samples a texture, using a comparison value to reject samples.</span></span><br/>                                                                                      |
| [<span data-ttu-id="663f4-140">**SampleCmpLevelZero**</span><span class="sxs-lookup"><span data-stu-id="663f4-140">**SampleCmpLevelZero**</span></span>](texturecubearray-samplecmplevelzero.md) | <span data-ttu-id="663f4-141">Échantillonne une texture (mipmap niveau 0 uniquement), en utilisant une valeur de comparaison pour rejeter les exemples.</span><span class="sxs-lookup"><span data-stu-id="663f4-141">Samples a texture (mipmap level 0 only), using a comparison value to reject samples.</span></span><br/>                                                                |
| [<span data-ttu-id="663f4-142">**SampleGrad**</span><span class="sxs-lookup"><span data-stu-id="663f4-142">**SampleGrad**</span></span>](texturecubearray-samplegrad.md)                 | <span data-ttu-id="663f4-143">Échantillonne une texture à l’aide d’un dégradé pour influencer la façon dont l’emplacement de l’échantillon est calculé.</span><span class="sxs-lookup"><span data-stu-id="663f4-143">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span><br/>                                                          |
| [<span data-ttu-id="663f4-144">**SampleLevel**</span><span class="sxs-lookup"><span data-stu-id="663f4-144">**SampleLevel**</span></span>](texturecubearray-samplelevel.md)               | <span data-ttu-id="663f4-145">Échantillonne une texture au niveau du mipmap spécifié.</span><span class="sxs-lookup"><span data-stu-id="663f4-145">Samples a texture on the specified mipmap level.</span></span><br/>                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="663f4-146">Notes</span><span class="sxs-lookup"><span data-stu-id="663f4-146">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="663f4-147">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="663f4-147">Minimum Shader Model</span></span>

<span data-ttu-id="663f4-148">Cet objet est pris en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="663f4-148">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="663f4-149">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="663f4-149">Shader Model</span></span>                                                                | <span data-ttu-id="663f4-150">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="663f4-150">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="663f4-151">[Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="663f4-151">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="663f4-152">Oui</span><span class="sxs-lookup"><span data-stu-id="663f4-152">yes</span></span>       |



 

<span data-ttu-id="663f4-153">Cet objet est pris en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="663f4-153">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="663f4-154">Sommet</span><span class="sxs-lookup"><span data-stu-id="663f4-154">Vertex</span></span> | <span data-ttu-id="663f4-155">Forme</span><span class="sxs-lookup"><span data-stu-id="663f4-155">Hull</span></span> | <span data-ttu-id="663f4-156">Domain</span><span class="sxs-lookup"><span data-stu-id="663f4-156">Domain</span></span> | <span data-ttu-id="663f4-157">Géométrie</span><span class="sxs-lookup"><span data-stu-id="663f4-157">Geometry</span></span> | <span data-ttu-id="663f4-158">Pixel</span><span class="sxs-lookup"><span data-stu-id="663f4-158">Pixel</span></span> | <span data-ttu-id="663f4-159">Compute</span><span class="sxs-lookup"><span data-stu-id="663f4-159">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="663f4-160">x</span><span class="sxs-lookup"><span data-stu-id="663f4-160">x</span></span>      | <span data-ttu-id="663f4-161">x</span><span class="sxs-lookup"><span data-stu-id="663f4-161">x</span></span>    | <span data-ttu-id="663f4-162">x</span><span class="sxs-lookup"><span data-stu-id="663f4-162">x</span></span>      | <span data-ttu-id="663f4-163">x</span><span class="sxs-lookup"><span data-stu-id="663f4-163">x</span></span>        | <span data-ttu-id="663f4-164">x</span><span class="sxs-lookup"><span data-stu-id="663f4-164">x</span></span>     | <span data-ttu-id="663f4-165">x</span><span class="sxs-lookup"><span data-stu-id="663f4-165">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="663f4-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="663f4-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="663f4-167">Objets Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="663f4-167">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 





