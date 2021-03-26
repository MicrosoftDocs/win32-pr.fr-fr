---
title: Load (objet texture HLSL DirectX)
description: Lit les données Texel sans aucun filtrage ni échantillonnage.
ms.assetid: a2fbda88-29c7-4d28-bd3e-df1d9aa36ee8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 08d3964788a238492ff7d5189544603b35808465
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/05/2021
ms.locfileid: "104108379"
---
# <a name="load-directx-hlsl-texture-object"></a><span data-ttu-id="c2af8-103">Load (objet texture HLSL DirectX)</span><span class="sxs-lookup"><span data-stu-id="c2af8-103">Load (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="c2af8-104">Lit les données Texel sans aucun filtrage ni échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="c2af8-104">Reads texel data without any filtering or sampling.</span></span>



<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c2af8-105">RET Object. Load (</span><span class="sxs-lookup"><span data-stu-id="c2af8-105">ret Object.Load(</span></span><dl> <span data-ttu-id="c2af8-106">Emplacement typeX,</span><span class="sxs-lookup"><span data-stu-id="c2af8-106">typeX Location,</span></span><br />
<span data-ttu-id="c2af8-107">[typeX SampleIndex,]</span><span class="sxs-lookup"><span data-stu-id="c2af8-107">[typeX SampleIndex, ]</span></span><br />
<span data-ttu-id="c2af8-108">[décalage typeX]</span><span class="sxs-lookup"><span data-stu-id="c2af8-108">[typeX Offset ]</span></span><br />
</dl><span data-ttu-id="c2af8-109">);</span><span class="sxs-lookup"><span data-stu-id="c2af8-109">);</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c2af8-110">typeX indique qu’il existe quatre types possibles : **int**, **Int2**, **Int3** ou **INT4**.</span><span class="sxs-lookup"><span data-stu-id="c2af8-110">typeX denotes that there are four possible types: **int**, **int2**, **int3** or **int4**.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="c2af8-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c2af8-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2af8-112"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Dessin*</span><span class="sxs-lookup"><span data-stu-id="c2af8-112"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Object*</span></span>
</dt> <dd>

<span data-ttu-id="c2af8-113">Un type d' [objet texture](dx-graphics-hlsl-to-type.md) (à l’exception de TextureCube ou TextureCubeArray).</span><span class="sxs-lookup"><span data-stu-id="c2af8-113">A [texture-object](dx-graphics-hlsl-to-type.md) type (except TextureCube or TextureCubeArray).</span></span>

</dd> <dt>

<span data-ttu-id="c2af8-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span>*Emplacement*</span><span class="sxs-lookup"><span data-stu-id="c2af8-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span>*Location*</span></span>
</dt> <dd>

<span data-ttu-id="c2af8-115">\[dans \] les coordonnées de texture, le dernier composant spécifie le niveau de mipmap.</span><span class="sxs-lookup"><span data-stu-id="c2af8-115">\[in\] The texture coordinates; the last component specifies the mipmap level.</span></span> <span data-ttu-id="c2af8-116">Cette méthode utilise un système de coordonnées de base 0 et non un système UV 0.0-1.0.</span><span class="sxs-lookup"><span data-stu-id="c2af8-116">This method uses a 0-based coordinate system and not a 0.0-1.0 UV system.</span></span> <span data-ttu-id="c2af8-117">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="c2af8-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="c2af8-118">Type d'objet</span><span class="sxs-lookup"><span data-stu-id="c2af8-118">Object Type</span></span>                                  | <span data-ttu-id="c2af8-119">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="c2af8-119">Parameter Type</span></span> |
|----------------------------------------------|----------------|
| <span data-ttu-id="c2af8-120">Buffer</span><span class="sxs-lookup"><span data-stu-id="c2af8-120">Buffer</span></span>                                       | <span data-ttu-id="c2af8-121">int</span><span class="sxs-lookup"><span data-stu-id="c2af8-121">int</span></span>            |
| <span data-ttu-id="c2af8-122">Texture1D, Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="c2af8-122">Texture1D, Texture2DMS</span></span>                       | <span data-ttu-id="c2af8-123">int2</span><span class="sxs-lookup"><span data-stu-id="c2af8-123">int2</span></span>           |
| <span data-ttu-id="c2af8-124">Texture1DArray, texture 2D, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="c2af8-124">Texture1DArray, Texture 2D, Texture2DMSArray</span></span> | <span data-ttu-id="c2af8-125">int3</span><span class="sxs-lookup"><span data-stu-id="c2af8-125">int3</span></span>           |
| <span data-ttu-id="c2af8-126">Texture2DArray, Texture3D</span><span class="sxs-lookup"><span data-stu-id="c2af8-126">Texture2DArray, Texture3D</span></span>                    | <span data-ttu-id="c2af8-127">int4</span><span class="sxs-lookup"><span data-stu-id="c2af8-127">int4</span></span>           |



 

