---
title: 'ByteAddressBuffer :: Load (int), fonction'
description: 'Obtient une valeur. | ByteAddressBuffer :: Load (int), fonction'
ms.assetid: a63f4099-2c3b-4d37-9135-b8c63df30824
keywords:
- Charger la fonction HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e0de7d1a8ef8a7fe3173016fe07a433a930c3d59
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991916"
---
# <a name="byteaddressbufferloadint-function"></a><span data-ttu-id="c62fa-105">ByteAddressBuffer :: Load (int), fonction</span><span class="sxs-lookup"><span data-stu-id="c62fa-105">ByteAddressBuffer::Load(int) function</span></span>

<span data-ttu-id="c62fa-106">Obtient une valeur.</span><span class="sxs-lookup"><span data-stu-id="c62fa-106">Gets one value.</span></span>

## <a name="syntax"></a><span data-ttu-id="c62fa-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c62fa-107">Syntax</span></span>

``` syntax
uint Load(
  in int address
);
```

## <a name="parameters"></a><span data-ttu-id="c62fa-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c62fa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c62fa-109">*adresse* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c62fa-109">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c62fa-110">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="c62fa-110">Type: **int**</span></span>

<span data-ttu-id="c62fa-111">Adresse d’entrée en octets, qui doit être un multiple de 4.</span><span class="sxs-lookup"><span data-stu-id="c62fa-111">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c62fa-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c62fa-112">Return value</span></span>

<span data-ttu-id="c62fa-113">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="c62fa-113">Type: **uint**</span></span>

<span data-ttu-id="c62fa-114">Une valeur.</span><span class="sxs-lookup"><span data-stu-id="c62fa-114">One value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c62fa-115">Notes</span><span class="sxs-lookup"><span data-stu-id="c62fa-115">Remarks</span></span>

<span data-ttu-id="c62fa-116">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="c62fa-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="c62fa-117">Sommet</span><span class="sxs-lookup"><span data-stu-id="c62fa-117">Vertex</span></span> | <span data-ttu-id="c62fa-118">Forme</span><span class="sxs-lookup"><span data-stu-id="c62fa-118">Hull</span></span> | <span data-ttu-id="c62fa-119">Domain</span><span class="sxs-lookup"><span data-stu-id="c62fa-119">Domain</span></span> | <span data-ttu-id="c62fa-120">Géométrie</span><span class="sxs-lookup"><span data-stu-id="c62fa-120">Geometry</span></span> | <span data-ttu-id="c62fa-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="c62fa-121">Pixel</span></span> | <span data-ttu-id="c62fa-122">Compute</span><span class="sxs-lookup"><span data-stu-id="c62fa-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="c62fa-123">x</span><span class="sxs-lookup"><span data-stu-id="c62fa-123">x</span></span>      | <span data-ttu-id="c62fa-124">x</span><span class="sxs-lookup"><span data-stu-id="c62fa-124">x</span></span>    | <span data-ttu-id="c62fa-125">x</span><span class="sxs-lookup"><span data-stu-id="c62fa-125">x</span></span>      | <span data-ttu-id="c62fa-126">x</span><span class="sxs-lookup"><span data-stu-id="c62fa-126">x</span></span>        | <span data-ttu-id="c62fa-127">x</span><span class="sxs-lookup"><span data-stu-id="c62fa-127">x</span></span>     | <span data-ttu-id="c62fa-128">x</span><span class="sxs-lookup"><span data-stu-id="c62fa-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="c62fa-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c62fa-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c62fa-130">Méthodes Load</span><span class="sxs-lookup"><span data-stu-id="c62fa-130">Load methods</span></span>](byteaddressbuffer-load.md)
</dt> <dt>

[<span data-ttu-id="c62fa-131">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="c62fa-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




