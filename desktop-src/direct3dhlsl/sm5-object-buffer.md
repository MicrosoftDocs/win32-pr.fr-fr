---
title: Buffer
description: Buffer
ms.assetid: 7f552b9b-c5fb-4bc2-a7ae-61983379db38
keywords:
- Buffer HLSL
topic_type:
- apiref
api_name:
- Buffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce1754272fd90cedc5a806543dd83a99cdcd9455
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104380883"
---
# <a name="buffer"></a><span data-ttu-id="15fed-104">Buffer</span><span class="sxs-lookup"><span data-stu-id="15fed-104">Buffer</span></span>

<span data-ttu-id="15fed-105">Type de mémoire tampon tel qu’il existe dans le nuanceur modèle 4, ainsi que les variables de ressource et les informations de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="15fed-105">Buffer type as it exists in Shader Model 4 plus resource variables and buffer info.</span></span>



| <span data-ttu-id="15fed-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="15fed-106">Method</span></span>                                                   | <span data-ttu-id="15fed-107">Description</span><span class="sxs-lookup"><span data-stu-id="15fed-107">Description</span></span>                         |
|----------------------------------------------------------|-------------------------------------|
| [<span data-ttu-id="15fed-108">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="15fed-108">**GetDimensions**</span></span>](sm5-object-buffer-getdimensions.md) | <span data-ttu-id="15fed-109">Obtient les dimensions de ressource.</span><span class="sxs-lookup"><span data-stu-id="15fed-109">Gets the resource dimensions.</span></span>       |
| [<span data-ttu-id="15fed-110">**Load**</span><span class="sxs-lookup"><span data-stu-id="15fed-110">**Load**</span></span>](buffer-load.md)                              | <span data-ttu-id="15fed-111">Lit les données de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="15fed-111">Reads buffer data.</span></span>                  |
| <span data-ttu-id="15fed-112">[**Opérateur\[\]**](sm5-object-buffer-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="15fed-112">[**Operator\[\]**](sm5-object-buffer-operatorindex.md)</span></span>  | <span data-ttu-id="15fed-113">Obtient une variable de ressource en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="15fed-113">Gets a read-only resource variable.</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="15fed-114">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="15fed-114">Minimum Shader Model</span></span>

<span data-ttu-id="15fed-115">Cet objet est pris en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="15fed-115">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="15fed-116">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="15fed-116">Shader Model</span></span>                                                                | <span data-ttu-id="15fed-117">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="15fed-117">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="15fed-118">[Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="15fed-118">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="15fed-119">Oui</span><span class="sxs-lookup"><span data-stu-id="15fed-119">yes</span></span>       |



 

<span data-ttu-id="15fed-120">Cet objet est pris en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="15fed-120">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="15fed-121">Sommet</span><span class="sxs-lookup"><span data-stu-id="15fed-121">Vertex</span></span> | <span data-ttu-id="15fed-122">Forme</span><span class="sxs-lookup"><span data-stu-id="15fed-122">Hull</span></span> | <span data-ttu-id="15fed-123">Domain</span><span class="sxs-lookup"><span data-stu-id="15fed-123">Domain</span></span> | <span data-ttu-id="15fed-124">Géométrie</span><span class="sxs-lookup"><span data-stu-id="15fed-124">Geometry</span></span> | <span data-ttu-id="15fed-125">Pixel</span><span class="sxs-lookup"><span data-stu-id="15fed-125">Pixel</span></span> | <span data-ttu-id="15fed-126">Compute</span><span class="sxs-lookup"><span data-stu-id="15fed-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="15fed-127">x</span><span class="sxs-lookup"><span data-stu-id="15fed-127">x</span></span>      | <span data-ttu-id="15fed-128">x</span><span class="sxs-lookup"><span data-stu-id="15fed-128">x</span></span>    | <span data-ttu-id="15fed-129">x</span><span class="sxs-lookup"><span data-stu-id="15fed-129">x</span></span>      | <span data-ttu-id="15fed-130">x</span><span class="sxs-lookup"><span data-stu-id="15fed-130">x</span></span>        | <span data-ttu-id="15fed-131">x</span><span class="sxs-lookup"><span data-stu-id="15fed-131">x</span></span>     | <span data-ttu-id="15fed-132">x</span><span class="sxs-lookup"><span data-stu-id="15fed-132">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="15fed-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15fed-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15fed-134">Objets Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="15fed-134">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




