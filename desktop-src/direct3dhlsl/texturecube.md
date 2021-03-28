---
title: TextureCube, objet
description: Type TextureCube (tel qu’il existe dans Shader Model 4) et variables de ressource. Cet objet texture prend en charge ces méthodes en plus des méthodes dans le nuanceur modèle 4.
ms.assetid: BC96D7BB-992E-48CC-A774-E211E1BB1720
keywords:
- TextureCube, objet HLSL
- Objet TextureCube HLSL, décrit
topic_type:
- apiref
api_name:
- TextureCube
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 939c79895ae1c24665fc70d6b6cf2ced19854e2b
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/14/2021
ms.locfileid: "104116022"
---
# <a name="texturecube-object"></a><span data-ttu-id="da4b8-106">TextureCube, objet</span><span class="sxs-lookup"><span data-stu-id="da4b8-106">TextureCube object</span></span>

<span data-ttu-id="da4b8-107">Type **TextureCube** ([tel qu’il existe dans Shader Model 4](dx-graphics-hlsl-to-type.md)) et variables de ressource.</span><span class="sxs-lookup"><span data-stu-id="da4b8-107">**TextureCube** type ([as it exists in Shader Model 4](dx-graphics-hlsl-to-type.md)) plus resource variables.</span></span> <span data-ttu-id="da4b8-108">Cet objet texture prend en charge ces méthodes en plus des méthodes dans le nuanceur modèle 4.</span><span class="sxs-lookup"><span data-stu-id="da4b8-108">This texture object supports these methods in addition to the methods in Shader Model 4.</span></span>

-   [<span data-ttu-id="da4b8-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="da4b8-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="da4b8-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="da4b8-110">Methods</span></span>

<span data-ttu-id="da4b8-111">L’objet **TextureCube** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="da4b8-111">The **TextureCube** object has these methods.</span></span>



| <span data-ttu-id="da4b8-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="da4b8-112">Method</span></span>                                                      | <span data-ttu-id="da4b8-113">Description</span><span class="sxs-lookup"><span data-stu-id="da4b8-113">Description</span></span>                                                                                                                                             |
|:------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="da4b8-114">**Gather**</span><span class="sxs-lookup"><span data-stu-id="da4b8-114">**Gather**</span></span>](texturecube-gather.md)                         | <span data-ttu-id="da4b8-115">Retourne les quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="da4b8-115">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                                                |
| [<span data-ttu-id="da4b8-116">**GatherAlpha**</span><span class="sxs-lookup"><span data-stu-id="da4b8-116">**GatherAlpha**</span></span>](texturecube-gatheralpha.md)               | <span data-ttu-id="da4b8-117">Retourne les composants alpha des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="da4b8-117">Returns the alpha components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                        |
| [<span data-ttu-id="da4b8-118">**GatherBlue**</span><span class="sxs-lookup"><span data-stu-id="da4b8-118">**GatherBlue**</span></span>](texturecube-gatherblue.md)                 | <span data-ttu-id="da4b8-119">Retourne les composants bleus des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="da4b8-119">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                         |
| [<span data-ttu-id="da4b8-120">**GatherCmp**</span><span class="sxs-lookup"><span data-stu-id="da4b8-120">**GatherCmp**</span></span>](texturecube-gathercmp.md)                   | <span data-ttu-id="da4b8-121">Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne leur comparaison par rapport à une valeur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="da4b8-121">For four texel values that would be used in a bi-linear filtering operation, returns their comparison against a compare value.</span></span><br/>                      |
| [<span data-ttu-id="da4b8-122">**GatherCmpAlpha**</span><span class="sxs-lookup"><span data-stu-id="da4b8-122">**GatherCmpAlpha**</span></span>](texturecube-gathercmpalpha.md)         | <span data-ttu-id="da4b8-123">Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant alpha par rapport à une valeur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="da4b8-123">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their alpha component against a compare value.</span></span><br/> |
| [<span data-ttu-id="da4b8-124">**GatherCmpBlue**</span><span class="sxs-lookup"><span data-stu-id="da4b8-124">**GatherCmpBlue**</span></span>](texturecube-gathercmpblue.md)           | <span data-ttu-id="da4b8-125">Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant bleu par rapport à une valeur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="da4b8-125">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their blue component against a compare value.</span></span><br/>  |
| [<span data-ttu-id="da4b8-126">**GatherCmpGreen**</span><span class="sxs-lookup"><span data-stu-id="da4b8-126">**GatherCmpGreen**</span></span>](texturecube-gathercmpgreen.md)         | <span data-ttu-id="da4b8-127">Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant vert par rapport à une valeur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="da4b8-127">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their green component against a compare value.</span></span><br/> |
| [<span data-ttu-id="da4b8-128">**GatherCmpRed**</span><span class="sxs-lookup"><span data-stu-id="da4b8-128">**GatherCmpRed**</span></span>](texturecube-gathercmpred.md)             | <span data-ttu-id="da4b8-129">Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant rouge par rapport à une valeur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="da4b8-129">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value.</span></span><br/>   |
| [<span data-ttu-id="da4b8-130">**GatherGreen**</span><span class="sxs-lookup"><span data-stu-id="da4b8-130">**GatherGreen**</span></span>](texturecube-gathergreen.md)               | <span data-ttu-id="da4b8-131">Retourne les composants verts des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="da4b8-131">Returns the green components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                        |
| [<span data-ttu-id="da4b8-132">**GatherRed**</span><span class="sxs-lookup"><span data-stu-id="da4b8-132">**GatherRed**</span></span>](texturecube-gatherred.md)                   | <span data-ttu-id="da4b8-133">Retourne les composants rouges des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="da4b8-133">Returns the red components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                          |
| [<span data-ttu-id="da4b8-134">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="da4b8-134">**Sample**</span></span>](texturecube-sample.md)                         | <span data-ttu-id="da4b8-135">Échantillonne une texture.</span><span class="sxs-lookup"><span data-stu-id="da4b8-135">Samples a texture.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="da4b8-136">**SampleBias**</span><span class="sxs-lookup"><span data-stu-id="da4b8-136">**SampleBias**</span></span>](texturecube-samplebias.md)                 | <span data-ttu-id="da4b8-137">Échantillonne une texture après avoir appliqué la valeur de biais au niveau de mipmap.</span><span class="sxs-lookup"><span data-stu-id="da4b8-137">Samples a texture, after applying the bias value to the mipmap level.</span></span><br/>                                                                               |
| [<span data-ttu-id="da4b8-138">**SampleCmp**</span><span class="sxs-lookup"><span data-stu-id="da4b8-138">**SampleCmp**</span></span>](texturecube-samplecmp.md)                   | <span data-ttu-id="da4b8-139">Échantillonne une texture en utilisant une valeur de comparaison pour rejeter des exemples.</span><span class="sxs-lookup"><span data-stu-id="da4b8-139">Samples a texture, using a comparison value to reject samples.</span></span><br/>                                                                                      |
| [<span data-ttu-id="da4b8-140">**SampleCmpLevelZero**</span><span class="sxs-lookup"><span data-stu-id="da4b8-140">**SampleCmpLevelZero**</span></span>](texturecube-samplecmplevelzero.md) | <span data-ttu-id="da4b8-141">Échantillonne une texture (mipmap niveau 0 uniquement), en utilisant une valeur de comparaison pour rejeter les exemples.</span><span class="sxs-lookup"><span data-stu-id="da4b8-141">Samples a texture (mipmap level 0 only), using a comparison value to reject samples.</span></span><br/>                                                                |
| [<span data-ttu-id="da4b8-142">**SampleGrad**</span><span class="sxs-lookup"><span data-stu-id="da4b8-142">**SampleGrad**</span></span>](texturecube-samplegrad.md)                 | <span data-ttu-id="da4b8-143">Échantillonne une texture à l’aide d’un dégradé pour influencer la façon dont l’emplacement de l’échantillon est calculé.</span><span class="sxs-lookup"><span data-stu-id="da4b8-143">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span><br/>                                                          |
| [<span data-ttu-id="da4b8-144">**SampleLevel**</span><span class="sxs-lookup"><span data-stu-id="da4b8-144">**SampleLevel**</span></span>](texturecube-samplelevel.md)               | <span data-ttu-id="da4b8-145">Échantillonne une texture au niveau du mipmap spécifié.</span><span class="sxs-lookup"><span data-stu-id="da4b8-145">Samples a texture on the specified mipmap level.</span></span><br/>                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="da4b8-146">Notes</span><span class="sxs-lookup"><span data-stu-id="da4b8-146">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="da4b8-147">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="da4b8-147">Minimum Shader Model</span></span>

