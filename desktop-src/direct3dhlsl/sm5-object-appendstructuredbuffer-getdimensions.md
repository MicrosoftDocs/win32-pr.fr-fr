---
title: 'AppendStructuredBuffer :: GetDimensions,, fonction'
description: 'Obtient les dimensions de ressource. | AppendStructuredBuffer :: GetDimensions,, fonction'
ms.assetid: 41ed86d5-25c0-48bd-add9-792eb89605c3
keywords:
- GetDimensions, fonction HLSL
topic_type:
- apiref
api_name:
- GetDimensions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 93db905ae40f1bec7488eca292f4ea44d87950d3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104973919"
---
# <a name="appendstructuredbuffergetdimensions-function"></a><span data-ttu-id="4ff06-105">AppendStructuredBuffer :: GetDimensions,, fonction</span><span class="sxs-lookup"><span data-stu-id="4ff06-105">AppendStructuredBuffer::GetDimensions function</span></span>

<span data-ttu-id="4ff06-106">Obtient les dimensions de ressource.</span><span class="sxs-lookup"><span data-stu-id="4ff06-106">Gets the resource dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ff06-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4ff06-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint numStructs,
  out uint stride
);
```

## <a name="parameters"></a><span data-ttu-id="4ff06-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4ff06-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ff06-109">*numStructs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4ff06-109">*numStructs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ff06-110">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="4ff06-110">Type: **uint**</span></span>

<span data-ttu-id="4ff06-111">Nombre de structures.</span><span class="sxs-lookup"><span data-stu-id="4ff06-111">The number of structures.</span></span>

</dd> <dt>

<span data-ttu-id="4ff06-112">*Stride* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4ff06-112">*stride* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ff06-113">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="4ff06-113">Type: **uint**</span></span>

<span data-ttu-id="4ff06-114">Nombre d’octets dans chaque élément.</span><span class="sxs-lookup"><span data-stu-id="4ff06-114">The number of bytes in each element.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ff06-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4ff06-115">Return value</span></span>

<span data-ttu-id="4ff06-116">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="4ff06-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ff06-117">Notes</span><span class="sxs-lookup"><span data-stu-id="4ff06-117">Remarks</span></span>

<span data-ttu-id="4ff06-118">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="4ff06-118">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="4ff06-119">Sommet</span><span class="sxs-lookup"><span data-stu-id="4ff06-119">Vertex</span></span> | <span data-ttu-id="4ff06-120">Forme</span><span class="sxs-lookup"><span data-stu-id="4ff06-120">Hull</span></span> | <span data-ttu-id="4ff06-121">Domain</span><span class="sxs-lookup"><span data-stu-id="4ff06-121">Domain</span></span> | <span data-ttu-id="4ff06-122">Géométrie</span><span class="sxs-lookup"><span data-stu-id="4ff06-122">Geometry</span></span> | <span data-ttu-id="4ff06-123">Pixel</span><span class="sxs-lookup"><span data-stu-id="4ff06-123">Pixel</span></span> | <span data-ttu-id="4ff06-124">Compute</span><span class="sxs-lookup"><span data-stu-id="4ff06-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="4ff06-125">x</span><span class="sxs-lookup"><span data-stu-id="4ff06-125">x</span></span>      | <span data-ttu-id="4ff06-126">x</span><span class="sxs-lookup"><span data-stu-id="4ff06-126">x</span></span>    | <span data-ttu-id="4ff06-127">x</span><span class="sxs-lookup"><span data-stu-id="4ff06-127">x</span></span>      | <span data-ttu-id="4ff06-128">x</span><span class="sxs-lookup"><span data-stu-id="4ff06-128">x</span></span>        | <span data-ttu-id="4ff06-129">x</span><span class="sxs-lookup"><span data-stu-id="4ff06-129">x</span></span>     | <span data-ttu-id="4ff06-130">x</span><span class="sxs-lookup"><span data-stu-id="4ff06-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="4ff06-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ff06-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ff06-132">AppendStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="4ff06-132">AppendStructuredBuffer</span></span>](sm5-object-appendstructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="4ff06-133">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="4ff06-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




