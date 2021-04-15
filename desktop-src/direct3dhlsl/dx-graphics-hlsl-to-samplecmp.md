---
title: SampleCmp (objet texture HLSL DirectX)
description: Échantillonne une texture et compare un composant unique à la valeur de comparaison spécifiée.
ms.assetid: e21894c4-e8c5-4c3d-92c1-727964f8fd94
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6991bead4bfc42451c26fe5476b4c114626eb7e8
ms.sourcegitcommit: 0d6365d4e852b09a9100d9cfb9a5334922ebf478
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/17/2020
ms.locfileid: "104991049"
---
# <a name="samplecmp-directx-hlsl-texture-object"></a><span data-ttu-id="07183-103">SampleCmp (objet texture HLSL DirectX)</span><span class="sxs-lookup"><span data-stu-id="07183-103">SampleCmp (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="07183-104">Échantillonne une texture et compare un composant unique à la valeur de comparaison spécifiée.</span><span class="sxs-lookup"><span data-stu-id="07183-104">Samples a texture and compares a single component against the specified comparison value.</span></span>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="07183-105">float Object. SampleCmp (</span><span class="sxs-lookup"><span data-stu-id="07183-105">float Object.SampleCmp(</span></span> <dl> <span data-ttu-id="07183-106">SamplerComparisonState S,</span><span class="sxs-lookup"><span data-stu-id="07183-106">SamplerComparisonState S,</span></span><br />
<span data-ttu-id="07183-107">Emplacement flottant,</span><span class="sxs-lookup"><span data-stu-id="07183-107">float Location,</span></span><br />
<span data-ttu-id="07183-108">float CompareValue,</span><span class="sxs-lookup"><span data-stu-id="07183-108">float CompareValue,</span></span><br />
<span data-ttu-id="07183-109">[décalage int]</span><span class="sxs-lookup"><span data-stu-id="07183-109">[int Offset]</span></span><br />
</dl><span data-ttu-id="07183-110">);</span><span class="sxs-lookup"><span data-stu-id="07183-110">);</span></span></td>
</tr>
</tbody>
</table>
 

<span data-ttu-id="07183-111">La comparaison est une comparaison à un seul composant entre le premier composant stocké dans la texture et la valeur de comparaison transmise dans la méthode.</span><span class="sxs-lookup"><span data-stu-id="07183-111">The comparison is a single-component comparison between the first component stored in the texture, and the comparison value passed into the method.</span></span>

<span data-ttu-id="07183-112">Cette méthode peut être appelée uniquement à partir d’un nuanceur de pixels ; elle n’est pas prise en charge dans un nuanceur de sommets ou de géométrie.</span><span class="sxs-lookup"><span data-stu-id="07183-112">This method can be invoked only from a pixel shader; it isn't supported in a vertex or geometry shader.</span></span>

## <a name="parameters"></a><span data-ttu-id="07183-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="07183-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07183-114"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Dessin*</span><span class="sxs-lookup"><span data-stu-id="07183-114"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Object*</span></span>
</dt> <dd>

<span data-ttu-id="07183-115">Tout type d' [objet texture](dx-graphics-hlsl-to-type.md) (à l’exception de Texture2DMS, Texture2DMSArray ou Texture3D).</span><span class="sxs-lookup"><span data-stu-id="07183-115">Any [texture-object](dx-graphics-hlsl-to-type.md) type (except Texture2DMS, Texture2DMSArray, or Texture3D).</span></span>

</dd> <dt>

<span data-ttu-id="07183-116"><span id="S"></span><span id="s"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="07183-116"><span id="S"></span><span id="s"></span>*S*</span></span>
</dt> <dd>

<span data-ttu-id="07183-117">\[dans \] un état de comparaison d’échantillonneur, qui est l’état de l’échantillonneur plus un état de comparaison (une fonction de comparaison et un filtre de comparaison).</span><span class="sxs-lookup"><span data-stu-id="07183-117">\[in\] A sampler-comparison state, which is the sampler state plus a comparison state (a comparison function and a comparison filter).</span></span> <span data-ttu-id="07183-118">Pour plus d’informations et pour obtenir un exemple, consultez [type d’échantillonneur](dx-graphics-hlsl-sampler.md) .</span><span class="sxs-lookup"><span data-stu-id="07183-118">See the [sampler type](dx-graphics-hlsl-sampler.md) for details and an example.</span></span>

</dd> <dt>

<span data-ttu-id="07183-119"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span>*Emplacement*</span><span class="sxs-lookup"><span data-stu-id="07183-119"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span>*Location*</span></span>
</dt> <dd>

<span data-ttu-id="07183-120">\[dans \] les coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="07183-120">\[in\] The texture coordinates.</span></span> <span data-ttu-id="07183-121">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="07183-121">The argument type is dependent on the texture-object type.</span></span>