<span data-ttu-id="da4b8-148">Cet objet est pris en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="da4b8-148">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="da4b8-149">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="da4b8-149">Shader Model</span></span>                                                                | <span data-ttu-id="da4b8-150">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="da4b8-150">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="da4b8-151">[Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="da4b8-151">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="da4b8-152">Oui</span><span class="sxs-lookup"><span data-stu-id="da4b8-152">yes</span></span>       |



 

<span data-ttu-id="da4b8-153">Cet objet est pris en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="da4b8-153">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="da4b8-154">Sommet</span><span class="sxs-lookup"><span data-stu-id="da4b8-154">Vertex</span></span> | <span data-ttu-id="da4b8-155">Forme</span><span class="sxs-lookup"><span data-stu-id="da4b8-155">Hull</span></span> | <span data-ttu-id="da4b8-156">Domain</span><span class="sxs-lookup"><span data-stu-id="da4b8-156">Domain</span></span> | <span data-ttu-id="da4b8-157">Géométrie</span><span class="sxs-lookup"><span data-stu-id="da4b8-157">Geometry</span></span> | <span data-ttu-id="da4b8-158">Pixel</span><span class="sxs-lookup"><span data-stu-id="da4b8-158">Pixel</span></span> | <span data-ttu-id="da4b8-159">Compute</span><span class="sxs-lookup"><span data-stu-id="da4b8-159">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="da4b8-160">x</span><span class="sxs-lookup"><span data-stu-id="da4b8-160">x</span></span>      | <span data-ttu-id="da4b8-161">x</span><span class="sxs-lookup"><span data-stu-id="da4b8-161">x</span></span>    | <span data-ttu-id="da4b8-162">x</span><span class="sxs-lookup"><span data-stu-id="da4b8-162">x</span></span>      | <span data-ttu-id="da4b8-163">x</span><span class="sxs-lookup"><span data-stu-id="da4b8-163">x</span></span>        | <span data-ttu-id="da4b8-164">x</span><span class="sxs-lookup"><span data-stu-id="da4b8-164">x</span></span>     | <span data-ttu-id="da4b8-165">x</span><span class="sxs-lookup"><span data-stu-id="da4b8-165">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="da4b8-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da4b8-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da4b8-167">Objets Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="da4b8-167">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 





