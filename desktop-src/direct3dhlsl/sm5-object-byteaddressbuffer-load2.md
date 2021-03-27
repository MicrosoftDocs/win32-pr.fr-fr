---
title: 'ByteAddressBuffer :: Load2 (uint), fonction'
description: 'Obtient deux valeurs. | ByteAddressBuffer :: Load2 (uint), fonction'
ms.assetid: 696ce310-4d65-4382-97ec-046160197c67
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
ms.openlocfilehash: 78204fc3d41daf07a54974fbf103685e718ab79d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761617"
---
# <a name="byteaddressbufferload2uint-function"></a><span data-ttu-id="8b97f-105">ByteAddressBuffer :: Load2 (uint), fonction</span><span class="sxs-lookup"><span data-stu-id="8b97f-105">ByteAddressBuffer::Load2(uint) function</span></span>

<span data-ttu-id="8b97f-106">Obtient deux valeurs.</span><span class="sxs-lookup"><span data-stu-id="8b97f-106">Gets two values.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b97f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8b97f-107">Syntax</span></span>

``` syntax
uint2 Load2(
  in uint address
);
```

## <a name="parameters"></a><span data-ttu-id="8b97f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8b97f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b97f-109">*adresse* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8b97f-109">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b97f-110">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="8b97f-110">Type: **uint**</span></span>

<span data-ttu-id="8b97f-111">Adresse d’entrée en octets, qui doit être un multiple de 4.</span><span class="sxs-lookup"><span data-stu-id="8b97f-111">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b97f-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8b97f-112">Return value</span></span>

<span data-ttu-id="8b97f-113">Type : **uint2**</span><span class="sxs-lookup"><span data-stu-id="8b97f-113">Type: **uint2**</span></span>

<span data-ttu-id="8b97f-114">Deux valeurs.</span><span class="sxs-lookup"><span data-stu-id="8b97f-114">Two values.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b97f-115">Notes</span><span class="sxs-lookup"><span data-stu-id="8b97f-115">Remarks</span></span>

<span data-ttu-id="8b97f-116">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="8b97f-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="8b97f-117">Sommet</span><span class="sxs-lookup"><span data-stu-id="8b97f-117">Vertex</span></span> | <span data-ttu-id="8b97f-118">Forme</span><span class="sxs-lookup"><span data-stu-id="8b97f-118">Hull</span></span> | <span data-ttu-id="8b97f-119">Domain</span><span class="sxs-lookup"><span data-stu-id="8b97f-119">Domain</span></span> | <span data-ttu-id="8b97f-120">Géométrie</span><span class="sxs-lookup"><span data-stu-id="8b97f-120">Geometry</span></span> | <span data-ttu-id="8b97f-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="8b97f-121">Pixel</span></span> | <span data-ttu-id="8b97f-122">Compute</span><span class="sxs-lookup"><span data-stu-id="8b97f-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="8b97f-123">x</span><span class="sxs-lookup"><span data-stu-id="8b97f-123">x</span></span>      | <span data-ttu-id="8b97f-124">x</span><span class="sxs-lookup"><span data-stu-id="8b97f-124">x</span></span>    | <span data-ttu-id="8b97f-125">x</span><span class="sxs-lookup"><span data-stu-id="8b97f-125">x</span></span>      | <span data-ttu-id="8b97f-126">x</span><span class="sxs-lookup"><span data-stu-id="8b97f-126">x</span></span>        | <span data-ttu-id="8b97f-127">x</span><span class="sxs-lookup"><span data-stu-id="8b97f-127">x</span></span>     | <span data-ttu-id="8b97f-128">x</span><span class="sxs-lookup"><span data-stu-id="8b97f-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="8b97f-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b97f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b97f-130">Méthodes Load2</span><span class="sxs-lookup"><span data-stu-id="8b97f-130">Load2 methods</span></span>](byteaddressbuffer-load2.md)
</dt> <dt>

[<span data-ttu-id="8b97f-131">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="8b97f-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




