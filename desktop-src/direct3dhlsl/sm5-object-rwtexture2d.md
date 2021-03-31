---
title: RWTexture2D
description: Ressource en lecture/écriture. | RWTexture2D
ms.assetid: 19b383f1-c787-4c20-b77a-60ef9f212b9f
keywords:
- HLSL RWTexture2D
topic_type:
- apiref
api_name:
- RWTexture2D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ccdeae4dd47d3ad4bf5d756c2ca362033eae6814
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322165"
---
# <a name="rwtexture2d"></a><span data-ttu-id="1bd4b-105">RWTexture2D</span><span class="sxs-lookup"><span data-stu-id="1bd4b-105">RWTexture2D</span></span>

<span data-ttu-id="1bd4b-106">Ressource en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="1bd4b-106">A read/write resource.</span></span>



| <span data-ttu-id="1bd4b-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="1bd4b-107">Method</span></span>                                                        | <span data-ttu-id="1bd4b-108">Description</span><span class="sxs-lookup"><span data-stu-id="1bd4b-108">Description</span></span>                   |
|---------------------------------------------------------------|-------------------------------|
| [<span data-ttu-id="1bd4b-109">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="1bd4b-109">**GetDimensions**</span></span>](sm5-object-rwtexture2d-getdimensions.md) | <span data-ttu-id="1bd4b-110">Obtient les dimensions de ressource.</span><span class="sxs-lookup"><span data-stu-id="1bd4b-110">Gets the resource dimensions.</span></span> |
| [<span data-ttu-id="1bd4b-111">**Load**</span><span class="sxs-lookup"><span data-stu-id="1bd4b-111">**Load**</span></span>](rwtexture2d-load.md)                              | <span data-ttu-id="1bd4b-112">Lit les données de texture.</span><span class="sxs-lookup"><span data-stu-id="1bd4b-112">Reads texture data.</span></span>           |
| <span data-ttu-id="1bd4b-113">[**Opérateur\[\]**](sm5-object-rwtexture2d-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="1bd4b-113">[**Operator\[\]**](sm5-object-rwtexture2d-operatorindex.md)</span></span>  | <span data-ttu-id="1bd4b-114">Obtient une variable de ressource.</span><span class="sxs-lookup"><span data-stu-id="1bd4b-114">Gets a resource variable.</span></span>     |



 

<span data-ttu-id="1bd4b-115">Vous pouvez préfixer les objets RWTexture2D avec la classe de stockage **globallycoherent**.</span><span class="sxs-lookup"><span data-stu-id="1bd4b-115">You can prefix RWTexture2D objects with the storage class **globallycoherent**.</span></span> <span data-ttu-id="1bd4b-116">Cette classe de stockage entraîne des barrières et des synchronisations de la mémoire pour vider les données sur l’ensemble du GPU, de telle sorte que les autres groupes puissent voir les écritures.</span><span class="sxs-lookup"><span data-stu-id="1bd4b-116">This storage class causes memory barriers and syncs to flush data across the entire GPU such that other groups can see writes.</span></span> <span data-ttu-id="1bd4b-117">Sans ce spécificateur, une barrière de mémoire ou une synchronisation vide uniquement un affichage d’accès non ordonné (UAV) dans le groupe actuel.</span><span class="sxs-lookup"><span data-stu-id="1bd4b-117">Without this specifier, a memory barrier or sync will flush only an unordered access view (UAV) within the current group.</span></span>

<span data-ttu-id="1bd4b-118">Un objet RWTexture2D requiert un type d’élément dans une instruction de déclaration pour l’objet.</span><span class="sxs-lookup"><span data-stu-id="1bd4b-118">A RWTexture2D object requires an element type in a declaration statement for the object.</span></span> <span data-ttu-id="1bd4b-119">Par exemple, la déclaration suivante n’est pas correcte :</span><span class="sxs-lookup"><span data-stu-id="1bd4b-119">For example, the following declaration is not correct:</span></span>


```
// The following declaration is incorrectly coded.
RWTexture2D myTexture;
```



<span data-ttu-id="1bd4b-120">La déclaration suivante est correcte :</span><span class="sxs-lookup"><span data-stu-id="1bd4b-120">The following declaration is correct:</span></span>


```
// The following declaration is correctly coded.
RWTexture2D<float> tex;
```



<span data-ttu-id="1bd4b-121">Étant donné qu’un objet RWTexture2D est un objet de type UAV, ses propriétés diffèrent d’un objet de type de vue de ressource (SRV) de nuanceur, tel qu’un objet [Texture2D](sm5-object-texture2d.md) .</span><span class="sxs-lookup"><span data-stu-id="1bd4b-121">Because a RWTexture2D object is a UAV-type object, its properties differ from a shader resource view (SRV)-type object, such as a [Texture2D](sm5-object-texture2d.md) object.</span></span> <span data-ttu-id="1bd4b-122">Par exemple, vous pouvez lire et écrire dans un objet RWTexture2D, mais vous ne pouvez lire qu’à partir d’un objet Texture2D.</span><span class="sxs-lookup"><span data-stu-id="1bd4b-122">For example, you can read from and write to a RWTexture2D object, but you can only read from a Texture2D object.</span></span>

<span data-ttu-id="1bd4b-123">Un objet RWTexture2D ne peut pas utiliser les méthodes d’un objet [Texture2D](sm5-object-texture2d.md) , comme [Sample](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="1bd4b-123">A RWTexture2D object cannot use methods from a [Texture2D](sm5-object-texture2d.md) object, such as [Sample](dx-graphics-hlsl-to-sample.md).</span></span> <span data-ttu-id="1bd4b-124">Toutefois, étant donné que vous pouvez créer plusieurs types d’affichages pour la même ressource, vous pouvez déclarer plusieurs types de texture comme une seule texture dans plusieurs nuanceurs.</span><span class="sxs-lookup"><span data-stu-id="1bd4b-124">However, because you can create multiple view types to the same resource, you can declare multiple texture types as a single texture in multiple shaders.</span></span> <span data-ttu-id="1bd4b-125">Par exemple, les extraits de code suivants montrent comment vous pouvez déclarer et utiliser un objet RWTexture2D comme *Tex* dans un nuanceur de calcul, puis déclarer et utiliser un objet Texture2D comme *Tex* dans un nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="1bd4b-125">For example, the following code snippets show how you can declare and use a RWTexture2D object as *tex* in a compute shader and then declare and use a Texture2D object as *tex* in a pixel shader.</span></span>

> [!Note]  
> <span data-ttu-id="1bd4b-126">Le runtime applique certains modèles d’utilisation quand vous créez plusieurs types d’affichages dans la même ressource.</span><span class="sxs-lookup"><span data-stu-id="1bd4b-126">The runtime enforces certain usage patterns when you create multiple view types to the same resource.</span></span> <span data-ttu-id="1bd4b-127">Par exemple, le runtime ne vous permet pas d’avoir à la fois un mappage UAV pour une ressource et un mappage SRV pour la même ressource active en même temps.</span><span class="sxs-lookup"><span data-stu-id="1bd4b-127">For example, the runtime does not allow you to have both a UAV mapping for a resource and SRV mapping for the same resource active at the same time.</span></span>

 

<span data-ttu-id="1bd4b-128">Le code suivant concerne le nuanceur de calcul :</span><span class="sxs-lookup"><span data-stu-id="1bd4b-128">The following code is for the compute shader:</span></span>


```
RWTexture2D<float> tex;
[numthreads(groupDim_x, groupDim_y, 1)]
void main(
    uint3 groupId : SV_GroupID,
    uint3 groupThreadId : SV_GroupThreadID,
    uint3 dispatchThreadId : SV_DispatchThreadID,
    uint groupIndex : SV_GroupIndex)
{
    tex [dispatchThreadId.xy] = <something>;
}
```



<span data-ttu-id="1bd4b-129">Le code suivant concerne le nuanceur de pixels :</span><span class="sxs-lookup"><span data-stu-id="1bd4b-129">The following code is for the pixel shader:</span></span>


```
struct PixelShaderInput
{
    float4 pos : SV_POSITION;
    float2 tex : TEXTURE;
};

Texture2D<float> tex;
float4 main(PixelShaderInput input) : SV_TARGET
{
    return tex.Sample(TextureSampler, input.tex);
}
```



## <a name="minimum-shader-model"></a><span data-ttu-id="1bd4b-130">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="1bd4b-130">Minimum Shader Model</span></span>

<span data-ttu-id="1bd4b-131">Cet objet est pris en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="1bd4b-131">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="1bd4b-132">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="1bd4b-132">Shader Model</span></span>                                                                | <span data-ttu-id="1bd4b-133">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="1bd4b-133">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="1bd4b-134">[Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="1bd4b-134">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="1bd4b-135">Oui</span><span class="sxs-lookup"><span data-stu-id="1bd4b-135">yes</span></span>       |



 

<span data-ttu-id="1bd4b-136">Cet objet est pris en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="1bd4b-136">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="1bd4b-137">Sommet</span><span class="sxs-lookup"><span data-stu-id="1bd4b-137">Vertex</span></span> | <span data-ttu-id="1bd4b-138">Forme</span><span class="sxs-lookup"><span data-stu-id="1bd4b-138">Hull</span></span> | <span data-ttu-id="1bd4b-139">Domain</span><span class="sxs-lookup"><span data-stu-id="1bd4b-139">Domain</span></span> | <span data-ttu-id="1bd4b-140">Géométrie</span><span class="sxs-lookup"><span data-stu-id="1bd4b-140">Geometry</span></span> | <span data-ttu-id="1bd4b-141">Pixel</span><span class="sxs-lookup"><span data-stu-id="1bd4b-141">Pixel</span></span> | <span data-ttu-id="1bd4b-142">Compute</span><span class="sxs-lookup"><span data-stu-id="1bd4b-142">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="1bd4b-143">x</span><span class="sxs-lookup"><span data-stu-id="1bd4b-143">x</span></span>     | <span data-ttu-id="1bd4b-144">x</span><span class="sxs-lookup"><span data-stu-id="1bd4b-144">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="1bd4b-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1bd4b-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bd4b-146">Objets Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="1bd4b-146">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