| <span data-ttu-id="07183-122">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="07183-122">Texture-Object Type</span></span>          | <span data-ttu-id="07183-123">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="07183-123">Parameter Type</span></span> |
|------------------------------|----------------|
| <span data-ttu-id="07183-124">Texture1D</span><span class="sxs-lookup"><span data-stu-id="07183-124">Texture1D</span></span>                    | <span data-ttu-id="07183-125">float</span><span class="sxs-lookup"><span data-stu-id="07183-125">float</span></span>          |
| <span data-ttu-id="07183-126">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="07183-126">Texture1DArray, Texture2D</span></span>    | <span data-ttu-id="07183-127">float2</span><span class="sxs-lookup"><span data-stu-id="07183-127">float2</span></span>         |
| <span data-ttu-id="07183-128">Texture2DArray ¹, TextureCube</span><span class="sxs-lookup"><span data-stu-id="07183-128">Texture2DArray¹, TextureCube</span></span> | <span data-ttu-id="07183-129">float3</span><span class="sxs-lookup"><span data-stu-id="07183-129">float3</span></span>         |
| <span data-ttu-id="07183-130">TextureCubeArray ¹</span><span class="sxs-lookup"><span data-stu-id="07183-130">TextureCubeArray¹</span></span>            | <span data-ttu-id="07183-131">float4</span><span class="sxs-lookup"><span data-stu-id="07183-131">float4</span></span>         |

</dd> <dt>

<span data-ttu-id="07183-132"><span id="CompareValue"></span><span id="comparevalue"></span><span id="COMPAREVALUE"></span>*CompareValue*</span><span class="sxs-lookup"><span data-stu-id="07183-132"><span id="CompareValue"></span><span id="comparevalue"></span><span id="COMPAREVALUE"></span>*CompareValue*</span></span>
</dt> <dd>

<span data-ttu-id="07183-133">Valeur à virgule flottante à utiliser comme valeur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="07183-133">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="07183-134"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span>*Décalage*</span><span class="sxs-lookup"><span data-stu-id="07183-134"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span>*Offset*</span></span>
</dt> <dd>

