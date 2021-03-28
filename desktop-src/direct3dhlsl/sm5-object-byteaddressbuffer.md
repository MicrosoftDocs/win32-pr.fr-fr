---
title: ByteAddressBuffer
description: ByteAddressBuffer
ms.assetid: 809b5ee8-0a25-402e-8cf2-f5e7a8094ec6
keywords:
- HLSL ByteAddressBuffer
topic_type:
- apiref
api_name:
- ByteAddressBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 03e89f56522d941db4447b33b55cbedc7c73303f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971786"
---
# <a name="byteaddressbuffer"></a><span data-ttu-id="464d0-104">ByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="464d0-104">ByteAddressBuffer</span></span>

<span data-ttu-id="464d0-105">Mémoire tampon en lecture seule indexée en octets.</span><span class="sxs-lookup"><span data-stu-id="464d0-105">A read-only buffer that is indexed in bytes.</span></span>



| <span data-ttu-id="464d0-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="464d0-106">Method</span></span>                                                              | <span data-ttu-id="464d0-107">Description</span><span class="sxs-lookup"><span data-stu-id="464d0-107">Description</span></span>                   |
|---------------------------------------------------------------------|-------------------------------|
| [<span data-ttu-id="464d0-108">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="464d0-108">**GetDimensions**</span></span>](sm5-object-byteaddressbuffer-getdimensions.md) | <span data-ttu-id="464d0-109">Obtient les dimensions de ressource.</span><span class="sxs-lookup"><span data-stu-id="464d0-109">Gets the resource dimensions.</span></span> |
| [<span data-ttu-id="464d0-110">**Load**</span><span class="sxs-lookup"><span data-stu-id="464d0-110">**Load**</span></span>](byteaddressbuffer-load.md)                              | <span data-ttu-id="464d0-111">Obtient une valeur.</span><span class="sxs-lookup"><span data-stu-id="464d0-111">Gets one value.</span></span>               |
| [<span data-ttu-id="464d0-112">**Load2**</span><span class="sxs-lookup"><span data-stu-id="464d0-112">**Load2**</span></span>](byteaddressbuffer-load2.md)                            | <span data-ttu-id="464d0-113">Obtient deux valeurs.</span><span class="sxs-lookup"><span data-stu-id="464d0-113">Gets two values.</span></span>              |
| [<span data-ttu-id="464d0-114">**Load3**</span><span class="sxs-lookup"><span data-stu-id="464d0-114">**Load3**</span></span>](byteaddressbuffer-load3.md)                            | <span data-ttu-id="464d0-115">Obtient trois valeurs.</span><span class="sxs-lookup"><span data-stu-id="464d0-115">Gets three values.</span></span>            |
| [<span data-ttu-id="464d0-116">**Load4**</span><span class="sxs-lookup"><span data-stu-id="464d0-116">**Load4**</span></span>](byteaddressbuffer-load4.md)                            | <span data-ttu-id="464d0-117">Obtient quatre valeurs.</span><span class="sxs-lookup"><span data-stu-id="464d0-117">Gets four values.</span></span>             |



 

<span data-ttu-id="464d0-118">Vous pouvez utiliser le type d’objet **ByteAddressBuffer** quand vous travaillez avec des mémoires tampons brutes.</span><span class="sxs-lookup"><span data-stu-id="464d0-118">You can use the **ByteAddressBuffer** object type when you work with raw buffers.</span></span> <span data-ttu-id="464d0-119">Pour plus d’informations sur l’affichage brut des tampons, consultez [affichages bruts de mémoires tampons](/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro).</span><span class="sxs-lookup"><span data-stu-id="464d0-119">For more info about raw viewing of buffers, see [Raw Views of Buffers](/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="464d0-120">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="464d0-120">Minimum Shader Model</span></span>

<span data-ttu-id="464d0-121">Cet objet est pris en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="464d0-121">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="464d0-122">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="464d0-122">Shader Model</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | <span data-ttu-id="464d0-123">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="464d0-123">Supported</span></span> |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="464d0-124">Nuanceur [modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur plus élevés [nuanceur de modèle 4](dx-graphics-hlsl-sm4.md) (disponible par le biais de l’API Direct3D 11 en utilisant le niveau de fonctionnalité 10,0 ou 10,1 ([**\_ \_ niveau de fonctionnalité D3D**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) \_ 10 \_ X) sur les appareils qui prennent en charge les nuanceurs de calcul.</span><span class="sxs-lookup"><span data-stu-id="464d0-124">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models [Shader Model 4](dx-graphics-hlsl-sm4.md) (Available through the Direct3D 11 API by using 10.0 or 10.1 feature level ([**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)\_10\_X) on devices that support compute shaders.</span></span> <span data-ttu-id="464d0-125">Pour plus d’informations sur la prise en charge du nuanceur de calcul sur du matériel de niveau inférieur, consultez [nuanceurs de calcul sur du matériel de niveau inférieur](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).)</span><span class="sxs-lookup"><span data-stu-id="464d0-125">For more info about compute shader support on downlevel hardware, see [Compute Shaders on Downlevel Hardware](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).)</span></span><br/> | <span data-ttu-id="464d0-126">Oui</span><span class="sxs-lookup"><span data-stu-id="464d0-126">yes</span></span>       |



 

<span data-ttu-id="464d0-127">Cet objet est pris en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="464d0-127">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="464d0-128">Sommet</span><span class="sxs-lookup"><span data-stu-id="464d0-128">Vertex</span></span> | <span data-ttu-id="464d0-129">Forme</span><span class="sxs-lookup"><span data-stu-id="464d0-129">Hull</span></span> | <span data-ttu-id="464d0-130">Domain</span><span class="sxs-lookup"><span data-stu-id="464d0-130">Domain</span></span> | <span data-ttu-id="464d0-131">Géométrie</span><span class="sxs-lookup"><span data-stu-id="464d0-131">Geometry</span></span> | <span data-ttu-id="464d0-132">Pixel</span><span class="sxs-lookup"><span data-stu-id="464d0-132">Pixel</span></span> | <span data-ttu-id="464d0-133">Compute</span><span class="sxs-lookup"><span data-stu-id="464d0-133">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="464d0-134">x</span><span class="sxs-lookup"><span data-stu-id="464d0-134">x</span></span>      | <span data-ttu-id="464d0-135">x</span><span class="sxs-lookup"><span data-stu-id="464d0-135">x</span></span>    | <span data-ttu-id="464d0-136">x</span><span class="sxs-lookup"><span data-stu-id="464d0-136">x</span></span>      | <span data-ttu-id="464d0-137">x</span><span class="sxs-lookup"><span data-stu-id="464d0-137">x</span></span>        | <span data-ttu-id="464d0-138">x</span><span class="sxs-lookup"><span data-stu-id="464d0-138">x</span></span>     | <span data-ttu-id="464d0-139">x</span><span class="sxs-lookup"><span data-stu-id="464d0-139">x</span></span>       |



 

<span data-ttu-id="464d0-140">Pour plus d’informations sur une mémoire tampon d’adresse en octets, consultez le [type de ressource adressable en octets](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).</span><span class="sxs-lookup"><span data-stu-id="464d0-140">For more info about a byte address buffer, see the [byte addressable resource type](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).</span></span>

<span data-ttu-id="464d0-141">Le Shader Model 5 implémente également une [mémoire tampon d’adresse d’octets en lecture-écriture](sm5-object-rwbyteaddressbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="464d0-141">Shader Model 5 also implements a [read-write byte address buffer](sm5-object-rwbyteaddressbuffer.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="464d0-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="464d0-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="464d0-143">Objets Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="464d0-143">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

