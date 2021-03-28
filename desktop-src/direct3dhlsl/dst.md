---
title: fonction DST
description: Calcule un vecteur de distance. | fonction DST
ms.assetid: 24d22743-5867-49db-8d0a-55cc3625c947
keywords:
- fonction DST HLSL
topic_type:
- apiref
api_name:
- dst
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 58ce243cf9a9f3e6118763368445e5bcf26ba4cc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103869725"
---
# <a name="dst-function"></a><span data-ttu-id="3ee5b-105">fonction DST</span><span class="sxs-lookup"><span data-stu-id="3ee5b-105">dst function</span></span>

<span data-ttu-id="3ee5b-106">Calcule un vecteur de distance.</span><span class="sxs-lookup"><span data-stu-id="3ee5b-106">Calculates a distance vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ee5b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3ee5b-107">Syntax</span></span>

``` syntax
fVector dst(
  in fVector src0,
  in fVector src1
);
```

## <a name="parameters"></a><span data-ttu-id="3ee5b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3ee5b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ee5b-109">*src0* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3ee5b-109">*src0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ee5b-110">Type : **[fVector](dx-graphics-hlsl-vector.md)**</span><span class="sxs-lookup"><span data-stu-id="3ee5b-110">Type: **[fVector](dx-graphics-hlsl-vector.md)**</span></span>

<span data-ttu-id="3ee5b-111">Premier vecteur.</span><span class="sxs-lookup"><span data-stu-id="3ee5b-111">The first vector.</span></span>

</dd> <dt>

<span data-ttu-id="3ee5b-112">*src1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3ee5b-112">*src1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ee5b-113">Type : **[fVector](dx-graphics-hlsl-vector.md)**</span><span class="sxs-lookup"><span data-stu-id="3ee5b-113">Type: **[fVector](dx-graphics-hlsl-vector.md)**</span></span>

<span data-ttu-id="3ee5b-114">Deuxième vecteur.</span><span class="sxs-lookup"><span data-stu-id="3ee5b-114">The second vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ee5b-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3ee5b-115">Return value</span></span>

<span data-ttu-id="3ee5b-116">Type : **[fVector](dx-graphics-hlsl-vector.md)**</span><span class="sxs-lookup"><span data-stu-id="3ee5b-116">Type: **[fVector](dx-graphics-hlsl-vector.md)**</span></span>

<span data-ttu-id="3ee5b-117">Vecteur de distance calculé.</span><span class="sxs-lookup"><span data-stu-id="3ee5b-117">The computed distance vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ee5b-118">Notes</span><span class="sxs-lookup"><span data-stu-id="3ee5b-118">Remarks</span></span>

<span data-ttu-id="3ee5b-119">Cette fonction intrinsèque fournit les mêmes fonctionnalités que l' [heure d’été](dst---vs.md)de l’instruction du nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="3ee5b-119">This intrinsic function provides the same functionality as the Vertex Shader instruction [dst](dst---vs.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="3ee5b-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ee5b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ee5b-121">Fonctions intrinsèques</span><span class="sxs-lookup"><span data-stu-id="3ee5b-121">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 




