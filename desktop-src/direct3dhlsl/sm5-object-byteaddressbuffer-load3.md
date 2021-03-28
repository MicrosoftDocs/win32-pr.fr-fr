---
title: 'ByteAddressBuffer :: Load3 (uint), fonction'
description: 'Obtient trois valeurs. | ByteAddressBuffer :: Load3 (uint), fonction'
ms.assetid: 79afeb36-e0e7-44a2-b252-8e3577f4c1a5
keywords:
- Load3 fonction HLSL
topic_type:
- apiref
api_name:
- Load3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e3975d454fcbb8c5dfa8cdef8d7f5718143546f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974338"
---
# <a name="byteaddressbufferload3uint-function"></a><span data-ttu-id="1c80b-105">ByteAddressBuffer :: Load3 (uint), fonction</span><span class="sxs-lookup"><span data-stu-id="1c80b-105">ByteAddressBuffer::Load3(uint) function</span></span>

<span data-ttu-id="1c80b-106">Obtient trois valeurs.</span><span class="sxs-lookup"><span data-stu-id="1c80b-106">Gets three values.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c80b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1c80b-107">Syntax</span></span>

``` syntax
uint3 Load3(
  in uint address
);
```

## <a name="parameters"></a><span data-ttu-id="1c80b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1c80b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c80b-109">*adresse* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1c80b-109">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c80b-110">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="1c80b-110">Type: **uint**</span></span>

<span data-ttu-id="1c80b-111">Adresse d’entrée en octets, qui doit être un multiple de 4.</span><span class="sxs-lookup"><span data-stu-id="1c80b-111">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c80b-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1c80b-112">Return value</span></span>

<span data-ttu-id="1c80b-113">Type : **uint3**</span><span class="sxs-lookup"><span data-stu-id="1c80b-113">Type: **uint3**</span></span>

<span data-ttu-id="1c80b-114">Trois valeurs.</span><span class="sxs-lookup"><span data-stu-id="1c80b-114">Three values.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c80b-115">Notes</span><span class="sxs-lookup"><span data-stu-id="1c80b-115">Remarks</span></span>

<span data-ttu-id="1c80b-116">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="1c80b-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="1c80b-117">Sommet</span><span class="sxs-lookup"><span data-stu-id="1c80b-117">Vertex</span></span> | <span data-ttu-id="1c80b-118">Forme</span><span class="sxs-lookup"><span data-stu-id="1c80b-118">Hull</span></span> | <span data-ttu-id="1c80b-119">Domain</span><span class="sxs-lookup"><span data-stu-id="1c80b-119">Domain</span></span> | <span data-ttu-id="1c80b-120">Géométrie</span><span class="sxs-lookup"><span data-stu-id="1c80b-120">Geometry</span></span> | <span data-ttu-id="1c80b-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="1c80b-121">Pixel</span></span> | <span data-ttu-id="1c80b-122">Compute</span><span class="sxs-lookup"><span data-stu-id="1c80b-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="1c80b-123">x</span><span class="sxs-lookup"><span data-stu-id="1c80b-123">x</span></span>      | <span data-ttu-id="1c80b-124">x</span><span class="sxs-lookup"><span data-stu-id="1c80b-124">x</span></span>    | <span data-ttu-id="1c80b-125">x</span><span class="sxs-lookup"><span data-stu-id="1c80b-125">x</span></span>      | <span data-ttu-id="1c80b-126">x</span><span class="sxs-lookup"><span data-stu-id="1c80b-126">x</span></span>        | <span data-ttu-id="1c80b-127">x</span><span class="sxs-lookup"><span data-stu-id="1c80b-127">x</span></span>     | <span data-ttu-id="1c80b-128">x</span><span class="sxs-lookup"><span data-stu-id="1c80b-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="1c80b-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c80b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c80b-130">Méthodes Load3</span><span class="sxs-lookup"><span data-stu-id="1c80b-130">Load3 methods</span></span>](byteaddressbuffer-load3.md)
</dt> <dt>

[<span data-ttu-id="1c80b-131">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="1c80b-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




