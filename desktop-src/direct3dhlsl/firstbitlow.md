---
title: firstbitlow (fonction)
description: Retourne l’emplacement du premier bit défini à partir du bit d’ordre le plus bas et du travail vers le haut, par composant.
ms.assetid: 204250f3-1a9b-445d-bd16-4cc9a5d9d60a
keywords:
- firstbitlow fonction HLSL
topic_type:
- apiref
api_name:
- firstbitlow
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a647314383bc022b7c3b3e1b5a255a42a099c620
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031433"
---
# <a name="firstbitlow-function"></a><span data-ttu-id="19263-104">firstbitlow (fonction)</span><span class="sxs-lookup"><span data-stu-id="19263-104">firstbitlow function</span></span>

<span data-ttu-id="19263-105">Retourne l’emplacement du premier bit défini à partir du bit d’ordre le plus bas et du travail vers le haut, par composant.</span><span class="sxs-lookup"><span data-stu-id="19263-105">Returns the location of the first set bit starting from the lowest order bit and working upward, per component.</span></span>

## <a name="syntax"></a><span data-ttu-id="19263-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="19263-106">Syntax</span></span>

``` syntax
int firstbitlow(
  in int value
);
```

## <a name="parameters"></a><span data-ttu-id="19263-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="19263-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19263-108">*valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="19263-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19263-109">Type : **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="19263-109">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="19263-110">Valeur d'entrée.</span><span class="sxs-lookup"><span data-stu-id="19263-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19263-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="19263-111">Return value</span></span>

<span data-ttu-id="19263-112">Type : **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="19263-112">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="19263-113">Emplacement du premier bit défini.</span><span class="sxs-lookup"><span data-stu-id="19263-113">The location of the first set bit.</span></span>

## <a name="remarks"></a><span data-ttu-id="19263-114">Notes</span><span class="sxs-lookup"><span data-stu-id="19263-114">Remarks</span></span>

<span data-ttu-id="19263-115">Les versions surchargées suivantes sont également disponibles :</span><span class="sxs-lookup"><span data-stu-id="19263-115">The following overloaded versions are also available:</span></span>

``` syntax
uint2 firstbitlow(uint2 value);
uint3 firstbitlow(uint3 value);
uint4 firstbitlow(uint4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="19263-116">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="19263-116">Minimum Shader Model</span></span>

<span data-ttu-id="19263-117">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="19263-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="19263-118">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="19263-118">Shader Model</span></span>                                                                | <span data-ttu-id="19263-119">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="19263-119">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="19263-120">[Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="19263-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="19263-121">Oui</span><span class="sxs-lookup"><span data-stu-id="19263-121">yes</span></span>       |



 

<span data-ttu-id="19263-122">Cette fonction est prise en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="19263-122">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="19263-123">Sommet</span><span class="sxs-lookup"><span data-stu-id="19263-123">Vertex</span></span> | <span data-ttu-id="19263-124">Forme</span><span class="sxs-lookup"><span data-stu-id="19263-124">Hull</span></span> | <span data-ttu-id="19263-125">Domain</span><span class="sxs-lookup"><span data-stu-id="19263-125">Domain</span></span> | <span data-ttu-id="19263-126">Géométrie</span><span class="sxs-lookup"><span data-stu-id="19263-126">Geometry</span></span> | <span data-ttu-id="19263-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="19263-127">Pixel</span></span> | <span data-ttu-id="19263-128">Compute</span><span class="sxs-lookup"><span data-stu-id="19263-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="19263-129">x</span><span class="sxs-lookup"><span data-stu-id="19263-129">x</span></span>      | <span data-ttu-id="19263-130">x</span><span class="sxs-lookup"><span data-stu-id="19263-130">x</span></span>    | <span data-ttu-id="19263-131">x</span><span class="sxs-lookup"><span data-stu-id="19263-131">x</span></span>      | <span data-ttu-id="19263-132">x</span><span class="sxs-lookup"><span data-stu-id="19263-132">x</span></span>        | <span data-ttu-id="19263-133">x</span><span class="sxs-lookup"><span data-stu-id="19263-133">x</span></span>     | <span data-ttu-id="19263-134">x</span><span class="sxs-lookup"><span data-stu-id="19263-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="19263-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19263-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19263-136">Fonctions intrinsèques</span><span class="sxs-lookup"><span data-stu-id="19263-136">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="19263-137">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="19263-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 