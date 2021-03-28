---
title: OutputPatch
description: OutputPatch
ms.assetid: 24841938-6c84-4e1f-ba8a-a81b589bdd51
keywords:
- HLSL OutputPatch
topic_type:
- apiref
api_name:
- OutputPatch
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c77a30a2ff23bdc292d45df6514ef00fab53463
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030080"
---
# <a name="outputpatch"></a><span data-ttu-id="81b35-104">OutputPatch</span><span class="sxs-lookup"><span data-stu-id="81b35-104">OutputPatch</span></span>

<span data-ttu-id="81b35-105">Représente un tableau de points de contrôle de sortie qui sont disponibles pour la fonction de correction constante du nuanceur de coque, ainsi que le nuanceur de domaine.</span><span class="sxs-lookup"><span data-stu-id="81b35-105">Represents an array of output control points that are available to the hull shader's patch-constant function as well as the domain shader.</span></span>



| <span data-ttu-id="81b35-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="81b35-106">Method</span></span>                                                       | <span data-ttu-id="81b35-107">Description</span><span class="sxs-lookup"><span data-stu-id="81b35-107">Description</span></span>                         |
|--------------------------------------------------------------|-------------------------------------|
| <span data-ttu-id="81b35-108">[**Opérateur\[\]**](sm5-object-outputpatch-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="81b35-108">[**Operator\[\]**](sm5-object-outputpatch-operatorindex.md)</span></span> | <span data-ttu-id="81b35-109">Obtient une variable de ressource en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="81b35-109">Gets a read-only resource variable.</span></span> |



 

<span data-ttu-id="81b35-110">En outre, la classe InputPatch prend en charge les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="81b35-110">In addition, the InputPatch class supports the following properties:</span></span>



| <span data-ttu-id="81b35-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="81b35-111">Properties</span></span> | <span data-ttu-id="81b35-112">Type</span><span class="sxs-lookup"><span data-stu-id="81b35-112">Type</span></span> | <span data-ttu-id="81b35-113">Description</span><span class="sxs-lookup"><span data-stu-id="81b35-113">Description</span></span>                   |
|------------|------|-------------------------------|
| <span data-ttu-id="81b35-114">Longueur</span><span class="sxs-lookup"><span data-stu-id="81b35-114">Length</span></span>     | <span data-ttu-id="81b35-115">uint</span><span class="sxs-lookup"><span data-stu-id="81b35-115">uint</span></span> | <span data-ttu-id="81b35-116">Nombre de points de contrôle.</span><span class="sxs-lookup"><span data-stu-id="81b35-116">The number of control points.</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="81b35-117">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="81b35-117">Minimum Shader Model</span></span>

<span data-ttu-id="81b35-118">Cet objet est pris en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="81b35-118">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="81b35-119">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="81b35-119">Shader Model</span></span>                                                                | <span data-ttu-id="81b35-120">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="81b35-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="81b35-121">[Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="81b35-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="81b35-122">Oui</span><span class="sxs-lookup"><span data-stu-id="81b35-122">yes</span></span>       |



 

<span data-ttu-id="81b35-123">Cet objet est pris en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="81b35-123">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="81b35-124">Sommet</span><span class="sxs-lookup"><span data-stu-id="81b35-124">Vertex</span></span> | <span data-ttu-id="81b35-125">Forme</span><span class="sxs-lookup"><span data-stu-id="81b35-125">Hull</span></span> | <span data-ttu-id="81b35-126">Domain</span><span class="sxs-lookup"><span data-stu-id="81b35-126">Domain</span></span> | <span data-ttu-id="81b35-127">Géométrie</span><span class="sxs-lookup"><span data-stu-id="81b35-127">Geometry</span></span> | <span data-ttu-id="81b35-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="81b35-128">Pixel</span></span> | <span data-ttu-id="81b35-129">Compute</span><span class="sxs-lookup"><span data-stu-id="81b35-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="81b35-130">x</span><span class="sxs-lookup"><span data-stu-id="81b35-130">x</span></span>    | <span data-ttu-id="81b35-131">x</span><span class="sxs-lookup"><span data-stu-id="81b35-131">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="81b35-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81b35-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81b35-133">Objets Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="81b35-133">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




