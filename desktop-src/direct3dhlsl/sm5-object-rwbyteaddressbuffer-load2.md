---
title: 'RWByteAddressBuffer :: Load2 (uint), fonction'
description: 'Obtient deux valeurs. | RWByteAddressBuffer :: Load2 (uint), fonction'
ms.assetid: a00396cb-e68d-479e-ab3f-4c52f2cfc3bc
keywords:
- Load2 fonction HLSL
topic_type:
- apiref
api_name:
- Load2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7595477448deb087b94664100710690a6f386a94
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974395"
---
# <a name="rwbyteaddressbufferload2uint-function"></a><span data-ttu-id="644be-105">RWByteAddressBuffer :: Load2 (uint), fonction</span><span class="sxs-lookup"><span data-stu-id="644be-105">RWByteAddressBuffer::Load2(uint) function</span></span>

<span data-ttu-id="644be-106">Obtient deux valeurs.</span><span class="sxs-lookup"><span data-stu-id="644be-106">Gets two values.</span></span>

## <a name="syntax"></a><span data-ttu-id="644be-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="644be-107">Syntax</span></span>

``` syntax
uint2 Load2(
  in uint address
);
```

## <a name="parameters"></a><span data-ttu-id="644be-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="644be-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="644be-109">*adresse* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="644be-109">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="644be-110">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="644be-110">Type: **uint**</span></span>

<span data-ttu-id="644be-111">Adresse d’entrée en octets, qui doit être un multiple de 4.</span><span class="sxs-lookup"><span data-stu-id="644be-111">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="644be-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="644be-112">Return value</span></span>

<span data-ttu-id="644be-113">Type : **uint2**</span><span class="sxs-lookup"><span data-stu-id="644be-113">Type: **uint2**</span></span>

<span data-ttu-id="644be-114">Deux valeurs.</span><span class="sxs-lookup"><span data-stu-id="644be-114">Two values.</span></span>

## <a name="remarks"></a><span data-ttu-id="644be-115">Notes</span><span class="sxs-lookup"><span data-stu-id="644be-115">Remarks</span></span>

<span data-ttu-id="644be-116">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="644be-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="644be-117">Sommet</span><span class="sxs-lookup"><span data-stu-id="644be-117">Vertex</span></span> | <span data-ttu-id="644be-118">Forme</span><span class="sxs-lookup"><span data-stu-id="644be-118">Hull</span></span> | <span data-ttu-id="644be-119">Domain</span><span class="sxs-lookup"><span data-stu-id="644be-119">Domain</span></span> | <span data-ttu-id="644be-120">Géométrie</span><span class="sxs-lookup"><span data-stu-id="644be-120">Geometry</span></span> | <span data-ttu-id="644be-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="644be-121">Pixel</span></span> | <span data-ttu-id="644be-122">Compute</span><span class="sxs-lookup"><span data-stu-id="644be-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="644be-123">x</span><span class="sxs-lookup"><span data-stu-id="644be-123">x</span></span>     | <span data-ttu-id="644be-124">x</span><span class="sxs-lookup"><span data-stu-id="644be-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="644be-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="644be-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="644be-126">Méthodes Load2</span><span class="sxs-lookup"><span data-stu-id="644be-126">Load2 methods</span></span>](rwbyteaddressbuffer-load2.md)
</dt> <dt>

[<span data-ttu-id="644be-127">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="644be-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




