---
title: RWStructuredBuffer
description: Mémoire tampon de lecture/écriture qui peut accepter un type T qui est une structure.
ms.assetid: 8dd93b81-135d-4f28-898f-38510dc39af1
keywords:
- HLSL RWStructuredBuffer
topic_type:
- apiref
api_name:
- RWStructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f921ca795e761522828de14ede61894defe44f6e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382136"
---
# <a name="rwstructuredbuffer"></a><span data-ttu-id="1690d-104">RWStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="1690d-104">RWStructuredBuffer</span></span>

<span data-ttu-id="1690d-105">Mémoire tampon de lecture/écriture qui peut accepter un type T qui est une structure.</span><span class="sxs-lookup"><span data-stu-id="1690d-105">A read/write buffer that can take a T type that is a structure.</span></span>



| <span data-ttu-id="1690d-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="1690d-106">Method</span></span>                                                                     | <span data-ttu-id="1690d-107">Description</span><span class="sxs-lookup"><span data-stu-id="1690d-107">Description</span></span>                             |
|----------------------------------------------------------------------------|-----------------------------------------|
| [<span data-ttu-id="1690d-108">**DecrementCounter**</span><span class="sxs-lookup"><span data-stu-id="1690d-108">**DecrementCounter**</span></span>](sm5-object-rwstructuredbuffer-decrementcounter.md) | <span data-ttu-id="1690d-109">Décrémente le compteur masqué de l’objet.</span><span class="sxs-lookup"><span data-stu-id="1690d-109">Decrements the object's hidden counter.</span></span> |
| [<span data-ttu-id="1690d-110">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="1690d-110">**GetDimensions**</span></span>](sm5-object-rwstructuredbuffer-getdimensions.md)       | <span data-ttu-id="1690d-111">Obtient les dimensions de ressource.</span><span class="sxs-lookup"><span data-stu-id="1690d-111">Gets the resource dimensions.</span></span>           |
| [<span data-ttu-id="1690d-112">**IncrementCounter**</span><span class="sxs-lookup"><span data-stu-id="1690d-112">**IncrementCounter**</span></span>](sm5-object-rwstructuredbuffer-incrementcounter.md) | <span data-ttu-id="1690d-113">Incrémente le compteur masqué de l’objet.</span><span class="sxs-lookup"><span data-stu-id="1690d-113">Increments the object's hidden counter.</span></span> |
| [<span data-ttu-id="1690d-114">**Load**</span><span class="sxs-lookup"><span data-stu-id="1690d-114">**Load**</span></span>](rwstructuredbuffer-load.md)                                    | <span data-ttu-id="1690d-115">Lit les données de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="1690d-115">Reads buffer data.</span></span>                      |
| <span data-ttu-id="1690d-116">[**Opérateur\[\]**](sm5-object-rwstructuredbuffer-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="1690d-116">[**Operator\[\]**](sm5-object-rwstructuredbuffer-operatorindex.md)</span></span>        | <span data-ttu-id="1690d-117">Retourne une variable de ressource.</span><span class="sxs-lookup"><span data-stu-id="1690d-117">Returns a resource variable.</span></span>            |



 

<span data-ttu-id="1690d-118">Une variable de ressource peut également être passée dans une opération non ordonnée ou verrouillée.</span><span class="sxs-lookup"><span data-stu-id="1690d-118">A resource variable can also be passed into any unordered or interlocked operation.</span></span>

<span data-ttu-id="1690d-119">Les objets RWStructuredBuffer peuvent être précédés de la classe de stockage **globallycoherent**.</span><span class="sxs-lookup"><span data-stu-id="1690d-119">RWStructuredBuffer objects can be prefixed with the storage class **globallycoherent**.</span></span> <span data-ttu-id="1690d-120">Cette classe de stockage entraîne des barrières et des synchronisations de la mémoire pour vider les données sur l’ensemble du GPU, de telle sorte que les autres groupes puissent voir les écritures.</span><span class="sxs-lookup"><span data-stu-id="1690d-120">This storage class causes memory barriers and syncs to flush data across the entire GPU such that other groups can see writes.</span></span> <span data-ttu-id="1690d-121">Sans ce spécificateur, une barrière de mémoire ou une synchronisation vide uniquement un UAV dans le groupe actuel.</span><span class="sxs-lookup"><span data-stu-id="1690d-121">Without this specifier, a memory barrier or sync will only flush a UAV within the current group.</span></span>

<span data-ttu-id="1690d-122">Le format UAV lié à cette ressource doit être créé avec le format DXGI \_ \_ inconnu.</span><span class="sxs-lookup"><span data-stu-id="1690d-122">The UAV format bound to this resource needs to be created with the DXGI\_FORMAT\_UNKNOWN format.</span></span>

<span data-ttu-id="1690d-123">Pour en savoir plus sur les [mémoires tampons structurées](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources), consultez la documentation de présentation.</span><span class="sxs-lookup"><span data-stu-id="1690d-123">To find out more about [structured buffers](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources), see the overview material.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="1690d-124">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="1690d-124">Minimum Shader Model</span></span>

<span data-ttu-id="1690d-125">Cet objet est pris en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="1690d-125">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="1690d-126">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="1690d-126">Shader Model</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | <span data-ttu-id="1690d-127">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="1690d-127">Supported</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="1690d-128">Nuanceur [modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur plus élevés [nuanceur de modèle 4](dx-graphics-hlsl-sm4.md) (disponible par le biais de l’API Direct3D 11 en utilisant le niveau de fonctionnalité 10,0 ou 10,1 ([**\_ \_ niveau de fonctionnalité D3D**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) \_ 10 \_ X) sur les appareils qui prennent en charge les nuanceurs de calcul.</span><span class="sxs-lookup"><span data-stu-id="1690d-128">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models [Shader Model 4](dx-graphics-hlsl-sm4.md) (Available through the Direct3D 11 API by using 10.0 or 10.1 feature level ([**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)\_10\_X) on devices that support compute shaders.</span></span> <span data-ttu-id="1690d-129">Pour plus d’informations sur la prise en charge du nuanceur de calcul sur du matériel de niveau inférieur, consultez [nuanceurs de calcul sur du matériel de niveau inférieur](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).)</span><span class="sxs-lookup"><span data-stu-id="1690d-129">For more information about compute shader support on downlevel hardware, see [Compute Shaders on Downlevel Hardware](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).)</span></span><br/> | <span data-ttu-id="1690d-130">Oui</span><span class="sxs-lookup"><span data-stu-id="1690d-130">yes</span></span>       |



 

<span data-ttu-id="1690d-131">Cet objet est pris en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="1690d-131">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="1690d-132">Sommet</span><span class="sxs-lookup"><span data-stu-id="1690d-132">Vertex</span></span> | <span data-ttu-id="1690d-133">Forme</span><span class="sxs-lookup"><span data-stu-id="1690d-133">Hull</span></span> | <span data-ttu-id="1690d-134">Domain</span><span class="sxs-lookup"><span data-stu-id="1690d-134">Domain</span></span> | <span data-ttu-id="1690d-135">Géométrie</span><span class="sxs-lookup"><span data-stu-id="1690d-135">Geometry</span></span> | <span data-ttu-id="1690d-136">Pixel</span><span class="sxs-lookup"><span data-stu-id="1690d-136">Pixel</span></span> | <span data-ttu-id="1690d-137">Compute</span><span class="sxs-lookup"><span data-stu-id="1690d-137">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="1690d-138">x</span><span class="sxs-lookup"><span data-stu-id="1690d-138">x</span></span>     | <span data-ttu-id="1690d-139">x</span><span class="sxs-lookup"><span data-stu-id="1690d-139">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="1690d-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1690d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1690d-141">Objets Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="1690d-141">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