<span data-ttu-id="c2af8-128">Par exemple, pour accéder à une texture 2D, fournissez des coordonnées UV pour les deux premiers composants et un niveau mipmap pour le troisième composant.</span><span class="sxs-lookup"><span data-stu-id="c2af8-128">For example, to access a 2D texture, supply UV coordinates for the first two components and a mipmap level for the third component.</span></span>

> [!Note]  
> <span data-ttu-id="c2af8-129">Lorsqu’une ou plusieurs des coordonnées de l' *emplacement* dépassent les dimensions de niveau mipmap u, v ou w de la texture, la fonction **Load** retourne zéro dans tous les composants.</span><span class="sxs-lookup"><span data-stu-id="c2af8-129">When one or more of the coordinates in *Location* exceed the u, v, or w mipmap level dimensions of the texture, **Load** returns zero in all components.</span></span> <span data-ttu-id="c2af8-130">Direct3D garantit de retourner zéro pour toute ressource qui est accessible à partir de limites.</span><span class="sxs-lookup"><span data-stu-id="c2af8-130">Direct3D guarantees to return zero for any resource that is accessed out of bounds.</span></span>

 

</dd> <dt>

<span data-ttu-id="c2af8-131"><span id="SampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*SampleIndex*</span><span class="sxs-lookup"><span data-stu-id="c2af8-131"><span id="SampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*SampleIndex*</span></span>
</dt> <dd>

<span data-ttu-id="c2af8-132">\[dans \] un index d’échantillonnage facultatif.</span><span class="sxs-lookup"><span data-stu-id="c2af8-132">\[in\] An optional sampling index.</span></span>



| <span data-ttu-id="c2af8-133">Type de texture</span><span class="sxs-lookup"><span data-stu-id="c2af8-133">Texture Type</span></span>                                                                                                   | <span data-ttu-id="c2af8-134">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="c2af8-134">Parameter Type</span></span> |
|----------------------------------------------------------------------------------------------------------------|----------------|
| <span data-ttu-id="c2af8-135">Texture1D, Texture1DArray, Texture2D, Texture2DArray, Texture3D, Texture2DArray, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="c2af8-135">Texture1D, Texture1DArray, Texture2D, Texture2DArray, Texture3D, Texture2DArray, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="c2af8-136">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2af8-136">not supported</span></span>  |
| <span data-ttu-id="c2af8-137">Texture2DMS, Texture2DMSArray ¹</span><span class="sxs-lookup"><span data-stu-id="c2af8-137">Texture2DMS, Texture2DMSArray¹</span></span>                                                                                 | <span data-ttu-id="c2af8-138">int</span><span class="sxs-lookup"><span data-stu-id="c2af8-138">int</span></span>            |



 

> [!Note]  
> <span data-ttu-id="c2af8-139">*SampleIndex* est disponible uniquement pour les textures à plusieurs échantillons.</span><span class="sxs-lookup"><span data-stu-id="c2af8-139">*SampleIndex* is only available for multi-sample textures.</span></span>

 

</dd> <dt>

<span data-ttu-id="c2af8-140"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span>*Décalage*</span><span class="sxs-lookup"><span data-stu-id="c2af8-140"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span>*Offset*</span></span>
</dt> <dd>

<span data-ttu-id="c2af8-141">\[dans \] un offset facultatif appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="c2af8-141">\[in\] An optional offset applied to the texture coordinates before sampling.</span></span> <span data-ttu-id="c2af8-142">Le type de décalage est dépendant du type de texture-objet et doit être statique.</span><span class="sxs-lookup"><span data-stu-id="c2af8-142">The offset type is dependent on the texture-object type, and needs to be static.</span></span>



| <span data-ttu-id="c2af8-143">Type de texture</span><span class="sxs-lookup"><span data-stu-id="c2af8-143">Texture Type</span></span>                                             | <span data-ttu-id="c2af8-144">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="c2af8-144">Parameter Type</span></span> |
|----------------------------------------------------------|----------------|
| <span data-ttu-id="c2af8-145">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="c2af8-145">Texture1D, Texture1DArray</span></span>                                | <span data-ttu-id="c2af8-146">int</span><span class="sxs-lookup"><span data-stu-id="c2af8-146">int</span></span>            |
| <span data-ttu-id="c2af8-147">Texture2D, Texture2DArray, Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="c2af8-147">Texture2D, Texture2DArray, Texture2DMS, Texture2DMSArray</span></span> | <span data-ttu-id="c2af8-148">int2</span><span class="sxs-lookup"><span data-stu-id="c2af8-148">int2</span></span>           |
| <span data-ttu-id="c2af8-149">Texture3D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="c2af8-149">Texture3D, Texture2DArray</span></span>                                | <span data-ttu-id="c2af8-150">int3</span><span class="sxs-lookup"><span data-stu-id="c2af8-150">int3</span></span>           |



 

