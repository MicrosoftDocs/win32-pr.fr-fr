---
title: AllMemoryBarrierWithGroupSync fonction)
description: Bloque l’exécution de tous les threads dans un groupe jusqu’à ce que tous les accès à la mémoire aient été effectués et que tous les threads du groupe aient atteint cet appel.
ms.assetid: 831830e7-19ce-41d0-b555-44a083b67cdc
keywords:
- AllMemoryBarrierWithGroupSync fonction HLSL
topic_type:
- apiref
api_name:
- AllMemoryBarrierWithGroupSync
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1fc005545485b7f894729ab6c7d7975acfd5b6d4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030390"
---
# <a name="allmemorybarrierwithgroupsync-function"></a><span data-ttu-id="1ae23-104">AllMemoryBarrierWithGroupSync fonction)</span><span class="sxs-lookup"><span data-stu-id="1ae23-104">AllMemoryBarrierWithGroupSync function</span></span>

<span data-ttu-id="1ae23-105">Bloque l’exécution de tous les threads dans un groupe jusqu’à ce que tous les accès à la mémoire aient été effectués et que tous les threads du groupe aient atteint cet appel.</span><span class="sxs-lookup"><span data-stu-id="1ae23-105">Blocks execution of all threads in a group until all memory accesses have been completed and all threads in the group have reached this call.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ae23-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1ae23-106">Syntax</span></span>

``` syntax
void AllMemoryBarrierWithGroupSync(void);
```

## <a name="parameters"></a><span data-ttu-id="1ae23-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1ae23-107">Parameters</span></span>

<span data-ttu-id="1ae23-108">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="1ae23-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1ae23-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1ae23-109">Return value</span></span>

<span data-ttu-id="1ae23-110">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="1ae23-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ae23-111">Notes</span><span class="sxs-lookup"><span data-stu-id="1ae23-111">Remarks</span></span>

<span data-ttu-id="1ae23-112">Une barrière de mémoire garantit que les opérations de mémoire en suspens sont terminées.</span><span class="sxs-lookup"><span data-stu-id="1ae23-112">A memory barrier guarantees that outstanding memory operations have completed.</span></span> <span data-ttu-id="1ae23-113">Les threads sont synchronisés aux barrières GroupSync.</span><span class="sxs-lookup"><span data-stu-id="1ae23-113">Threads are synchronized at GroupSync barriers.</span></span> <span data-ttu-id="1ae23-114">Cela peut bloquer un ou des threads si les opérations de mémoire sont en cours.</span><span class="sxs-lookup"><span data-stu-id="1ae23-114">This may stall a thread or threads if memory operations are in progress.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="1ae23-115">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="1ae23-115">Minimum Shader Model</span></span>

<span data-ttu-id="1ae23-116">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="1ae23-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="1ae23-117">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="1ae23-117">Shader Model</span></span>                                                                | <span data-ttu-id="1ae23-118">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="1ae23-118">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="1ae23-119">[Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="1ae23-119">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="1ae23-120">Oui</span><span class="sxs-lookup"><span data-stu-id="1ae23-120">yes</span></span>       |



 

<span data-ttu-id="1ae23-121">Cette fonction est prise en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="1ae23-121">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="1ae23-122">Sommet</span><span class="sxs-lookup"><span data-stu-id="1ae23-122">Vertex</span></span> | <span data-ttu-id="1ae23-123">Forme</span><span class="sxs-lookup"><span data-stu-id="1ae23-123">Hull</span></span> | <span data-ttu-id="1ae23-124">Domain</span><span class="sxs-lookup"><span data-stu-id="1ae23-124">Domain</span></span> | <span data-ttu-id="1ae23-125">Géométrie</span><span class="sxs-lookup"><span data-stu-id="1ae23-125">Geometry</span></span> | <span data-ttu-id="1ae23-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="1ae23-126">Pixel</span></span> | <span data-ttu-id="1ae23-127">Compute</span><span class="sxs-lookup"><span data-stu-id="1ae23-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="1ae23-128">x</span><span class="sxs-lookup"><span data-stu-id="1ae23-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="1ae23-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ae23-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ae23-130">Fonctions intrinsèques</span><span class="sxs-lookup"><span data-stu-id="1ae23-130">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="1ae23-131">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="1ae23-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




