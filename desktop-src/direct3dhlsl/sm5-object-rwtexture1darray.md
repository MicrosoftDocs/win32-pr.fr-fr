---
title: RWTexture1DArray
description: Ressource en lecture/écriture. | RWTexture1DArray
ms.assetid: 214c7e7d-4e74-4f4f-bf78-98e9df0b3a0e
keywords:
- HLSL RWTexture1DArray
topic_type:
- apiref
api_name:
- RWTexture1DArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2e7f6841cb1f15b12c9755da2a9fae50e42ed333
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103953667"
---
# <a name="rwtexture1darray"></a><span data-ttu-id="f539b-105">RWTexture1DArray</span><span class="sxs-lookup"><span data-stu-id="f539b-105">RWTexture1DArray</span></span>

<span data-ttu-id="f539b-106">Ressource en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="f539b-106">A read/write resource.</span></span>



| <span data-ttu-id="f539b-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="f539b-107">Method</span></span>                                                             | <span data-ttu-id="f539b-108">Description</span><span class="sxs-lookup"><span data-stu-id="f539b-108">Description</span></span>                   |
|--------------------------------------------------------------------|-------------------------------|
| [<span data-ttu-id="f539b-109">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="f539b-109">**GetDimensions**</span></span>](sm5-object-rwtexture1darray-getdimensions.md) | <span data-ttu-id="f539b-110">Obtient les dimensions de ressource.</span><span class="sxs-lookup"><span data-stu-id="f539b-110">Gets the resource dimensions.</span></span> |
| [<span data-ttu-id="f539b-111">**Load**</span><span class="sxs-lookup"><span data-stu-id="f539b-111">**Load**</span></span>](rwtexture1darray-load.md)                              | <span data-ttu-id="f539b-112">Lit les données de texture.</span><span class="sxs-lookup"><span data-stu-id="f539b-112">Reads texture data.</span></span>           |
| <span data-ttu-id="f539b-113">[**Opérateur\[\]**](sm5-object-rwtexture1darray-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="f539b-113">[**Operator\[\]**](sm5-object-rwtexture1darray-operatorindex.md)</span></span>  | <span data-ttu-id="f539b-114">Obtient une variable de ressource.</span><span class="sxs-lookup"><span data-stu-id="f539b-114">Gets a resource variable.</span></span>     |



 

<span data-ttu-id="f539b-115">Vous pouvez préfixer les objets **RWTexture1DArray** avec la classe de stockage **globallycoherent**.</span><span class="sxs-lookup"><span data-stu-id="f539b-115">You can prefix **RWTexture1DArray** objects with the storage class **globallycoherent**.</span></span> <span data-ttu-id="f539b-116">Cette classe de stockage entraîne des barrières et des synchronisations de la mémoire pour vider les données sur l’ensemble du GPU, de telle sorte que les autres groupes puissent voir les écritures.</span><span class="sxs-lookup"><span data-stu-id="f539b-116">This storage class causes memory barriers and syncs to flush data across the entire GPU such that other groups can see writes.</span></span> <span data-ttu-id="f539b-117">Sans ce spécificateur, une barrière de mémoire ou une synchronisation vide un UAV uniquement dans le groupe actuel.</span><span class="sxs-lookup"><span data-stu-id="f539b-117">Without this specifier, a memory barrier or sync will flush a UAV only within the current group.</span></span>

<span data-ttu-id="f539b-118">Un objet **RWTexture1DArray** requiert un type d’élément dans une instruction de déclaration pour l’objet.</span><span class="sxs-lookup"><span data-stu-id="f539b-118">A **RWTexture1DArray** object requires an element type in a declaration statement for the object.</span></span> <span data-ttu-id="f539b-119">Par exemple, la déclaration suivante est correcte :</span><span class="sxs-lookup"><span data-stu-id="f539b-119">For example, the following declaration is correct:</span></span>


```
RWTexture1DArray<float> tex;
```



<span data-ttu-id="f539b-120">Étant donné qu’un objet **RWTexture1DArray** est un objet de type UAV, ses propriétés diffèrent d’un objet de type de vue de ressource (SRV) de nuanceur, tel qu’un objet [**Texture1DArray**](sm5-object-texture1darray.md) .</span><span class="sxs-lookup"><span data-stu-id="f539b-120">Because a **RWTexture1DArray** object is a UAV-type object, its properties differ from a shader resource view (SRV)-type object, such as a [**Texture1DArray**](sm5-object-texture1darray.md) object.</span></span> <span data-ttu-id="f539b-121">Par exemple, vous pouvez lire et écrire dans un objet **RWTexture1DArray** , mais vous ne pouvez lire qu’à partir d’un objet **Texture1DArray** .</span><span class="sxs-lookup"><span data-stu-id="f539b-121">For example, you can read from and write to a **RWTexture1DArray** object, but you can only read from a **Texture1DArray** object.</span></span>

<span data-ttu-id="f539b-122">Un objet **RWTexture1DArray** ne peut pas utiliser les méthodes d’un objet [**Texture1DArray**](sm5-object-texture1darray.md) , comme [Sample](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="f539b-122">A **RWTexture1DArray** object cannot use methods from a [**Texture1DArray**](sm5-object-texture1darray.md) object, such as [Sample](dx-graphics-hlsl-to-sample.md).</span></span> <span data-ttu-id="f539b-123">Toutefois, étant donné que vous pouvez créer plusieurs types d’affichages pour la même ressource, vous pouvez déclarer plusieurs types de texture comme une seule texture dans plusieurs nuanceurs.</span><span class="sxs-lookup"><span data-stu-id="f539b-123">However, because you can create multiple view types to the same resource, you can declare multiple texture types as a single texture in multiple shaders.</span></span> <span data-ttu-id="f539b-124">Par exemple, vous pouvez déclarer et utiliser un objet **RWTexture1DArray** comme *Tex* dans un nuanceur de calcul, puis déclarer et utiliser un objet **Texture1DArray** comme *Tex* dans un nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="f539b-124">For example, you can declare and use a **RWTexture1DArray** object as *tex* in a compute shader and then declare and use a **Texture1DArray** object as *tex* in a pixel shader.</span></span>

> [!Note]  
> <span data-ttu-id="f539b-125">Le runtime applique certains modèles d’utilisation quand vous créez plusieurs types d’affichages dans la même ressource.</span><span class="sxs-lookup"><span data-stu-id="f539b-125">The runtime enforces certain usage patterns when you create multiple view types to the same resource.</span></span> <span data-ttu-id="f539b-126">Par exemple, le runtime ne vous permet pas d’avoir à la fois un mappage UAV pour une ressource et un mappage SRV pour la même ressource active en même temps.</span><span class="sxs-lookup"><span data-stu-id="f539b-126">For example, the runtime does not allow you to have both a UAV mapping for a resource and SRV mapping for the same resource active at the same time.</span></span>

 

## <a name="minimum-shader-model"></a><span data-ttu-id="f539b-127">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="f539b-127">Minimum Shader Model</span></span>

<span data-ttu-id="f539b-128">Cet objet est pris en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="f539b-128">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="f539b-129">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="f539b-129">Shader Model</span></span>                                                                | <span data-ttu-id="f539b-130">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="f539b-130">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="f539b-131">[Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="f539b-131">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="f539b-132">Oui</span><span class="sxs-lookup"><span data-stu-id="f539b-132">yes</span></span>       |



 

<span data-ttu-id="f539b-133">Cet objet est pris en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="f539b-133">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="f539b-134">Sommet</span><span class="sxs-lookup"><span data-stu-id="f539b-134">Vertex</span></span> | <span data-ttu-id="f539b-135">Forme</span><span class="sxs-lookup"><span data-stu-id="f539b-135">Hull</span></span> | <span data-ttu-id="f539b-136">Domain</span><span class="sxs-lookup"><span data-stu-id="f539b-136">Domain</span></span> | <span data-ttu-id="f539b-137">Géométrie</span><span class="sxs-lookup"><span data-stu-id="f539b-137">Geometry</span></span> | <span data-ttu-id="f539b-138">Pixel</span><span class="sxs-lookup"><span data-stu-id="f539b-138">Pixel</span></span> | <span data-ttu-id="f539b-139">Compute</span><span class="sxs-lookup"><span data-stu-id="f539b-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="f539b-140">x</span><span class="sxs-lookup"><span data-stu-id="f539b-140">x</span></span>     | <span data-ttu-id="f539b-141">x</span><span class="sxs-lookup"><span data-stu-id="f539b-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="f539b-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f539b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f539b-143">Objets Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="f539b-143">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




