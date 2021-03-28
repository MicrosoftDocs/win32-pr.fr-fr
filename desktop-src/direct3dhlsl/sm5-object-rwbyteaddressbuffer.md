---
title: RWByteAddressBuffer
description: Mémoire tampon de lecture/écriture qui indexe en octets.
ms.assetid: 8370c14c-5822-4240-942d-565aa223d48c
keywords:
- HLSL RWByteAddressBuffer
topic_type:
- apiref
api_name:
- RWByteAddressBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4d065926b0769e15284cbe705783be012d82554b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104381984"
---
# <a name="rwbyteaddressbuffer"></a><span data-ttu-id="5706e-104">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="5706e-104">RWByteAddressBuffer</span></span>

<span data-ttu-id="5706e-105">Mémoire tampon de lecture/écriture qui indexe en octets.</span><span class="sxs-lookup"><span data-stu-id="5706e-105">A read/write buffer that indexes in bytes.</span></span>



| <span data-ttu-id="5706e-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="5706e-106">Method</span></span>                                                                                          | <span data-ttu-id="5706e-107">Description</span><span class="sxs-lookup"><span data-stu-id="5706e-107">Description</span></span>                         |
|-------------------------------------------------------------------------------------------------|-------------------------------------|
| [<span data-ttu-id="5706e-108">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="5706e-108">**GetDimensions**</span></span>](sm5-object-rwbyteaddressbuffer-getdimensions.md)                           | <span data-ttu-id="5706e-109">Obtient les dimensions de ressource.</span><span class="sxs-lookup"><span data-stu-id="5706e-109">Gets the resource dimensions.</span></span>       |
| [<span data-ttu-id="5706e-110">**InterlockedAdd**</span><span class="sxs-lookup"><span data-stu-id="5706e-110">**InterlockedAdd**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedadd.md)                         | <span data-ttu-id="5706e-111">Ajoute, atomiquement.</span><span class="sxs-lookup"><span data-stu-id="5706e-111">Adds, atomically.</span></span>                   |
| [<span data-ttu-id="5706e-112">**InterlockedAnd**</span><span class="sxs-lookup"><span data-stu-id="5706e-112">**InterlockedAnd**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedand.md)                         | <span data-ttu-id="5706e-113">ANDs, atomiquement.</span><span class="sxs-lookup"><span data-stu-id="5706e-113">ANDs, atomically.</span></span>                   |
| [<span data-ttu-id="5706e-114">**InterlockedCompareExchange**</span><span class="sxs-lookup"><span data-stu-id="5706e-114">**InterlockedCompareExchange**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedcompareexchange.md) | <span data-ttu-id="5706e-115">Compare et échange, de manière atomique.</span><span class="sxs-lookup"><span data-stu-id="5706e-115">Compares and exchanges, atomically.</span></span> |
| [<span data-ttu-id="5706e-116">**InterlockedCompareStore**</span><span class="sxs-lookup"><span data-stu-id="5706e-116">**InterlockedCompareStore**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedcomparestore.md)       | <span data-ttu-id="5706e-117">Compare et stocke atomiquement.</span><span class="sxs-lookup"><span data-stu-id="5706e-117">Compares and stores, atomically.</span></span>    |
| [<span data-ttu-id="5706e-118">**Interlockedexchang**</span><span class="sxs-lookup"><span data-stu-id="5706e-118">**InterlockedExchange**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedexchange.md)               | <span data-ttu-id="5706e-119">Les échanges, de manière atomique.</span><span class="sxs-lookup"><span data-stu-id="5706e-119">Exchanges, atomically.</span></span>              |
| [<span data-ttu-id="5706e-120">**InterlockedMax**</span><span class="sxs-lookup"><span data-stu-id="5706e-120">**InterlockedMax**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedmax.md)                         | <span data-ttu-id="5706e-121">Recherche le nombre maximal, atomique.</span><span class="sxs-lookup"><span data-stu-id="5706e-121">Finds the max, atomically.</span></span>          |
| [<span data-ttu-id="5706e-122">**InterlockedMin**</span><span class="sxs-lookup"><span data-stu-id="5706e-122">**InterlockedMin**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedmin.md)                         | <span data-ttu-id="5706e-123">Rechercher le minimum, atomiquement.</span><span class="sxs-lookup"><span data-stu-id="5706e-123">Find the min, atomically.</span></span>           |
| [<span data-ttu-id="5706e-124">**Interverrouiller**</span><span class="sxs-lookup"><span data-stu-id="5706e-124">**InterlockedOr**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedor.md)                           | <span data-ttu-id="5706e-125">ORs, atomiquement.</span><span class="sxs-lookup"><span data-stu-id="5706e-125">ORs, atomically.</span></span>                    |
| [<span data-ttu-id="5706e-126">**InterlockedXor**</span><span class="sxs-lookup"><span data-stu-id="5706e-126">**InterlockedXor**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedxor.md)                         | <span data-ttu-id="5706e-127">XORs, atomiquement.</span><span class="sxs-lookup"><span data-stu-id="5706e-127">XORs, atomically.</span></span>                   |
| [<span data-ttu-id="5706e-128">**Load**</span><span class="sxs-lookup"><span data-stu-id="5706e-128">**Load**</span></span>](rwbyteaddressbuffer-load.md)                                                        | <span data-ttu-id="5706e-129">Obtient une valeur.</span><span class="sxs-lookup"><span data-stu-id="5706e-129">Gets one value.</span></span>                     |
| [<span data-ttu-id="5706e-130">**Load2**</span><span class="sxs-lookup"><span data-stu-id="5706e-130">**Load2**</span></span>](rwbyteaddressbuffer-load2.md)                                                      | <span data-ttu-id="5706e-131">Obtient deux valeurs.</span><span class="sxs-lookup"><span data-stu-id="5706e-131">Gets two values.</span></span>                    |
| [<span data-ttu-id="5706e-132">**Load3**</span><span class="sxs-lookup"><span data-stu-id="5706e-132">**Load3**</span></span>](rwbyteaddressbuffer-load3.md)                                                      | <span data-ttu-id="5706e-133">Obtient trois valeurs.</span><span class="sxs-lookup"><span data-stu-id="5706e-133">Gets three values.</span></span>                  |
| [<span data-ttu-id="5706e-134">**Load4**</span><span class="sxs-lookup"><span data-stu-id="5706e-134">**Load4**</span></span>](rwbyteaddressbuffer-load4.md)                                                      | <span data-ttu-id="5706e-135">Obtient quatre valeurs.</span><span class="sxs-lookup"><span data-stu-id="5706e-135">Gets four values.</span></span>                   |
| [<span data-ttu-id="5706e-136">**Store**</span><span class="sxs-lookup"><span data-stu-id="5706e-136">**Store**</span></span>](sm5-object-rwbyteaddressbuffer-store.md)                                           | <span data-ttu-id="5706e-137">Définit une valeur.</span><span class="sxs-lookup"><span data-stu-id="5706e-137">Sets one value.</span></span>                     |
| [<span data-ttu-id="5706e-138">**Banque**</span><span class="sxs-lookup"><span data-stu-id="5706e-138">**Store2**</span></span>](sm5-object-rwbyteaddressbuffer-store2.md)                                         | <span data-ttu-id="5706e-139">Définit deux valeurs.</span><span class="sxs-lookup"><span data-stu-id="5706e-139">Sets two values.</span></span>                    |
| [<span data-ttu-id="5706e-140">**Store3**</span><span class="sxs-lookup"><span data-stu-id="5706e-140">**Store3**</span></span>](sm5-object-rwbyteaddressbuffer-store3.md)                                         | <span data-ttu-id="5706e-141">Définit trois valeurs.</span><span class="sxs-lookup"><span data-stu-id="5706e-141">Sets three values.</span></span>                  |
| [<span data-ttu-id="5706e-142">**Store4**</span><span class="sxs-lookup"><span data-stu-id="5706e-142">**Store4**</span></span>](sm5-object-rwbyteaddressbuffer-store4.md)                                         | <span data-ttu-id="5706e-143">Définit quatre valeurs.</span><span class="sxs-lookup"><span data-stu-id="5706e-143">Sets four values.</span></span>                   |



 