<span data-ttu-id="07183-135">\[dans \] un décalage de coordonnée de texture facultatif, qui peut être utilisé pour tout type d’objet de texture ; le décalage est appliqué à l’emplacement avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="07183-135">\[in\] An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="07183-136">Les décalages de texture doivent être statiques.</span><span class="sxs-lookup"><span data-stu-id="07183-136">The texture offsets need to be static.</span></span> <span data-ttu-id="07183-137">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="07183-137">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="07183-138">Pour plus d’informations, consultez [application de décalages de coordonnées de texture](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="07183-138">For more info, see [Applying texture coordinate offsets](dx-graphics-hlsl-to-sample.md).</span></span>

| <span data-ttu-id="07183-139">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="07183-139">Texture-Object Type</span></span>            | <span data-ttu-id="07183-140">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="07183-140">Parameter Type</span></span> |
|--------------------------------|----------------|
| <span data-ttu-id="07183-141">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="07183-141">Texture1D, Texture1DArray</span></span>      | <span data-ttu-id="07183-142">int</span><span class="sxs-lookup"><span data-stu-id="07183-142">int</span></span>            |
| <span data-ttu-id="07183-143">Texture2D, Texture2DArray ¹</span><span class="sxs-lookup"><span data-stu-id="07183-143">Texture2D, Texture2DArray¹</span></span>     | <span data-ttu-id="07183-144">int2</span><span class="sxs-lookup"><span data-stu-id="07183-144">int2</span></span>           |
| <span data-ttu-id="07183-145">TextureCube, TextureCubeArray ¹</span><span class="sxs-lookup"><span data-stu-id="07183-145">TextureCube, TextureCubeArray¹</span></span> | <span data-ttu-id="07183-146">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="07183-146">Not supported</span></span>  |

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07183-147">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="07183-147">Return Value</span></span>

<span data-ttu-id="07183-148">Retourne une valeur à virgule flottante dans la plage \[ 0.. 1 \] .</span><span class="sxs-lookup"><span data-stu-id="07183-148">Returns a floating-point value in the range \[0..1\].</span></span>

<span data-ttu-id="07183-149">Pour chaque élément Texel récupéré (en fonction de la configuration de l’échantillonneur du mode filtre), **SampleCmp** effectue une comparaison de la valeur z (le troisième composant de l’entrée) du nuanceur à la valeur Texel (1 si la comparaison réussit ; sinon, 0).</span><span class="sxs-lookup"><span data-stu-id="07183-149">For each texel fetched (based on the sampler configuration of the filter mode), **SampleCmp** performs a comparison of the z value (3rd component of input) from the shader against the texel value (1 if the comparison passes; otherwise 0).</span></span> <span data-ttu-id="07183-150">**SampleCmp** fusionne ensuite ces résultats 0 et 1 pour chaque Texel ensemble comme dans le filtrage de texture normal (et non en moyenne) et retourne la \[ valeur 0.. 1 obtenue \] au nuanceur.</span><span class="sxs-lookup"><span data-stu-id="07183-150">**SampleCmp** then blends these 0 and 1 results for each texel together as in normal texture filtering (not an average) and returns the resulting \[0..1\] value to the shader.</span></span>

## <a name="remarks"></a><span data-ttu-id="07183-151">Notes</span><span class="sxs-lookup"><span data-stu-id="07183-151">Remarks</span></span>

<span data-ttu-id="07183-152">Le filtrage de comparaison fournit une opération de filtrage de base qui est utile pour le filtrage en pourcentage plus profond.</span><span class="sxs-lookup"><span data-stu-id="07183-152">Comparison filtering provides a basic filtering operation that is useful for percentage-closer-depth filtering.</span></span>

<span data-ttu-id="07183-153">Lors de l’utilisation de cette méthode sur une ressource à virgule flottante (au lieu d’un format normalisé normalisé ou non signé), la valeur de comparaison n’est pas automatiquement ancrée entre 0,0 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="07183-153">When using this method on a floating-point resource (Instead of a signed-normalized or unsigned-normalized format), the comparison value is not automatically clamped between 0.0 and 1.0.</span></span> <span data-ttu-id="07183-154">Par conséquent, une fixation manuelle de la valeur de comparaison peut être nécessaire pour les techniques d’occultation courantes.</span><span class="sxs-lookup"><span data-stu-id="07183-154">Therefore, a manual clamp of the comparison value may be necessary for common shadowing techniques.</span></span>

<span data-ttu-id="07183-155">Utilisez un décalage uniquement au niveau d’un miplevel entier ; dans le cas contraire, vous risquez d’obtenir des résultats différents en fonction de l’implémentation matérielle ou des paramètres du pilote.</span><span class="sxs-lookup"><span data-stu-id="07183-155">Use an offset only at an integer miplevel; otherwise, you may get different results depending on hardware implementation or driver settings.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="07183-156">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="07183-156">Minimum Shader Model</span></span>

<span data-ttu-id="07183-157">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="07183-157">This function is supported in the following shader models.</span></span>

| <span data-ttu-id="07183-158">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="07183-158">vs\_4\_0</span></span> | <span data-ttu-id="07183-159">vs \_ 4 \_ 1 ²</span><span class="sxs-lookup"><span data-stu-id="07183-159">vs\_4\_1²</span></span> | <span data-ttu-id="07183-160">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="07183-160">ps\_4\_0</span></span> | <span data-ttu-id="07183-161">PS \_ 4 \_ 1 ²</span><span class="sxs-lookup"><span data-stu-id="07183-161">ps\_4\_1²</span></span> | <span data-ttu-id="07183-162">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="07183-162">gs\_4\_0</span></span> | <span data-ttu-id="07183-163">GS \_ 4 \_ 1 ²</span><span class="sxs-lookup"><span data-stu-id="07183-163">gs\_4\_1²</span></span> |
|----------|-----------|----------|-----------|----------|-----------|
|          |           | <span data-ttu-id="07183-164">x ¹</span><span class="sxs-lookup"><span data-stu-id="07183-164">x¹</span></span>       | <span data-ttu-id="07183-165">x</span><span class="sxs-lookup"><span data-stu-id="07183-165">x</span></span>         |          |           |

1.  <span data-ttu-id="07183-166">Texture2DArray et TextureCubeArray sont disponibles dans le modèle de nuanceur 4,1 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="07183-166">Texture2DArray and TextureCubeArray are available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="07183-167">Le modèle de nuanceur 4,1 est disponible dans Direct3D 10,1 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="07183-167">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

> [!NOTE]  
> <span data-ttu-id="07183-168">**SampleCmp** est également disponible dans PS 4 \_ 0 \_ Level \_ 9 \_ 1 et 4 \_ 0 \_ Level \_ 9 \_ 3 lorsque vous utilisez les techniques décrites dans implémentation de [mémoires tampons secondaires pour la fonctionnalité Direct3D de niveau 9](/previous-versions/windows/apps/jj262110(v=win.10)).</span><span class="sxs-lookup"><span data-stu-id="07183-168">**SampleCmp** is also available in ps 4\_0\_level\_9\_1 and 4\_0\_level\_9\_3 when you use the techniques that are described in [Implementing shadow buffers for Direct3D feature level 9](/previous-versions/windows/apps/jj262110(v=win.10)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="07183-169">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="07183-169">Related topics</span></span>

[<span data-ttu-id="07183-170">Texture-objet</span><span class="sxs-lookup"><span data-stu-id="07183-170">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
