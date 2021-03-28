---
title: StructuredBuffer
description: Mémoire tampon en lecture seule, qui peut accepter un type T qui est une structure.
ms.assetid: fe2ec0b8-0e19-42b6-9dad-c992ecdeb19e
keywords:
- HLSL StructuredBuffer
topic_type:
- apiref
api_name:
- StructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 524078780ac28d691c4999491bed146a04d34439
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990928"
---
# <a name="structuredbuffer"></a><span data-ttu-id="5de8e-104">StructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="5de8e-104">StructuredBuffer</span></span>

<span data-ttu-id="5de8e-105">Mémoire tampon en lecture seule, qui peut accepter un type T qui est une structure.</span><span class="sxs-lookup"><span data-stu-id="5de8e-105">A read-only buffer, which can take a T type that is a structure.</span></span>



| <span data-ttu-id="5de8e-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="5de8e-106">Method</span></span>                                                             | <span data-ttu-id="5de8e-107">Description</span><span class="sxs-lookup"><span data-stu-id="5de8e-107">Description</span></span>                            |
|--------------------------------------------------------------------|----------------------------------------|
| [<span data-ttu-id="5de8e-108">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="5de8e-108">**GetDimensions**</span></span>](sm5-object-structuredbuffer-getdimensions.md) | <span data-ttu-id="5de8e-109">Obtient les dimensions de ressource.</span><span class="sxs-lookup"><span data-stu-id="5de8e-109">Gets the resource dimensions.</span></span>          |
| [<span data-ttu-id="5de8e-110">**Load**</span><span class="sxs-lookup"><span data-stu-id="5de8e-110">**Load**</span></span>](structuredbuffer-load.md)                              | <span data-ttu-id="5de8e-111">Lit les données de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="5de8e-111">Reads buffer data.</span></span>                     |
| <span data-ttu-id="5de8e-112">[**Opérateur\[\]**](sm5-object-structuredbuffer-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="5de8e-112">[**Operator\[\]**](sm5-object-structuredbuffer-operatorindex.md)</span></span>  | <span data-ttu-id="5de8e-113">Retourne une variable de ressource en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="5de8e-113">Returns a read-only resource variable.</span></span> |



 

<span data-ttu-id="5de8e-114">Le format UAV lié à cette ressource doit être créé avec le format DXGI \_ \_ inconnu.</span><span class="sxs-lookup"><span data-stu-id="5de8e-114">The UAV format bound to this resource needs to be created with the DXGI\_FORMAT\_UNKNOWN format.</span></span>

<span data-ttu-id="5de8e-115">Pour en savoir plus sur les [mémoires tampons structurées](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources), consultez la documentation de présentation.</span><span class="sxs-lookup"><span data-stu-id="5de8e-115">To find out more about [structured buffers](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources), see the overview material.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="5de8e-116">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="5de8e-116">Minimum Shader Model</span></span>

<span data-ttu-id="5de8e-117">Cet objet est pris en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="5de8e-117">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="5de8e-118">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="5de8e-118">Shader Model</span></span>                                                                                                                                                                                                            | <span data-ttu-id="5de8e-119">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="5de8e-119">Supported</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="5de8e-120">Shader [Model 5](d3d11-graphics-reference-sm5.md) et versions supérieures nuanceur Model [Shader Model 4](dx-graphics-hlsl-sm4.md) (disponible pour les nuanceurs de calcul et de pixel dans Direct3D 11 sur certains périphériques Direct3D 10.)</span><span class="sxs-lookup"><span data-stu-id="5de8e-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models [Shader Model 4](dx-graphics-hlsl-sm4.md) (Available for compute and pixel shaders in Direct3D 11 on some Direct3D 10 devices.)</span></span><br/> | <span data-ttu-id="5de8e-121">Oui</span><span class="sxs-lookup"><span data-stu-id="5de8e-121">yes</span></span>       |



 

<span data-ttu-id="5de8e-122">Cet objet est pris en charge pour les types de nuanceurs suivants.</span><span class="sxs-lookup"><span data-stu-id="5de8e-122">This object is supported for the following types of shaders.</span></span>



| <span data-ttu-id="5de8e-123">Sommet</span><span class="sxs-lookup"><span data-stu-id="5de8e-123">Vertex</span></span> | <span data-ttu-id="5de8e-124">Forme</span><span class="sxs-lookup"><span data-stu-id="5de8e-124">Hull</span></span> | <span data-ttu-id="5de8e-125">Domain</span><span class="sxs-lookup"><span data-stu-id="5de8e-125">Domain</span></span> | <span data-ttu-id="5de8e-126">Géométrie</span><span class="sxs-lookup"><span data-stu-id="5de8e-126">Geometry</span></span> | <span data-ttu-id="5de8e-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="5de8e-127">Pixel</span></span> | <span data-ttu-id="5de8e-128">Compute</span><span class="sxs-lookup"><span data-stu-id="5de8e-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="5de8e-129">x</span><span class="sxs-lookup"><span data-stu-id="5de8e-129">x</span></span>      | <span data-ttu-id="5de8e-130">x</span><span class="sxs-lookup"><span data-stu-id="5de8e-130">x</span></span>    | <span data-ttu-id="5de8e-131">x</span><span class="sxs-lookup"><span data-stu-id="5de8e-131">x</span></span>      | <span data-ttu-id="5de8e-132">x</span><span class="sxs-lookup"><span data-stu-id="5de8e-132">x</span></span>        | <span data-ttu-id="5de8e-133">x</span><span class="sxs-lookup"><span data-stu-id="5de8e-133">x</span></span>     | <span data-ttu-id="5de8e-134">x</span><span class="sxs-lookup"><span data-stu-id="5de8e-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="5de8e-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5de8e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5de8e-136">Objets Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="5de8e-136">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

