---
title: ConsumeStructuredBuffer
description: Mémoire tampon d’entrée qui apparaît sous forme de flux à partir duquel le nuanceur peut extraire des valeurs. Seules les mémoires tampons structurées peuvent être des types de T qui sont des structures.
ms.assetid: 373bdd97-6186-4bce-99bf-738a153234f6
keywords:
- HLSL ConsumeStructuredBuffer
topic_type:
- apiref
api_name:
- ConsumeStructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: af7a670713dc5b63839702a04a632dda61ebfa43
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104991021"
---
# <a name="consumestructuredbuffer"></a><span data-ttu-id="c4317-105">ConsumeStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="c4317-105">ConsumeStructuredBuffer</span></span>

<span data-ttu-id="c4317-106">Mémoire tampon d’entrée qui apparaît sous forme de flux à partir duquel le nuanceur peut extraire des valeurs.</span><span class="sxs-lookup"><span data-stu-id="c4317-106">An input buffer that appears as a stream the shader may pull values from.</span></span> <span data-ttu-id="c4317-107">Seules les mémoires tampons structurées peuvent être des types de T qui sont des structures.</span><span class="sxs-lookup"><span data-stu-id="c4317-107">Only structured buffers can take T types that are structures.</span></span>



| <span data-ttu-id="c4317-108">Méthode</span><span class="sxs-lookup"><span data-stu-id="c4317-108">Method</span></span>                                                                    | <span data-ttu-id="c4317-109">Description</span><span class="sxs-lookup"><span data-stu-id="c4317-109">Description</span></span>                                 |
|---------------------------------------------------------------------------|---------------------------------------------|
| [<span data-ttu-id="c4317-110">**Utiliser**</span><span class="sxs-lookup"><span data-stu-id="c4317-110">**Consume**</span></span>](sm5-object-consumestructuredbuffer-consume.md)             | <span data-ttu-id="c4317-111">Supprime une valeur à partir de la fin de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="c4317-111">Removes a value from the end of the buffer.</span></span> |
| [<span data-ttu-id="c4317-112">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="c4317-112">**GetDimensions**</span></span>](sm5-object-consumestructuredbuffer-getdimensions.md) | <span data-ttu-id="c4317-113">Obtient les dimensions de ressource.</span><span class="sxs-lookup"><span data-stu-id="c4317-113">Gets the resource dimensions.</span></span>               |



 

<span data-ttu-id="c4317-114">Le format UAV lié à cette ressource doit être créé avec le format DXGI \_ \_ inconnu.</span><span class="sxs-lookup"><span data-stu-id="c4317-114">The UAV format bound to this resource needs to be created with the DXGI\_FORMAT\_UNKNOWN format.</span></span>

<span data-ttu-id="c4317-115">Le UAV lié à cette ressource doit avoir été créé avec l’ajout de l' [**\_ \_ \_ indicateur \_ UAV de tampon d3d11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).</span><span class="sxs-lookup"><span data-stu-id="c4317-115">The UAV bound to this resource must have been created with [**D3D11\_BUFFER\_UAV\_FLAG\_APPEND**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).</span></span>

<span data-ttu-id="c4317-116">Pour plus d’informations sur l’utilisation de mémoires tampons structurées, consultez les deux sections : [Append et consume](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) buffer et [Structured buffer](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).</span><span class="sxs-lookup"><span data-stu-id="c4317-116">For more info about consume structured buffers, see both sections: [append and consume buffer](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) and [structured buffer](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="c4317-117">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="c4317-117">Minimum Shader Model</span></span>

<span data-ttu-id="c4317-118">Cet objet est pris en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="c4317-118">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="c4317-119">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="c4317-119">Shader Model</span></span>                                                                | <span data-ttu-id="c4317-120">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="c4317-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="c4317-121">[Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="c4317-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="c4317-122">Oui</span><span class="sxs-lookup"><span data-stu-id="c4317-122">yes</span></span>       |



 

<span data-ttu-id="c4317-123">Cet objet est pris en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="c4317-123">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="c4317-124">Sommet</span><span class="sxs-lookup"><span data-stu-id="c4317-124">Vertex</span></span> | <span data-ttu-id="c4317-125">Forme</span><span class="sxs-lookup"><span data-stu-id="c4317-125">Hull</span></span> | <span data-ttu-id="c4317-126">Domain</span><span class="sxs-lookup"><span data-stu-id="c4317-126">Domain</span></span> | <span data-ttu-id="c4317-127">Géométrie</span><span class="sxs-lookup"><span data-stu-id="c4317-127">Geometry</span></span> | <span data-ttu-id="c4317-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="c4317-128">Pixel</span></span> | <span data-ttu-id="c4317-129">Compute</span><span class="sxs-lookup"><span data-stu-id="c4317-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="c4317-130">x</span><span class="sxs-lookup"><span data-stu-id="c4317-130">x</span></span>     | <span data-ttu-id="c4317-131">x</span><span class="sxs-lookup"><span data-stu-id="c4317-131">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="c4317-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4317-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4317-133">Objets Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="c4317-133">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 