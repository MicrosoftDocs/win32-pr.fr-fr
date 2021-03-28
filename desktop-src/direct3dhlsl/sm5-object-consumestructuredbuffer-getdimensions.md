---
title: 'ConsumeStructuredBuffer :: GetDimensions,, fonction'
description: 'Obtient les dimensions de ressource. | ConsumeStructuredBuffer :: GetDimensions,, fonction'
ms.assetid: 0710a4fb-23b0-4b19-b9ed-21bbb9874d33
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
ms.openlocfilehash: a204ed44c90c60b327ceb201037c6758763b3a05
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991881"
---
# <a name="consumestructuredbuffergetdimensions-function"></a><span data-ttu-id="2ba92-105">ConsumeStructuredBuffer :: GetDimensions,, fonction</span><span class="sxs-lookup"><span data-stu-id="2ba92-105">ConsumeStructuredBuffer::GetDimensions function</span></span>

<span data-ttu-id="2ba92-106">Obtient les dimensions de ressource.</span><span class="sxs-lookup"><span data-stu-id="2ba92-106">Gets the resource dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ba92-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2ba92-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint numStructs,
  out uint stride
);
```

## <a name="parameters"></a><span data-ttu-id="2ba92-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2ba92-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ba92-109">*numStructs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2ba92-109">*numStructs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ba92-110">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="2ba92-110">Type: **uint**</span></span>

<span data-ttu-id="2ba92-111">Nombre de structures.</span><span class="sxs-lookup"><span data-stu-id="2ba92-111">The number of structures.</span></span>

</dd> <dt>

<span data-ttu-id="2ba92-112">*Stride* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2ba92-112">*stride* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ba92-113">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="2ba92-113">Type: **uint**</span></span>

<span data-ttu-id="2ba92-114">STRIDE, en octets, de chaque élément.</span><span class="sxs-lookup"><span data-stu-id="2ba92-114">The stride, in bytes, of each element.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ba92-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2ba92-115">Return value</span></span>

<span data-ttu-id="2ba92-116">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="2ba92-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ba92-117">Notes</span><span class="sxs-lookup"><span data-stu-id="2ba92-117">Remarks</span></span>

<span data-ttu-id="2ba92-118">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="2ba92-118">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="2ba92-119">Sommet</span><span class="sxs-lookup"><span data-stu-id="2ba92-119">Vertex</span></span> | <span data-ttu-id="2ba92-120">Forme</span><span class="sxs-lookup"><span data-stu-id="2ba92-120">Hull</span></span> | <span data-ttu-id="2ba92-121">Domain</span><span class="sxs-lookup"><span data-stu-id="2ba92-121">Domain</span></span> | <span data-ttu-id="2ba92-122">Géométrie</span><span class="sxs-lookup"><span data-stu-id="2ba92-122">Geometry</span></span> | <span data-ttu-id="2ba92-123">Pixel</span><span class="sxs-lookup"><span data-stu-id="2ba92-123">Pixel</span></span> | <span data-ttu-id="2ba92-124">Compute</span><span class="sxs-lookup"><span data-stu-id="2ba92-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="2ba92-125">x</span><span class="sxs-lookup"><span data-stu-id="2ba92-125">x</span></span>      | <span data-ttu-id="2ba92-126">x</span><span class="sxs-lookup"><span data-stu-id="2ba92-126">x</span></span>    | <span data-ttu-id="2ba92-127">x</span><span class="sxs-lookup"><span data-stu-id="2ba92-127">x</span></span>      | <span data-ttu-id="2ba92-128">x</span><span class="sxs-lookup"><span data-stu-id="2ba92-128">x</span></span>        | <span data-ttu-id="2ba92-129">x</span><span class="sxs-lookup"><span data-stu-id="2ba92-129">x</span></span>     | <span data-ttu-id="2ba92-130">x</span><span class="sxs-lookup"><span data-stu-id="2ba92-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="2ba92-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ba92-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ba92-132">ConsumeStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="2ba92-132">ConsumeStructuredBuffer</span></span>](sm5-object-consumestructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="2ba92-133">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="2ba92-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




