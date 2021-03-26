---
title: Texture2DArray
description: Texture2DArray
ms.assetid: 78ab2feb-4d67-4f6f-bffe-48d55183ce28
keywords:
- HLSL Texture2DArray
topic_type:
- apiref
api_name:
- Texture2DArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f1aefa9171ed634934ea5e1306973fe3b22abdfa
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/14/2021
ms.locfileid: "104973871"
---
# <a name="texture2darray"></a><span data-ttu-id="eb3da-104">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="eb3da-104">Texture2DArray</span></span>

<span data-ttu-id="eb3da-105">Type Texture2DArray ([tel qu’il existe dans Shader Model 4](dx-graphics-hlsl-to-type.md)) et variables de ressource.</span><span class="sxs-lookup"><span data-stu-id="eb3da-105">Texture2DArray type ([as it exists in Shader Model 4](dx-graphics-hlsl-to-type.md)) plus resource variables.</span></span> <span data-ttu-id="eb3da-106">Cet objet texture prend en charge les méthodes suivantes en plus des méthodes dans le nuanceur modèle 4.</span><span class="sxs-lookup"><span data-stu-id="eb3da-106">This texture object supports the following methods in addition to the methods in Shader Model 4.</span></span>



| <span data-ttu-id="eb3da-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="eb3da-107">Method</span></span>                                                                      | <span data-ttu-id="eb3da-108">Description</span><span class="sxs-lookup"><span data-stu-id="eb3da-108">Description</span></span>                                                                                                                                         |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eb3da-109">**Gather**</span><span class="sxs-lookup"><span data-stu-id="eb3da-109">**Gather**</span></span>](texture2darray-gather.md)                                      | <span data-ttu-id="eb3da-110">Retourne les quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="eb3da-110">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span>                                                                |
| [<span data-ttu-id="eb3da-111">**GatherRed**</span><span class="sxs-lookup"><span data-stu-id="eb3da-111">**GatherRed**</span></span>](texture2darray-gatherred.md)                                | <span data-ttu-id="eb3da-112">Retourne les composants rouges des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="eb3da-112">Returns the red components of the four texel values that would be used in a bi-linear filtering operation.</span></span>                                          |
| [<span data-ttu-id="eb3da-113">**GatherGreen**</span><span class="sxs-lookup"><span data-stu-id="eb3da-113">**GatherGreen**</span></span>](texture2darray-gathergreen.md)                            | <span data-ttu-id="eb3da-114">Retourne les composants verts des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="eb3da-114">Returns the green components of the four texel values that would be used in a bi-linear filtering operation.</span></span>                                        |
| [<span data-ttu-id="eb3da-115">**GatherBlue**</span><span class="sxs-lookup"><span data-stu-id="eb3da-115">**GatherBlue**</span></span>](texture2darray-gatherblue.md)                              | <span data-ttu-id="eb3da-116">Retourne les composants bleus des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="eb3da-116">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation.</span></span>                                         |
| [<span data-ttu-id="eb3da-117">**GatherAlpha**</span><span class="sxs-lookup"><span data-stu-id="eb3da-117">**GatherAlpha**</span></span>](texture2darray-gatheralpha.md)                            | <span data-ttu-id="eb3da-118">Retourne les composants alpha des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="eb3da-118">Returns the alpha components of the four texel values that would be used in a bi-linear filtering operation.</span></span>                                        |
| [<span data-ttu-id="eb3da-119">**GatherCmp**</span><span class="sxs-lookup"><span data-stu-id="eb3da-119">**GatherCmp**</span></span>](texture2darray-gathercmp.md)                                | <span data-ttu-id="eb3da-120">Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne leur comparaison par rapport à une valeur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="eb3da-120">For four texel values that would be used in a bi-linear filtering operation, returns their comparison against a compare value.</span></span>                      |
| [<span data-ttu-id="eb3da-121">**GatherCmpRed**</span><span class="sxs-lookup"><span data-stu-id="eb3da-121">**GatherCmpRed**</span></span>](texture2darray-gathercmpred.md)                          | <span data-ttu-id="eb3da-122">Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant rouge par rapport à une valeur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="eb3da-122">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value.</span></span>   |
| [<span data-ttu-id="eb3da-123">**GatherCmpGreen**</span><span class="sxs-lookup"><span data-stu-id="eb3da-123">**GatherCmpGreen**</span></span>](texture2darray-gathercmpgreen.md)                      | <span data-ttu-id="eb3da-124">Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant vert par rapport à une valeur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="eb3da-124">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their green component against a compare value.</span></span> |
| [<span data-ttu-id="eb3da-125">**GatherCmpBlue**</span><span class="sxs-lookup"><span data-stu-id="eb3da-125">**GatherCmpBlue**</span></span>](texture2darray-gathercmpblue.md)                        | <span data-ttu-id="eb3da-126">Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant bleu par rapport à une valeur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="eb3da-126">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their blue component against a compare value.</span></span>  |
| [<span data-ttu-id="eb3da-127">**GatherCmpAlpha**</span><span class="sxs-lookup"><span data-stu-id="eb3da-127">**GatherCmpAlpha**</span></span>](texture2darray-gathercmpalpha.md)                      | <span data-ttu-id="eb3da-128">Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant alpha par rapport à une valeur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="eb3da-128">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their alpha component against a compare value.</span></span> |
| [<span data-ttu-id="eb3da-129">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="eb3da-129">**GetDimensions**</span></span>](sm5-object-texture2darray-getdimensions.md)             | <span data-ttu-id="eb3da-130">Obtient les dimensions de ressource.</span><span class="sxs-lookup"><span data-stu-id="eb3da-130">Gets the resource dimensions.</span></span>                                                                                                                       |
| [<span data-ttu-id="eb3da-131">**Load**</span><span class="sxs-lookup"><span data-stu-id="eb3da-131">**Load**</span></span>](texture2darray-load.md)                                          | <span data-ttu-id="eb3da-132">Lit les données de texture.</span><span class="sxs-lookup"><span data-stu-id="eb3da-132">Reads texture data.</span></span>                                                                                                                                 |
| <span data-ttu-id="eb3da-133">[**mips. And\[\]\[\]**](sm5-object-texture2darray-mipsoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="eb3da-133">[**mips.Operator\[\]\[\]**](sm5-object-texture2darray-mipsoperatorindex.md)</span></span> | <span data-ttu-id="eb3da-134">Obtient une variable de ressource en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="eb3da-134">Gets a read-only resource variable.</span></span>                                                                                                                 |
| <span data-ttu-id="eb3da-135">[**Opérateur\[\]**](sm5-object-texture2darray-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="eb3da-135">[**Operator\[\]**](sm5-object-texture2darray-operatorindex.md)</span></span>              | <span data-ttu-id="eb3da-136">Obtient une variable de ressource en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="eb3da-136">Gets a read-only resource variable.</span></span>                                                                                                                 |
| [<span data-ttu-id="eb3da-137">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="eb3da-137">**Sample**</span></span>](texture2darray-sample.md)                                      | <span data-ttu-id="eb3da-138">Échantillonne une texture.</span><span class="sxs-lookup"><span data-stu-id="eb3da-138">Samples a texture.</span></span>                                                                                                                                  |
| [<span data-ttu-id="eb3da-139">**SampleBias**</span><span class="sxs-lookup"><span data-stu-id="eb3da-139">**SampleBias**</span></span>](texture2darray-samplebias.md)                              | <span data-ttu-id="eb3da-140">Échantillonne une texture après avoir appliqué la valeur de biais au niveau de mipmap.</span><span class="sxs-lookup"><span data-stu-id="eb3da-140">Samples a texture, after applying the bias value to the mipmap level.</span></span>                                                                               |
| [<span data-ttu-id="eb3da-141">**SampleCmp**</span><span class="sxs-lookup"><span data-stu-id="eb3da-141">**SampleCmp**</span></span>](texture2darray-samplecmp.md)                                | <span data-ttu-id="eb3da-142">Échantillonne une texture en utilisant une valeur de comparaison pour rejeter des exemples.</span><span class="sxs-lookup"><span data-stu-id="eb3da-142">Samples a texture, using a comparison value to reject samples.</span></span>                                                                                      |
| [<span data-ttu-id="eb3da-143">**SampleCmpLevelZero**</span><span class="sxs-lookup"><span data-stu-id="eb3da-143">**SampleCmpLevelZero**</span></span>](texture2darray-samplecmplevelzero.md)              | <span data-ttu-id="eb3da-144">Échantillonne une texture (mipmap niveau 0 uniquement), en utilisant une valeur de comparaison pour rejeter les exemples.</span><span class="sxs-lookup"><span data-stu-id="eb3da-144">Samples a texture (mipmap level 0 only), using a comparison value to reject samples.</span></span>                                                                |
| [<span data-ttu-id="eb3da-145">**SampleGrad**</span><span class="sxs-lookup"><span data-stu-id="eb3da-145">**SampleGrad**</span></span>](texture2darray-samplegrad.md)                              | <span data-ttu-id="eb3da-146">Échantillonne une texture à l’aide d’un dégradé pour influencer la façon dont l’emplacement de l’échantillon est calculé.</span><span class="sxs-lookup"><span data-stu-id="eb3da-146">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span>                                                          |
| [<span data-ttu-id="eb3da-147">**SampleLevel**</span><span class="sxs-lookup"><span data-stu-id="eb3da-147">**SampleLevel**</span></span>](texture2darray-samplelevel.md)                            | <span data-ttu-id="eb3da-148">Échantillonne une texture au niveau du mipmap spécifié.</span><span class="sxs-lookup"><span data-stu-id="eb3da-148">Samples a texture on the specified mipmap level.</span></span>                                                                                                    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="eb3da-149">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="eb3da-149">Minimum Shader Model</span></span>

<span data-ttu-id="eb3da-150">Cet objet est pris en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="eb3da-150">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="eb3da-151">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="eb3da-151">Shader Model</span></span>                                                                | <span data-ttu-id="eb3da-152">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="eb3da-152">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="eb3da-153">[Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="eb3da-153">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="eb3da-154">Oui</span><span class="sxs-lookup"><span data-stu-id="eb3da-154">yes</span></span>       |



 

<span data-ttu-id="eb3da-155">Cet objet est pris en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="eb3da-155">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="eb3da-156">Sommet</span><span class="sxs-lookup"><span data-stu-id="eb3da-156">Vertex</span></span> | <span data-ttu-id="eb3da-157">Forme</span><span class="sxs-lookup"><span data-stu-id="eb3da-157">Hull</span></span> | <span data-ttu-id="eb3da-158">Domain</span><span class="sxs-lookup"><span data-stu-id="eb3da-158">Domain</span></span> | <span data-ttu-id="eb3da-159">Géométrie</span><span class="sxs-lookup"><span data-stu-id="eb3da-159">Geometry</span></span> | <span data-ttu-id="eb3da-160">Pixel</span><span class="sxs-lookup"><span data-stu-id="eb3da-160">Pixel</span></span> | <span data-ttu-id="eb3da-161">Compute</span><span class="sxs-lookup"><span data-stu-id="eb3da-161">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="eb3da-162">x</span><span class="sxs-lookup"><span data-stu-id="eb3da-162">x</span></span>      | <span data-ttu-id="eb3da-163">x</span><span class="sxs-lookup"><span data-stu-id="eb3da-163">x</span></span>    | <span data-ttu-id="eb3da-164">x</span><span class="sxs-lookup"><span data-stu-id="eb3da-164">x</span></span>      | <span data-ttu-id="eb3da-165">x</span><span class="sxs-lookup"><span data-stu-id="eb3da-165">x</span></span>        | <span data-ttu-id="eb3da-166">x</span><span class="sxs-lookup"><span data-stu-id="eb3da-166">x</span></span>     | <span data-ttu-id="eb3da-167">x</span><span class="sxs-lookup"><span data-stu-id="eb3da-167">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="eb3da-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb3da-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb3da-169">Objets Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="eb3da-169">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




