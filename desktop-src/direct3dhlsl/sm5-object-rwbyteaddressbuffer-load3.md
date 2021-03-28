---
title: 'RWByteAddressBuffer :: Load3 (uint), fonction'
description: 'Obtient trois valeurs. | RWByteAddressBuffer :: Load3 (uint), fonction'
ms.assetid: cf8c4c5d-4748-43d7-896e-33ed07c94b9e
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
ms.openlocfilehash: d6658b4929f09aa7296a284de1fdbf39c7c4f038
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974415"
---
# <a name="rwbyteaddressbufferload3uint-function"></a><span data-ttu-id="dac88-105">RWByteAddressBuffer :: Load3 (uint), fonction</span><span class="sxs-lookup"><span data-stu-id="dac88-105">RWByteAddressBuffer::Load3(uint) function</span></span>

<span data-ttu-id="dac88-106">Obtient trois valeurs.</span><span class="sxs-lookup"><span data-stu-id="dac88-106">Gets three values.</span></span>

## <a name="syntax"></a><span data-ttu-id="dac88-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dac88-107">Syntax</span></span>

``` syntax
uint3 Load3(
  in uint address
);
```

## <a name="parameters"></a><span data-ttu-id="dac88-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dac88-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dac88-109">*adresse* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dac88-109">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dac88-110">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="dac88-110">Type: **uint**</span></span>

<span data-ttu-id="dac88-111">Adresse d’entrée en octets, qui doit être un multiple de 4.</span><span class="sxs-lookup"><span data-stu-id="dac88-111">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dac88-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dac88-112">Return value</span></span>

<span data-ttu-id="dac88-113">Type : **uint3**</span><span class="sxs-lookup"><span data-stu-id="dac88-113">Type: **uint3**</span></span>

<span data-ttu-id="dac88-114">Trois valeurs.</span><span class="sxs-lookup"><span data-stu-id="dac88-114">Three values.</span></span>

## <a name="remarks"></a><span data-ttu-id="dac88-115">Notes</span><span class="sxs-lookup"><span data-stu-id="dac88-115">Remarks</span></span>

<span data-ttu-id="dac88-116">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="dac88-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="dac88-117">Sommet</span><span class="sxs-lookup"><span data-stu-id="dac88-117">Vertex</span></span> | <span data-ttu-id="dac88-118">Forme</span><span class="sxs-lookup"><span data-stu-id="dac88-118">Hull</span></span> | <span data-ttu-id="dac88-119">Domain</span><span class="sxs-lookup"><span data-stu-id="dac88-119">Domain</span></span> | <span data-ttu-id="dac88-120">Géométrie</span><span class="sxs-lookup"><span data-stu-id="dac88-120">Geometry</span></span> | <span data-ttu-id="dac88-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="dac88-121">Pixel</span></span> | <span data-ttu-id="dac88-122">Compute</span><span class="sxs-lookup"><span data-stu-id="dac88-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="dac88-123">x</span><span class="sxs-lookup"><span data-stu-id="dac88-123">x</span></span>     | <span data-ttu-id="dac88-124">x</span><span class="sxs-lookup"><span data-stu-id="dac88-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="dac88-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dac88-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dac88-126">Méthodes Load3</span><span class="sxs-lookup"><span data-stu-id="dac88-126">Load3 methods</span></span>](rwbyteaddressbuffer-load3.md)
</dt> <dt>

[<span data-ttu-id="dac88-127">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="dac88-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