<span data-ttu-id="5706e-144">Les objets RWByteAddressBuffer peuvent être précédés de la classe de stockage **globallycoherent**.</span><span class="sxs-lookup"><span data-stu-id="5706e-144">RWByteAddressBuffer objects can be prefixed with the storage class **globallycoherent**.</span></span> <span data-ttu-id="5706e-145">Cette classe de stockage entraîne des barrières et des synchronisations de la mémoire pour vider les données sur l’ensemble du GPU, de telle sorte que les autres groupes puissent voir les écritures.</span><span class="sxs-lookup"><span data-stu-id="5706e-145">This storage class causes memory barriers and syncs to flush data across the entire GPU such that other groups can see writes.</span></span> <span data-ttu-id="5706e-146">Sans ce spécificateur, une barrière de mémoire ou une synchronisation vide un UAV uniquement dans le groupe actuel.</span><span class="sxs-lookup"><span data-stu-id="5706e-146">Without this specifier, a memory barrier or sync will flush a UAV only within the current group.</span></span>

<span data-ttu-id="5706e-147">Le format UAV lié à cette ressource doit être créé avec le format DXGI \_ \_ R32 sans \_ type.</span><span class="sxs-lookup"><span data-stu-id="5706e-147">The UAV format bound to this resource needs to be created with the DXGI\_FORMAT\_R32\_TYPELESS format.</span></span>

