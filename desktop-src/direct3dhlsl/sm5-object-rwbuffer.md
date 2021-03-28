---
title: RWBuffer
description: Mémoire tampon de lecture/écriture.
ms.assetid: e9b60e63-5b2b-4f45-834b-269e692ba84c
keywords:
- HLSL RWBuffer
topic_type:
- apiref
api_name:
- RWBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 765634da85fb74f2d3a3591bfe4767ccee1a80c8
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312559"
---
# <a name="rwbuffer"></a><span data-ttu-id="9346d-104">RWBuffer</span><span class="sxs-lookup"><span data-stu-id="9346d-104">RWBuffer</span></span>

<span data-ttu-id="9346d-105">Mémoire tampon de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="9346d-105">A read/write buffer.</span></span>



| <span data-ttu-id="9346d-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="9346d-106">Method</span></span>                                                     | <span data-ttu-id="9346d-107">Description</span><span class="sxs-lookup"><span data-stu-id="9346d-107">Description</span></span>                            |
|------------------------------------------------------------|----------------------------------------|
| [<span data-ttu-id="9346d-108">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="9346d-108">**GetDimensions**</span></span>](sm5-object-rwbuffer-getdimensions.md) | <span data-ttu-id="9346d-109">Obtient les dimensions de ressource.</span><span class="sxs-lookup"><span data-stu-id="9346d-109">Gets the resource dimensions.</span></span>          |
| [<span data-ttu-id="9346d-110">**Load**</span><span class="sxs-lookup"><span data-stu-id="9346d-110">**Load**</span></span>](rwbuffer-load.md)                              | <span data-ttu-id="9346d-111">Obtient une valeur dans un tampon en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="9346d-111">Gets one value in a read-write buffer.</span></span> |
| <span data-ttu-id="9346d-112">[**Opérateur\[\]**](sm5-object-rwbuffer-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="9346d-112">[**Operator\[\]**](sm5-object-rwbuffer-operatorindex.md)</span></span>  | <span data-ttu-id="9346d-113">Retourne une variable de ressource.</span><span class="sxs-lookup"><span data-stu-id="9346d-113">Returns a resource variable.</span></span>           |



 

<span data-ttu-id="9346d-114">Une variable de ressource peut également être passée dans une opération non ordonnée ou verrouillée.</span><span class="sxs-lookup"><span data-stu-id="9346d-114">A resource variable can also be passed into any unordered or interlocked operation.</span></span>

<span data-ttu-id="9346d-115">Les objets **RWBuffer** peuvent être précédés de la classe de stockage **globallycoherent**.</span><span class="sxs-lookup"><span data-stu-id="9346d-115">**RWBuffer** objects can be prefixed with the storage class **globallycoherent**.</span></span> <span data-ttu-id="9346d-116">Cette classe de stockage entraîne des barrières et des synchronisations de la mémoire pour vider les données sur l’ensemble du GPU, de telle sorte que les autres groupes puissent voir les écritures.</span><span class="sxs-lookup"><span data-stu-id="9346d-116">This storage class causes memory barriers and syncs to flush data across the entire GPU such that other groups can see writes.</span></span> <span data-ttu-id="9346d-117">Sans ce spécificateur, une barrière de mémoire ou une synchronisation vide un UAV uniquement dans le groupe actuel.</span><span class="sxs-lookup"><span data-stu-id="9346d-117">Without this specifier, a memory barrier or sync will flush a UAV only within the current group.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="9346d-118">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="9346d-118">Minimum Shader Model</span></span>

<span data-ttu-id="9346d-119">Cet objet est pris en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="9346d-119">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="9346d-120">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="9346d-120">Shader Model</span></span>                                                                | <span data-ttu-id="9346d-121">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="9346d-121">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="9346d-122">[Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="9346d-122">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="9346d-123">Oui</span><span class="sxs-lookup"><span data-stu-id="9346d-123">yes</span></span>       |



 

<span data-ttu-id="9346d-124">Cet objet est pris en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="9346d-124">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="9346d-125">Sommet</span><span class="sxs-lookup"><span data-stu-id="9346d-125">Vertex</span></span> | <span data-ttu-id="9346d-126">Forme</span><span class="sxs-lookup"><span data-stu-id="9346d-126">Hull</span></span> | <span data-ttu-id="9346d-127">Domain</span><span class="sxs-lookup"><span data-stu-id="9346d-127">Domain</span></span> | <span data-ttu-id="9346d-128">Géométrie</span><span class="sxs-lookup"><span data-stu-id="9346d-128">Geometry</span></span> | <span data-ttu-id="9346d-129">Pixel</span><span class="sxs-lookup"><span data-stu-id="9346d-129">Pixel</span></span> | <span data-ttu-id="9346d-130">Compute</span><span class="sxs-lookup"><span data-stu-id="9346d-130">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="9346d-131">x</span><span class="sxs-lookup"><span data-stu-id="9346d-131">x</span></span>     | <span data-ttu-id="9346d-132">x</span><span class="sxs-lookup"><span data-stu-id="9346d-132">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="9346d-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9346d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9346d-134">Objets Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="9346d-134">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




