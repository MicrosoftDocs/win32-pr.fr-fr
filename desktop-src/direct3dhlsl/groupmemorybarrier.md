---
title: GroupMemoryBarrier fonction)
description: Bloque l’exécution de tous les threads dans un groupe jusqu’à ce que tous les accès partagés au groupe aient été effectués.
ms.assetid: cebd4277-47a0-401a-bfbe-8d956412f254
keywords:
- GroupMemoryBarrier fonction HLSL
topic_type:
- apiref
api_name:
- GroupMemoryBarrier
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 54a140a892b0e9144ef23fc0290ca3bb3747e90a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104029958"
---
# <a name="groupmemorybarrier-function"></a><span data-ttu-id="cef4e-104">GroupMemoryBarrier fonction)</span><span class="sxs-lookup"><span data-stu-id="cef4e-104">GroupMemoryBarrier function</span></span>

<span data-ttu-id="cef4e-105">Bloque l’exécution de tous les threads dans un groupe jusqu’à ce que tous les accès partagés au groupe aient été effectués.</span><span class="sxs-lookup"><span data-stu-id="cef4e-105">Blocks execution of all threads in a group until all group shared accesses have been completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="cef4e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cef4e-106">Syntax</span></span>

``` syntax
void GroupMemoryBarrier(void);
```

## <a name="parameters"></a><span data-ttu-id="cef4e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cef4e-107">Parameters</span></span>

<span data-ttu-id="cef4e-108">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="cef4e-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cef4e-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cef4e-109">Return value</span></span>

<span data-ttu-id="cef4e-110">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="cef4e-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cef4e-111">Notes</span><span class="sxs-lookup"><span data-stu-id="cef4e-111">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="cef4e-112">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="cef4e-112">Minimum Shader Model</span></span>

<span data-ttu-id="cef4e-113">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="cef4e-113">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="cef4e-114">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="cef4e-114">Shader Model</span></span>                                                                | <span data-ttu-id="cef4e-115">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="cef4e-115">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="cef4e-116">[Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="cef4e-116">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="cef4e-117">Oui</span><span class="sxs-lookup"><span data-stu-id="cef4e-117">yes</span></span>       |



 

<span data-ttu-id="cef4e-118">Cette fonction est prise en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="cef4e-118">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="cef4e-119">Sommet</span><span class="sxs-lookup"><span data-stu-id="cef4e-119">Vertex</span></span> | <span data-ttu-id="cef4e-120">Forme</span><span class="sxs-lookup"><span data-stu-id="cef4e-120">Hull</span></span> | <span data-ttu-id="cef4e-121">Domain</span><span class="sxs-lookup"><span data-stu-id="cef4e-121">Domain</span></span> | <span data-ttu-id="cef4e-122">Géométrie</span><span class="sxs-lookup"><span data-stu-id="cef4e-122">Geometry</span></span> | <span data-ttu-id="cef4e-123">Pixel</span><span class="sxs-lookup"><span data-stu-id="cef4e-123">Pixel</span></span> | <span data-ttu-id="cef4e-124">Compute</span><span class="sxs-lookup"><span data-stu-id="cef4e-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="cef4e-125">x</span><span class="sxs-lookup"><span data-stu-id="cef4e-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="cef4e-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cef4e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cef4e-127">Fonctions intrinsèques</span><span class="sxs-lookup"><span data-stu-id="cef4e-127">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="cef4e-128">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="cef4e-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




