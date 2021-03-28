---
title: InputPatch
description: Représente un tableau de points de contrôle qui sont disponibles pour le nuanceur de coque en tant qu’entrées.
ms.assetid: a2eeb45a-85b2-4ed0-b071-fcbb8abf4f2d
keywords:
- HLSL InputPatch
topic_type:
- apiref
api_name:
- InputPatch
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a882d032133ccb7bc98a34b3ef99551aa18fa51b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104990668"
---
# <a name="inputpatch"></a><span data-ttu-id="b70d1-104">InputPatch</span><span class="sxs-lookup"><span data-stu-id="b70d1-104">InputPatch</span></span>

<span data-ttu-id="b70d1-105">Représente un tableau de points de contrôle qui sont disponibles pour le nuanceur de coque en tant qu’entrées.</span><span class="sxs-lookup"><span data-stu-id="b70d1-105">Represents an array of control points that are available to the hull shader as inputs.</span></span>



| <span data-ttu-id="b70d1-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="b70d1-106">Method</span></span>                                                      | <span data-ttu-id="b70d1-107">Description</span><span class="sxs-lookup"><span data-stu-id="b70d1-107">Description</span></span>                         |
|-------------------------------------------------------------|-------------------------------------|
| <span data-ttu-id="b70d1-108">[**Opérateur\[\]**](sm5-object-inputpatch-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="b70d1-108">[**Operator\[\]**](sm5-object-inputpatch-operatorindex.md)</span></span> | <span data-ttu-id="b70d1-109">Obtient une variable de ressource en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b70d1-109">Gets a read-only resource variable.</span></span> |



 

<span data-ttu-id="b70d1-110">La classe InputPatch prend également en charge les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="b70d1-110">The InputPatch class also supports the following properties:</span></span>



| <span data-ttu-id="b70d1-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b70d1-111">Properties</span></span> | <span data-ttu-id="b70d1-112">Type</span><span class="sxs-lookup"><span data-stu-id="b70d1-112">Type</span></span> | <span data-ttu-id="b70d1-113">Description</span><span class="sxs-lookup"><span data-stu-id="b70d1-113">Description</span></span>                   |
|------------|------|-------------------------------|
| <span data-ttu-id="b70d1-114">Longueur</span><span class="sxs-lookup"><span data-stu-id="b70d1-114">Length</span></span>     | <span data-ttu-id="b70d1-115">uint</span><span class="sxs-lookup"><span data-stu-id="b70d1-115">uint</span></span> | <span data-ttu-id="b70d1-116">Nombre de points de contrôle.</span><span class="sxs-lookup"><span data-stu-id="b70d1-116">The number of control points.</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b70d1-117">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="b70d1-117">Minimum Shader Model</span></span>

<span data-ttu-id="b70d1-118">Cet objet est pris en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="b70d1-118">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="b70d1-119">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="b70d1-119">Shader Model</span></span>                                                                | <span data-ttu-id="b70d1-120">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="b70d1-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="b70d1-121">[Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="b70d1-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="b70d1-122">Oui</span><span class="sxs-lookup"><span data-stu-id="b70d1-122">yes</span></span>       |



 

<span data-ttu-id="b70d1-123">Cet objet est pris en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="b70d1-123">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="b70d1-124">Sommet</span><span class="sxs-lookup"><span data-stu-id="b70d1-124">Vertex</span></span> | <span data-ttu-id="b70d1-125">Forme</span><span class="sxs-lookup"><span data-stu-id="b70d1-125">Hull</span></span> | <span data-ttu-id="b70d1-126">Domain</span><span class="sxs-lookup"><span data-stu-id="b70d1-126">Domain</span></span> | <span data-ttu-id="b70d1-127">Géométrie</span><span class="sxs-lookup"><span data-stu-id="b70d1-127">Geometry</span></span> | <span data-ttu-id="b70d1-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="b70d1-128">Pixel</span></span> | <span data-ttu-id="b70d1-129">Compute</span><span class="sxs-lookup"><span data-stu-id="b70d1-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="b70d1-130">x</span><span class="sxs-lookup"><span data-stu-id="b70d1-130">x</span></span>    |        | <span data-ttu-id="b70d1-131">x</span><span class="sxs-lookup"><span data-stu-id="b70d1-131">x</span></span>        |       |         |



 

## <a name="see-also"></a><span data-ttu-id="b70d1-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b70d1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b70d1-133">Objets Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="b70d1-133">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




