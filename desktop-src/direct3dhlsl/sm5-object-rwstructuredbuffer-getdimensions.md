---
title: 'RWStructuredBuffer :: GetDimensions,, fonction'
description: 'Obtient les dimensions de ressource. | RWStructuredBuffer :: GetDimensions,, fonction'
ms.assetid: 842b3d21-2e2b-4906-93ee-0252b2e8cf85
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
ms.openlocfilehash: 0e3868f33e372472999c29bffdd8e12bc8ef09b7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104973914"
---
# <a name="rwstructuredbuffergetdimensions-function"></a><span data-ttu-id="3ee4c-105">RWStructuredBuffer :: GetDimensions,, fonction</span><span class="sxs-lookup"><span data-stu-id="3ee4c-105">RWStructuredBuffer::GetDimensions function</span></span>

<span data-ttu-id="3ee4c-106">Obtient les dimensions de ressource.</span><span class="sxs-lookup"><span data-stu-id="3ee4c-106">Gets the resource dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ee4c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3ee4c-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint numStructs,
  out uint stride
);
```

## <a name="parameters"></a><span data-ttu-id="3ee4c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3ee4c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ee4c-109">*numStructs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3ee4c-109">*numStructs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ee4c-110">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="3ee4c-110">Type: **uint**</span></span>

<span data-ttu-id="3ee4c-111">Nombre de structures dans la ressource.</span><span class="sxs-lookup"><span data-stu-id="3ee4c-111">The number of structures in the resource.</span></span>

</dd> <dt>

<span data-ttu-id="3ee4c-112">*Stride* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3ee4c-112">*stride* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ee4c-113">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="3ee4c-113">Type: **uint**</span></span>

<span data-ttu-id="3ee4c-114">STRIDE, en octets, de chaque élément de structure.</span><span class="sxs-lookup"><span data-stu-id="3ee4c-114">The stride, in bytes, of each structure element.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ee4c-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3ee4c-115">Return value</span></span>

<span data-ttu-id="3ee4c-116">Rien</span><span class="sxs-lookup"><span data-stu-id="3ee4c-116">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="3ee4c-117">Notes</span><span class="sxs-lookup"><span data-stu-id="3ee4c-117">Remarks</span></span>

<span data-ttu-id="3ee4c-118">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="3ee4c-118">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="3ee4c-119">Sommet</span><span class="sxs-lookup"><span data-stu-id="3ee4c-119">Vertex</span></span> | <span data-ttu-id="3ee4c-120">Forme</span><span class="sxs-lookup"><span data-stu-id="3ee4c-120">Hull</span></span> | <span data-ttu-id="3ee4c-121">Domain</span><span class="sxs-lookup"><span data-stu-id="3ee4c-121">Domain</span></span> | <span data-ttu-id="3ee4c-122">Géométrie</span><span class="sxs-lookup"><span data-stu-id="3ee4c-122">Geometry</span></span> | <span data-ttu-id="3ee4c-123">Pixel</span><span class="sxs-lookup"><span data-stu-id="3ee4c-123">Pixel</span></span> | <span data-ttu-id="3ee4c-124">Compute</span><span class="sxs-lookup"><span data-stu-id="3ee4c-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="3ee4c-125">x</span><span class="sxs-lookup"><span data-stu-id="3ee4c-125">x</span></span>     | <span data-ttu-id="3ee4c-126">x</span><span class="sxs-lookup"><span data-stu-id="3ee4c-126">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="3ee4c-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ee4c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ee4c-128">RWStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="3ee4c-128">RWStructuredBuffer</span></span>](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="3ee4c-129">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="3ee4c-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