<span data-ttu-id="5706e-148">Le UAV lié à cette ressource doit avoir été créé avec l' [**\_ indicateur UAV de mémoire tampon d3d11 \_ \_ \_ RAW**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).</span><span class="sxs-lookup"><span data-stu-id="5706e-148">The UAV bound to this resource must have been created with the [**D3D11\_BUFFER\_UAV\_FLAG\_RAW**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).</span></span>

<span data-ttu-id="5706e-149">Vous pouvez utiliser le type d’objet **RWByteAddressBuffer** quand vous travaillez avec des mémoires tampons brutes.</span><span class="sxs-lookup"><span data-stu-id="5706e-149">You can use the **RWByteAddressBuffer** object type when you work with raw buffers.</span></span> <span data-ttu-id="5706e-150">Pour plus d’informations sur l’affichage brut des tampons, consultez [affichages bruts de mémoires tampons](/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro).</span><span class="sxs-lookup"><span data-stu-id="5706e-150">For more info about raw viewing of buffers, see [Raw Views of Buffers](/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="5706e-151">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="5706e-151">Minimum Shader Model</span></span>

<span data-ttu-id="5706e-152">Cet objet est pris en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="5706e-152">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="5706e-153">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="5706e-153">Shader Model</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | <span data-ttu-id="5706e-154">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="5706e-154">Supported</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="5706e-155">Nuanceur [modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur plus élevés [nuanceur de modèle 4](dx-graphics-hlsl-sm4.md) (disponible par le biais de l’API Direct3D 11 en utilisant le niveau de fonctionnalité 10,0 ou 10,1 ([**\_ \_ niveau de fonctionnalité D3D**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) \_ 10 \_ X) sur les appareils qui prennent en charge les nuanceurs de calcul.</span><span class="sxs-lookup"><span data-stu-id="5706e-155">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models [Shader Model 4](dx-graphics-hlsl-sm4.md) (Available through the Direct3D 11 API by using 10.0 or 10.1 feature level ([**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)\_10\_X) on devices that support compute shaders.</span></span> <span data-ttu-id="5706e-156">Pour plus d’informations sur la prise en charge du nuanceur de calcul sur du matériel de niveau inférieur, consultez [nuanceurs de calcul sur du matériel de niveau inférieur](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).)</span><span class="sxs-lookup"><span data-stu-id="5706e-156">For more information about compute shader support on downlevel hardware, see [Compute Shaders on Downlevel Hardware](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).)</span></span><br/> | <span data-ttu-id="5706e-157">Oui</span><span class="sxs-lookup"><span data-stu-id="5706e-157">yes</span></span>       |



 

<span data-ttu-id="5706e-158">Cet objet est pris en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="5706e-158">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="5706e-159">Sommet</span><span class="sxs-lookup"><span data-stu-id="5706e-159">Vertex</span></span> | <span data-ttu-id="5706e-160">Forme</span><span class="sxs-lookup"><span data-stu-id="5706e-160">Hull</span></span> | <span data-ttu-id="5706e-161">Domain</span><span class="sxs-lookup"><span data-stu-id="5706e-161">Domain</span></span> | <span data-ttu-id="5706e-162">Géométrie</span><span class="sxs-lookup"><span data-stu-id="5706e-162">Geometry</span></span> | <span data-ttu-id="5706e-163">Pixel</span><span class="sxs-lookup"><span data-stu-id="5706e-163">Pixel</span></span> | <span data-ttu-id="5706e-164">Compute</span><span class="sxs-lookup"><span data-stu-id="5706e-164">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="5706e-165">x</span><span class="sxs-lookup"><span data-stu-id="5706e-165">x</span></span>     | <span data-ttu-id="5706e-166">x</span><span class="sxs-lookup"><span data-stu-id="5706e-166">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="5706e-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5706e-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5706e-168">Objets Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="5706e-168">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

