---
title: Texture2DMSArray
description: Texture2DMSArray
ms.assetid: 4200eba8-a9e5-41ba-b04c-4ac7b20274d2
keywords:
- HLSL Texture2DMSArray
topic_type:
- apiref
api_name:
- Texture2DMSArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: effe4819c674a7909cc445b9e9f7b5322fae7676
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/14/2021
ms.locfileid: "104211206"
---
# <a name="texture2dmsarray"></a><span data-ttu-id="8cf16-104">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="8cf16-104">Texture2DMSArray</span></span>

<span data-ttu-id="8cf16-105">Type Texture2DMSArray (tel qu’il existe dans Shader Model 4) et variables de ressource.</span><span class="sxs-lookup"><span data-stu-id="8cf16-105">Texture2DMSArray type (as it exists in Shader Model 4) plus resource variables.</span></span>



| <span data-ttu-id="8cf16-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="8cf16-106">Method</span></span>                                                                             | <span data-ttu-id="8cf16-107">Description</span><span class="sxs-lookup"><span data-stu-id="8cf16-107">Description</span></span>                                        |
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="8cf16-108">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="8cf16-108">**GetDimensions**</span></span>](sm5-object-texture2dmsarray-getdimensions.md)                  | <span data-ttu-id="8cf16-109">Obtient les dimensions de ressource.</span><span class="sxs-lookup"><span data-stu-id="8cf16-109">Gets the resource dimensions.</span></span>                      |
| [<span data-ttu-id="8cf16-110">**GetSamplePosition**</span><span class="sxs-lookup"><span data-stu-id="8cf16-110">**GetSamplePosition**</span></span>](sm5-object-texture2dmsarray-getsampleposition.md)          | <span data-ttu-id="8cf16-111">Obtient la position de l’échantillon spécifié.</span><span class="sxs-lookup"><span data-stu-id="8cf16-111">Gets the position of the specified sample.</span></span>         |
| [<span data-ttu-id="8cf16-112">**Load**</span><span class="sxs-lookup"><span data-stu-id="8cf16-112">**Load**</span></span>](texture2dmsarray-load.md)                                               | <span data-ttu-id="8cf16-113">Obtient une valeur.</span><span class="sxs-lookup"><span data-stu-id="8cf16-113">Gets one value.</span></span>                                    |
| <span data-ttu-id="8cf16-114">[**exemple. And\[\]\[\]**](sm5-object-texture2dmsarray-sampleoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="8cf16-114">[**sample.Operator\[\]\[\]**](sm5-object-texture2dmsarray-sampleoperatorindex.md)</span></span>  | <span data-ttu-id="8cf16-115">Obtient une variable de ressource en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="8cf16-115">Gets a read-only resource variable.</span></span>                |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8cf16-116">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="8cf16-116">Minimum Shader Model</span></span>

<span data-ttu-id="8cf16-117">Cet objet est pris en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="8cf16-117">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="8cf16-118">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="8cf16-118">Shader Model</span></span>                                                                | <span data-ttu-id="8cf16-119">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="8cf16-119">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="8cf16-120">[Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="8cf16-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="8cf16-121">Oui</span><span class="sxs-lookup"><span data-stu-id="8cf16-121">yes</span></span>       |



 

<span data-ttu-id="8cf16-122">Cet objet est pris en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="8cf16-122">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="8cf16-123">Sommet</span><span class="sxs-lookup"><span data-stu-id="8cf16-123">Vertex</span></span> | <span data-ttu-id="8cf16-124">Forme</span><span class="sxs-lookup"><span data-stu-id="8cf16-124">Hull</span></span> | <span data-ttu-id="8cf16-125">Domain</span><span class="sxs-lookup"><span data-stu-id="8cf16-125">Domain</span></span> | <span data-ttu-id="8cf16-126">Géométrie</span><span class="sxs-lookup"><span data-stu-id="8cf16-126">Geometry</span></span> | <span data-ttu-id="8cf16-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="8cf16-127">Pixel</span></span> | <span data-ttu-id="8cf16-128">Compute</span><span class="sxs-lookup"><span data-stu-id="8cf16-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="8cf16-129">x</span><span class="sxs-lookup"><span data-stu-id="8cf16-129">x</span></span>      | <span data-ttu-id="8cf16-130">x</span><span class="sxs-lookup"><span data-stu-id="8cf16-130">x</span></span>    | <span data-ttu-id="8cf16-131">x</span><span class="sxs-lookup"><span data-stu-id="8cf16-131">x</span></span>      | <span data-ttu-id="8cf16-132">x</span><span class="sxs-lookup"><span data-stu-id="8cf16-132">x</span></span>        | <span data-ttu-id="8cf16-133">x</span><span class="sxs-lookup"><span data-stu-id="8cf16-133">x</span></span>     | <span data-ttu-id="8cf16-134">x</span><span class="sxs-lookup"><span data-stu-id="8cf16-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="8cf16-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8cf16-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cf16-136">Objets Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="8cf16-136">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




