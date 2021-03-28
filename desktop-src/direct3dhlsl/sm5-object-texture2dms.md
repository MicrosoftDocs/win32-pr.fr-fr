---
title: Texture2DMS
description: Type Texture2DMS (tel qu’il existe dans Shader Model 4) et variables de ressource.
ms.assetid: afda7324-680e-432a-a445-d90bd708e5e0
keywords:
- HLSL Texture2DMS
topic_type:
- apiref
api_name:
- Texture2DMS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c16c69a4fa0fd35ce7b12d69f880daa4b8345d02
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030120"
---
# <a name="texture2dms"></a><span data-ttu-id="c56a8-104">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="c56a8-104">Texture2DMS</span></span>

<span data-ttu-id="c56a8-105">Type Texture2DMS (tel qu’il existe dans Shader Model 4) et variables de ressource.</span><span class="sxs-lookup"><span data-stu-id="c56a8-105">Texture2DMS type (as it exists in Shader Model 4) plus resource variables.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c56a8-106">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="c56a8-106">In this section</span></span>



| <span data-ttu-id="c56a8-107">Rubrique</span><span class="sxs-lookup"><span data-stu-id="c56a8-107">Topic</span></span>                                                                                    | <span data-ttu-id="c56a8-108">Description</span><span class="sxs-lookup"><span data-stu-id="c56a8-108">Description</span></span>                                                                                 |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c56a8-109">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="c56a8-109">**GetDimensions**</span></span>](sm5-object-texture2dms-getdimensions.md)<br/>                 | <span data-ttu-id="c56a8-110">Retourne les dimensions de la ressource.</span><span class="sxs-lookup"><span data-stu-id="c56a8-110">Returns the dimensions of the resource.</span></span><br/>                                          |
| [<span data-ttu-id="c56a8-111">**GetSamplePosition**</span><span class="sxs-lookup"><span data-stu-id="c56a8-111">**GetSamplePosition**</span></span>](sm5-object-texture2dms-getsampleposition.md)<br/>         | <span data-ttu-id="c56a8-112">Retourne la position d’échantillon pour l’exemple d’index fourni.</span><span class="sxs-lookup"><span data-stu-id="c56a8-112">Returns the sample position for the sample index provided.</span></span><br/>                       |
| [<span data-ttu-id="c56a8-113">**Méthodes Load**</span><span class="sxs-lookup"><span data-stu-id="c56a8-113">**Load methods**</span></span>](texture2dms-load.md)<br/>                                      | <span data-ttu-id="c56a8-114">Récupère une valeur de la ressource à l’emplacement et l’exemple d’index fournis.</span><span class="sxs-lookup"><span data-stu-id="c56a8-114">Retrieves a value from the resource at the location and sample index provided.</span></span><br/>   |
| <span data-ttu-id="c56a8-115">[**exemple. And\[\]\[\]**](sm5-object-texture2dms-sampleoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="c56a8-115">[**sample.Operator\[\]\[\]**](sm5-object-texture2dms-sampleoperatorindex.md)</span></span><br/> | <span data-ttu-id="c56a8-116">Récupère une valeur de la ressource à l’emplacement et l’exemple d’index fournis.</span><span class="sxs-lookup"><span data-stu-id="c56a8-116">Retrieves a value from the resource at the location and sample index provided.</span></span><br/>   |
| <span data-ttu-id="c56a8-117">[**Opérateur\[\]**](sm5-object-texture2dms-operator1.md)</span><span class="sxs-lookup"><span data-stu-id="c56a8-117">[**Operator\[\]**](sm5-object-texture2dms-operator1.md)</span></span><br/>                      | <span data-ttu-id="c56a8-118">Récupère une valeur de la ressource à l’emplacement fourni à l’exemple d’index 0.</span><span class="sxs-lookup"><span data-stu-id="c56a8-118">Retrieves a value from the resource at the location provided at sample index 0.</span></span> <br/> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c56a8-119">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="c56a8-119">Minimum Shader Model</span></span>

<span data-ttu-id="c56a8-120">Cet objet est pris en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="c56a8-120">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="c56a8-121">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="c56a8-121">Shader Model</span></span>              | <span data-ttu-id="c56a8-122">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="c56a8-122">Supported</span></span> |
|---------------------------|-----------|
| <span data-ttu-id="c56a8-123">Shader Model 4 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="c56a8-123">Shader model 4 and higher</span></span> | <span data-ttu-id="c56a8-124">Oui</span><span class="sxs-lookup"><span data-stu-id="c56a8-124">yes</span></span>       |



 

<span data-ttu-id="c56a8-125">Cet objet est pris en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="c56a8-125">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="c56a8-126">Sommet</span><span class="sxs-lookup"><span data-stu-id="c56a8-126">Vertex</span></span> | <span data-ttu-id="c56a8-127">Forme</span><span class="sxs-lookup"><span data-stu-id="c56a8-127">Hull</span></span> | <span data-ttu-id="c56a8-128">Domain</span><span class="sxs-lookup"><span data-stu-id="c56a8-128">Domain</span></span> | <span data-ttu-id="c56a8-129">Géométrie</span><span class="sxs-lookup"><span data-stu-id="c56a8-129">Geometry</span></span> | <span data-ttu-id="c56a8-130">Pixel</span><span class="sxs-lookup"><span data-stu-id="c56a8-130">Pixel</span></span> | <span data-ttu-id="c56a8-131">Compute</span><span class="sxs-lookup"><span data-stu-id="c56a8-131">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="c56a8-132">x</span><span class="sxs-lookup"><span data-stu-id="c56a8-132">x</span></span>      | <span data-ttu-id="c56a8-133">x</span><span class="sxs-lookup"><span data-stu-id="c56a8-133">x</span></span>    | <span data-ttu-id="c56a8-134">x</span><span class="sxs-lookup"><span data-stu-id="c56a8-134">x</span></span>      | <span data-ttu-id="c56a8-135">x</span><span class="sxs-lookup"><span data-stu-id="c56a8-135">x</span></span>        | <span data-ttu-id="c56a8-136">x</span><span class="sxs-lookup"><span data-stu-id="c56a8-136">x</span></span>     | <span data-ttu-id="c56a8-137">x</span><span class="sxs-lookup"><span data-stu-id="c56a8-137">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="c56a8-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c56a8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c56a8-139">Objets Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="c56a8-139">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 