> [!Note]  
> <span data-ttu-id="c2af8-151">Si vous utilisez *offset* avec des textures à échantillons multiples, vous devez également spécifier *SampleIndex*.</span><span class="sxs-lookup"><span data-stu-id="c2af8-151">If you use *Offset* with multi-sample textures, you must also specify *SampleIndex*.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2af8-152">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c2af8-152">Return Value</span></span>

<span data-ttu-id="c2af8-153">Le type de retour correspond au type dans la déclaration de l' *objet* .</span><span class="sxs-lookup"><span data-stu-id="c2af8-153">The return type matches the type in the *Object* declaration.</span></span> <span data-ttu-id="c2af8-154">Par exemple, un objet Texture2D qui a été déclaré comme « Texture2d <uint4> myTexture ; » a une valeur de retour de type **uint4**.</span><span class="sxs-lookup"><span data-stu-id="c2af8-154">For example, a Texture2D object that was declared as "Texture2d<uint4> myTexture;" has a return value of type **uint4**.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="c2af8-155">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="c2af8-155">Minimum Shader Model</span></span>

<span data-ttu-id="c2af8-156">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="c2af8-156">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c2af8-157">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c2af8-157">vs\_4\_0</span></span> | <span data-ttu-id="c2af8-158">vs \_ 4 \_ 1 ¹</span><span class="sxs-lookup"><span data-stu-id="c2af8-158">vs\_4\_1¹</span></span> | <span data-ttu-id="c2af8-159">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c2af8-159">ps\_4\_0</span></span> | <span data-ttu-id="c2af8-160">PS \_ 4 \_ 1 ¹</span><span class="sxs-lookup"><span data-stu-id="c2af8-160">ps\_4\_1¹</span></span> | <span data-ttu-id="c2af8-161">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c2af8-161">gs\_4\_0</span></span> | <span data-ttu-id="c2af8-162">GS \_ 4 \_ 1 ¹</span><span class="sxs-lookup"><span data-stu-id="c2af8-162">gs\_4\_1¹</span></span> |
|----------|-----------|----------|-----------|----------|-----------|
| <span data-ttu-id="c2af8-163">x</span><span class="sxs-lookup"><span data-stu-id="c2af8-163">x</span></span>        | <span data-ttu-id="c2af8-164">x</span><span class="sxs-lookup"><span data-stu-id="c2af8-164">x</span></span>         | <span data-ttu-id="c2af8-165">x</span><span class="sxs-lookup"><span data-stu-id="c2af8-165">x</span></span>        | <span data-ttu-id="c2af8-166">x</span><span class="sxs-lookup"><span data-stu-id="c2af8-166">x</span></span>         | <span data-ttu-id="c2af8-167">x</span><span class="sxs-lookup"><span data-stu-id="c2af8-167">x</span></span>        | <span data-ttu-id="c2af8-168">x</span><span class="sxs-lookup"><span data-stu-id="c2af8-168">x</span></span>         |



 

-   <span data-ttu-id="c2af8-169">Le modèle de nuanceur 4,1 est disponible dans Direct3D 10,1 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="c2af8-169">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="example"></a><span data-ttu-id="c2af8-170">Exemple</span><span class="sxs-lookup"><span data-stu-id="c2af8-170">Example</span></span>

<span data-ttu-id="c2af8-171">Cet exemple de code partiel provient du fichier Paint. fx dans l' [exemple AdvancedParticles](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="c2af8-171">This partial code example is from the Paint.fx file in the [AdvancedParticles Sample](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx).</span></span>


```
// Object Declarations
Buffer<float4> g_ParticleBuffer;

// Shader body calling the intrinsic function
float4 PSPaint(PSQuadIn input) : SV_Target
{       
    ... 
    for( int i=g_ParticleStart; i<g_NumParticles; i+=g_ParticleStep )
    {
        ... 
        // load the particle
        float4 particlePos = g_ParticleBuffer.Load( i*4 );
        float4 particleColor = g_ParticleBuffer.Load( (i*4) + 2 );
        ...     
    }
    ...
}   
```



## <a name="related-topics"></a><span data-ttu-id="c2af8-172">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c2af8-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2af8-173">Texture-objet</span><span class="sxs-lookup"><span data-stu-id="c2af8-173">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 




