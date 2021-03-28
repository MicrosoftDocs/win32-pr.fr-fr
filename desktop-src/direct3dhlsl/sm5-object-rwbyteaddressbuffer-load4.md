---
title: 'RWByteAddressBuffer :: Load4 (uint), fonction'
description: 'Obtient quatre valeurs. | RWByteAddressBuffer :: Load4 (uint), fonction'
ms.assetid: b46cd119-75be-4c2d-82f9-5dcabd7e4400
keywords:
- Load4 fonction HLSL
topic_type:
- apiref
api_name:
- Load4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb2bdc5adf3b3d95c68871a14c9382891a59ad52
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974410"
---
# <a name="rwbyteaddressbufferload4uint-function"></a><span data-ttu-id="32f6d-105">RWByteAddressBuffer :: Load4 (uint), fonction</span><span class="sxs-lookup"><span data-stu-id="32f6d-105">RWByteAddressBuffer::Load4(uint) function</span></span>

<span data-ttu-id="32f6d-106">Obtient quatre valeurs.</span><span class="sxs-lookup"><span data-stu-id="32f6d-106">Gets four values.</span></span>

## <a name="syntax"></a><span data-ttu-id="32f6d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="32f6d-107">Syntax</span></span>

``` syntax
uint4 Load4(
  in uint address
);
```

## <a name="parameters"></a><span data-ttu-id="32f6d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="32f6d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32f6d-109">*adresse* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="32f6d-109">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32f6d-110">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="32f6d-110">Type: **uint**</span></span>

<span data-ttu-id="32f6d-111">Adresse d’entrée en octets, qui doit être un multiple de 4.</span><span class="sxs-lookup"><span data-stu-id="32f6d-111">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32f6d-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="32f6d-112">Return value</span></span>

<span data-ttu-id="32f6d-113">Type : **uint4**</span><span class="sxs-lookup"><span data-stu-id="32f6d-113">Type: **uint4**</span></span>

<span data-ttu-id="32f6d-114">Quatre valeurs.</span><span class="sxs-lookup"><span data-stu-id="32f6d-114">Four values.</span></span>

## <a name="remarks"></a><span data-ttu-id="32f6d-115">Notes</span><span class="sxs-lookup"><span data-stu-id="32f6d-115">Remarks</span></span>

<span data-ttu-id="32f6d-116">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="32f6d-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="32f6d-117">Sommet</span><span class="sxs-lookup"><span data-stu-id="32f6d-117">Vertex</span></span> | <span data-ttu-id="32f6d-118">Forme</span><span class="sxs-lookup"><span data-stu-id="32f6d-118">Hull</span></span> | <span data-ttu-id="32f6d-119">Domain</span><span class="sxs-lookup"><span data-stu-id="32f6d-119">Domain</span></span> | <span data-ttu-id="32f6d-120">Géométrie</span><span class="sxs-lookup"><span data-stu-id="32f6d-120">Geometry</span></span> | <span data-ttu-id="32f6d-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="32f6d-121">Pixel</span></span> | <span data-ttu-id="32f6d-122">Compute</span><span class="sxs-lookup"><span data-stu-id="32f6d-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="32f6d-123">x</span><span class="sxs-lookup"><span data-stu-id="32f6d-123">x</span></span>     | <span data-ttu-id="32f6d-124">x</span><span class="sxs-lookup"><span data-stu-id="32f6d-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="32f6d-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="32f6d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32f6d-126">Méthodes Load4</span><span class="sxs-lookup"><span data-stu-id="32f6d-126">Load4 methods</span></span>](rwbyteaddressbuffer-load4.md)
</dt> <dt>

[<span data-ttu-id="32f6d-127">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="32f6d-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




