---
title: DeviceMemoryBarrierWithGroupSync fonction)
description: Bloque l’exécution de tous les threads dans un groupe jusqu’à ce que tous les accès à la mémoire de l’appareil aient été effectués et que tous les threads du groupe aient atteint cet appel.
ms.assetid: 77c54064-a996-4c51-84b5-7da60e884c4f
keywords:
- DeviceMemoryBarrierWithGroupSync fonction HLSL
topic_type:
- apiref
api_name:
- DeviceMemoryBarrierWithGroupSync
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a7a4a27b3256fb78c7b60b960fc5383cfd5b5d4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312832"
---
# <a name="devicememorybarrierwithgroupsync-function"></a><span data-ttu-id="e3239-104">DeviceMemoryBarrierWithGroupSync fonction)</span><span class="sxs-lookup"><span data-stu-id="e3239-104">DeviceMemoryBarrierWithGroupSync function</span></span>

<span data-ttu-id="e3239-105">Bloque l’exécution de tous les threads dans un groupe jusqu’à ce que tous les accès à la mémoire de l’appareil aient été effectués et que tous les threads du groupe aient atteint cet appel.</span><span class="sxs-lookup"><span data-stu-id="e3239-105">Blocks execution of all threads in a group until all device memory accesses have been completed and all threads in the group have reached this call.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3239-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e3239-106">Syntax</span></span>

``` syntax
void DeviceMemoryBarrierWithGroupSync(void);
```

## <a name="parameters"></a><span data-ttu-id="e3239-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e3239-107">Parameters</span></span>

<span data-ttu-id="e3239-108">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="e3239-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e3239-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e3239-109">Return value</span></span>

<span data-ttu-id="e3239-110">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="e3239-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3239-111">Notes</span><span class="sxs-lookup"><span data-stu-id="e3239-111">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="e3239-112">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="e3239-112">Minimum Shader Model</span></span>

<span data-ttu-id="e3239-113">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="e3239-113">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e3239-114">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="e3239-114">Shader Model</span></span>                                                                | <span data-ttu-id="e3239-115">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="e3239-115">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="e3239-116">[Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="e3239-116">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="e3239-117">Oui</span><span class="sxs-lookup"><span data-stu-id="e3239-117">yes</span></span>       |



 

<span data-ttu-id="e3239-118">Cette fonction est prise en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="e3239-118">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="e3239-119">Sommet</span><span class="sxs-lookup"><span data-stu-id="e3239-119">Vertex</span></span> | <span data-ttu-id="e3239-120">Forme</span><span class="sxs-lookup"><span data-stu-id="e3239-120">Hull</span></span> | <span data-ttu-id="e3239-121">Domain</span><span class="sxs-lookup"><span data-stu-id="e3239-121">Domain</span></span> | <span data-ttu-id="e3239-122">Géométrie</span><span class="sxs-lookup"><span data-stu-id="e3239-122">Geometry</span></span> | <span data-ttu-id="e3239-123">Pixel</span><span class="sxs-lookup"><span data-stu-id="e3239-123">Pixel</span></span> | <span data-ttu-id="e3239-124">Compute</span><span class="sxs-lookup"><span data-stu-id="e3239-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="e3239-125">x</span><span class="sxs-lookup"><span data-stu-id="e3239-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="e3239-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3239-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3239-127">Fonctions intrinsèques</span><span class="sxs-lookup"><span data-stu-id="e3239-127">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="e3239-128">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="e3239-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




