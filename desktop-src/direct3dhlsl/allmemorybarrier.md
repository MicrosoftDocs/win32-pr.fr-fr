---
title: AllMemoryBarrier fonction)
description: Bloque l’exécution de tous les threads dans un groupe jusqu’à ce que tous les accès à la mémoire aient été effectués.
ms.assetid: 63593de6-7b92-4f29-bcd9-21c69b9defcb
keywords:
- AllMemoryBarrier fonction HLSL
topic_type:
- apiref
api_name:
- AllMemoryBarrier
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3252389da64b74e07853069c71315b290a2ba6d5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104380957"
---
# <a name="allmemorybarrier-function"></a><span data-ttu-id="1f2e9-104">AllMemoryBarrier fonction)</span><span class="sxs-lookup"><span data-stu-id="1f2e9-104">AllMemoryBarrier function</span></span>

<span data-ttu-id="1f2e9-105">Bloque l’exécution de tous les threads dans un groupe jusqu’à ce que tous les accès à la mémoire aient été effectués.</span><span class="sxs-lookup"><span data-stu-id="1f2e9-105">Blocks execution of all threads in a group until all memory accesses have been completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f2e9-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1f2e9-106">Syntax</span></span>

``` syntax
void AllMemoryBarrier(void);
```

## <a name="parameters"></a><span data-ttu-id="1f2e9-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1f2e9-107">Parameters</span></span>

<span data-ttu-id="1f2e9-108">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="1f2e9-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1f2e9-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1f2e9-109">Return value</span></span>

<span data-ttu-id="1f2e9-110">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="1f2e9-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f2e9-111">Notes</span><span class="sxs-lookup"><span data-stu-id="1f2e9-111">Remarks</span></span>

<span data-ttu-id="1f2e9-112">Une barrière de mémoire garantit que les opérations de mémoire en suspens sont terminées.</span><span class="sxs-lookup"><span data-stu-id="1f2e9-112">A memory barrier guarantees that outstanding memory operations have completed.</span></span> <span data-ttu-id="1f2e9-113">Les threads sont synchronisés aux barrières GroupSync.</span><span class="sxs-lookup"><span data-stu-id="1f2e9-113">Threads are synchronized at GroupSync barriers.</span></span> <span data-ttu-id="1f2e9-114">Cela peut bloquer un ou des threads si les opérations de mémoire sont en cours.</span><span class="sxs-lookup"><span data-stu-id="1f2e9-114">This may stall a thread or threads if memory operations are in progress.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="1f2e9-115">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="1f2e9-115">Minimum Shader Model</span></span>

<span data-ttu-id="1f2e9-116">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="1f2e9-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="1f2e9-117">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="1f2e9-117">Shader Model</span></span>                                                                | <span data-ttu-id="1f2e9-118">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="1f2e9-118">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="1f2e9-119">[Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="1f2e9-119">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="1f2e9-120">Oui</span><span class="sxs-lookup"><span data-stu-id="1f2e9-120">yes</span></span>       |



 

<span data-ttu-id="1f2e9-121">Cette fonction est prise en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="1f2e9-121">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="1f2e9-122">Sommet</span><span class="sxs-lookup"><span data-stu-id="1f2e9-122">Vertex</span></span> | <span data-ttu-id="1f2e9-123">Forme</span><span class="sxs-lookup"><span data-stu-id="1f2e9-123">Hull</span></span> | <span data-ttu-id="1f2e9-124">Domain</span><span class="sxs-lookup"><span data-stu-id="1f2e9-124">Domain</span></span> | <span data-ttu-id="1f2e9-125">Géométrie</span><span class="sxs-lookup"><span data-stu-id="1f2e9-125">Geometry</span></span> | <span data-ttu-id="1f2e9-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="1f2e9-126">Pixel</span></span> | <span data-ttu-id="1f2e9-127">Compute</span><span class="sxs-lookup"><span data-stu-id="1f2e9-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="1f2e9-128">x</span><span class="sxs-lookup"><span data-stu-id="1f2e9-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="1f2e9-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f2e9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f2e9-130">Fonctions intrinsèques</span><span class="sxs-lookup"><span data-stu-id="1f2e9-130">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="1f2e9-131">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="1f2e9-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




