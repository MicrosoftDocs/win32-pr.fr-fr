---
title: firstbithigh (fonction)
description: Obtient l’emplacement du premier bit défini à partir du bit de poids le plus élevé et du travail vers le bas, par composant.
ms.assetid: 0fa89a9e-1706-44f7-8dd3-c37af5c11ddc
keywords:
- firstbithigh fonction HLSL
topic_type:
- apiref
api_name:
- firstbithigh
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4da4956aa3a12d064566a3767423f42039b01355
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382142"
---
# <a name="firstbithigh-function"></a><span data-ttu-id="4c8a3-104">firstbithigh (fonction)</span><span class="sxs-lookup"><span data-stu-id="4c8a3-104">firstbithigh function</span></span>

<span data-ttu-id="4c8a3-105">Obtient l’emplacement du premier bit défini à partir du bit de poids le plus élevé et du travail vers le bas, par composant.</span><span class="sxs-lookup"><span data-stu-id="4c8a3-105">Gets the location of the first set bit starting from the highest order bit and working downward, per component.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c8a3-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4c8a3-106">Syntax</span></span>

``` syntax
int firstbithigh(
  in int value
);
```

## <a name="parameters"></a><span data-ttu-id="4c8a3-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4c8a3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c8a3-108">*valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4c8a3-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c8a3-109">Type : **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4c8a3-109">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="4c8a3-110">Valeur d'entrée.</span><span class="sxs-lookup"><span data-stu-id="4c8a3-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c8a3-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4c8a3-111">Return value</span></span>

<span data-ttu-id="4c8a3-112">Type : **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4c8a3-112">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="4c8a3-113">Emplacement du premier bit défini.</span><span class="sxs-lookup"><span data-stu-id="4c8a3-113">The location of the first set bit.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c8a3-114">Notes</span><span class="sxs-lookup"><span data-stu-id="4c8a3-114">Remarks</span></span>

<span data-ttu-id="4c8a3-115">Pour un entier signé, le premier bit significatif est zéro pour un nombre négatif.</span><span class="sxs-lookup"><span data-stu-id="4c8a3-115">For a signed integer, the first significant bit is zero for a negative number.</span></span>

<span data-ttu-id="4c8a3-116">Les versions surchargées suivantes sont également disponibles :</span><span class="sxs-lookup"><span data-stu-id="4c8a3-116">The following overloaded versions are also available:</span></span>

``` syntax
int2 firstbithigh(int2 value);
int3 firstbithigh(int3 value);
int4 firstbithigh(int4 value);
uint firstbithigh(uint value);
uint2 firstbithigh(uint2 value);
uint3 firstbithigh(uint3 value);
uint4 firstbithigh(uint4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="4c8a3-117">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="4c8a3-117">Minimum Shader Model</span></span>

<span data-ttu-id="4c8a3-118">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="4c8a3-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="4c8a3-119">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="4c8a3-119">Shader Model</span></span>                                                                | <span data-ttu-id="4c8a3-120">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="4c8a3-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="4c8a3-121">[Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="4c8a3-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="4c8a3-122">Oui</span><span class="sxs-lookup"><span data-stu-id="4c8a3-122">yes</span></span>       |



 

<span data-ttu-id="4c8a3-123">Cette fonction est prise en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="4c8a3-123">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="4c8a3-124">Sommet</span><span class="sxs-lookup"><span data-stu-id="4c8a3-124">Vertex</span></span> | <span data-ttu-id="4c8a3-125">Forme</span><span class="sxs-lookup"><span data-stu-id="4c8a3-125">Hull</span></span> | <span data-ttu-id="4c8a3-126">Domain</span><span class="sxs-lookup"><span data-stu-id="4c8a3-126">Domain</span></span> | <span data-ttu-id="4c8a3-127">Géométrie</span><span class="sxs-lookup"><span data-stu-id="4c8a3-127">Geometry</span></span> | <span data-ttu-id="4c8a3-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="4c8a3-128">Pixel</span></span> | <span data-ttu-id="4c8a3-129">Compute</span><span class="sxs-lookup"><span data-stu-id="4c8a3-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="4c8a3-130">x</span><span class="sxs-lookup"><span data-stu-id="4c8a3-130">x</span></span>      | <span data-ttu-id="4c8a3-131">x</span><span class="sxs-lookup"><span data-stu-id="4c8a3-131">x</span></span>    | <span data-ttu-id="4c8a3-132">x</span><span class="sxs-lookup"><span data-stu-id="4c8a3-132">x</span></span>      | <span data-ttu-id="4c8a3-133">x</span><span class="sxs-lookup"><span data-stu-id="4c8a3-133">x</span></span>        | <span data-ttu-id="4c8a3-134">x</span><span class="sxs-lookup"><span data-stu-id="4c8a3-134">x</span></span>     | <span data-ttu-id="4c8a3-135">x</span><span class="sxs-lookup"><span data-stu-id="4c8a3-135">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="4c8a3-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c8a3-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c8a3-137">Fonctions intrinsèques</span><span class="sxs-lookup"><span data-stu-id="4c8a3-137">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="4c8a3-138">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="4c8a3-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 