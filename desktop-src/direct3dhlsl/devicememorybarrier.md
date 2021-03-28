---
title: DeviceMemoryBarrier fonction)
description: Bloque l’exécution de tous les threads dans un groupe jusqu’à ce que tous les accès à la mémoire de l’appareil aient été effectués.
ms.assetid: 904ab8f6-4849-4b13-8fac-3967cf66574e
keywords:
- DeviceMemoryBarrier fonction HLSL
topic_type:
- apiref
api_name:
- DeviceMemoryBarrier
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1875b780f528000d46ba31bb979072d6d462fa91
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104380493"
---
# <a name="devicememorybarrier-function"></a><span data-ttu-id="43861-104">DeviceMemoryBarrier fonction)</span><span class="sxs-lookup"><span data-stu-id="43861-104">DeviceMemoryBarrier function</span></span>

<span data-ttu-id="43861-105">Bloque l’exécution de tous les threads dans un groupe jusqu’à ce que tous les accès à la mémoire de l’appareil aient été effectués.</span><span class="sxs-lookup"><span data-stu-id="43861-105">Blocks execution of all threads in a group until all device memory accesses have been completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="43861-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="43861-106">Syntax</span></span>

``` syntax
void DeviceMemoryBarrier(void);
```

## <a name="parameters"></a><span data-ttu-id="43861-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="43861-107">Parameters</span></span>

<span data-ttu-id="43861-108">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="43861-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="43861-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="43861-109">Return value</span></span>

<span data-ttu-id="43861-110">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="43861-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="43861-111">Notes</span><span class="sxs-lookup"><span data-stu-id="43861-111">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="43861-112">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="43861-112">Minimum Shader Model</span></span>

<span data-ttu-id="43861-113">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="43861-113">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="43861-114">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="43861-114">Shader Model</span></span>                                                                | <span data-ttu-id="43861-115">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="43861-115">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="43861-116">[Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="43861-116">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="43861-117">Oui</span><span class="sxs-lookup"><span data-stu-id="43861-117">yes</span></span>       |



 

<span data-ttu-id="43861-118">Cette fonction est prise en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="43861-118">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="43861-119">Sommet</span><span class="sxs-lookup"><span data-stu-id="43861-119">Vertex</span></span> | <span data-ttu-id="43861-120">Forme</span><span class="sxs-lookup"><span data-stu-id="43861-120">Hull</span></span> | <span data-ttu-id="43861-121">Domain</span><span class="sxs-lookup"><span data-stu-id="43861-121">Domain</span></span> | <span data-ttu-id="43861-122">Géométrie</span><span class="sxs-lookup"><span data-stu-id="43861-122">Geometry</span></span> | <span data-ttu-id="43861-123">Pixel</span><span class="sxs-lookup"><span data-stu-id="43861-123">Pixel</span></span> | <span data-ttu-id="43861-124">Compute</span><span class="sxs-lookup"><span data-stu-id="43861-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="43861-125">x</span><span class="sxs-lookup"><span data-stu-id="43861-125">x</span></span>     | <span data-ttu-id="43861-126">x</span><span class="sxs-lookup"><span data-stu-id="43861-126">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="43861-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43861-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43861-128">Fonctions intrinsèques</span><span class="sxs-lookup"><span data-stu-id="43861-128">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="43861-129">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="43861-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




