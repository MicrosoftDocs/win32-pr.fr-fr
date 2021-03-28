---
title: 'ByteAddressBuffer :: Load4 (uint), fonction'
description: 'Obtient quatre valeurs. | ByteAddressBuffer :: Load4 (uint), fonction'
ms.assetid: bc74bf29-1c22-4e47-bafc-ecef194f54b8
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
ms.openlocfilehash: 18ce27e7d02a414165aab169e40a6ab14cdd8c4c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974335"
---
# <a name="byteaddressbufferload4uint-function"></a><span data-ttu-id="f2a87-105">ByteAddressBuffer :: Load4 (uint), fonction</span><span class="sxs-lookup"><span data-stu-id="f2a87-105">ByteAddressBuffer::Load4(uint) function</span></span>

<span data-ttu-id="f2a87-106">Obtient quatre valeurs.</span><span class="sxs-lookup"><span data-stu-id="f2a87-106">Gets four values.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2a87-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f2a87-107">Syntax</span></span>

``` syntax
uint4 Load4(
  in uint address
);
```

## <a name="parameters"></a><span data-ttu-id="f2a87-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f2a87-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2a87-109">*adresse* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f2a87-109">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2a87-110">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="f2a87-110">Type: **uint**</span></span>

<span data-ttu-id="f2a87-111">Adresse d’entrée en octets, qui doit être un multiple de 4.</span><span class="sxs-lookup"><span data-stu-id="f2a87-111">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2a87-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f2a87-112">Return value</span></span>

<span data-ttu-id="f2a87-113">Type : **uint4**</span><span class="sxs-lookup"><span data-stu-id="f2a87-113">Type: **uint4**</span></span>

<span data-ttu-id="f2a87-114">Quatre valeurs.</span><span class="sxs-lookup"><span data-stu-id="f2a87-114">Four values.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2a87-115">Notes</span><span class="sxs-lookup"><span data-stu-id="f2a87-115">Remarks</span></span>

<span data-ttu-id="f2a87-116">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="f2a87-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="f2a87-117">Sommet</span><span class="sxs-lookup"><span data-stu-id="f2a87-117">Vertex</span></span> | <span data-ttu-id="f2a87-118">Forme</span><span class="sxs-lookup"><span data-stu-id="f2a87-118">Hull</span></span> | <span data-ttu-id="f2a87-119">Domain</span><span class="sxs-lookup"><span data-stu-id="f2a87-119">Domain</span></span> | <span data-ttu-id="f2a87-120">Géométrie</span><span class="sxs-lookup"><span data-stu-id="f2a87-120">Geometry</span></span> | <span data-ttu-id="f2a87-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="f2a87-121">Pixel</span></span> | <span data-ttu-id="f2a87-122">Compute</span><span class="sxs-lookup"><span data-stu-id="f2a87-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="f2a87-123">x</span><span class="sxs-lookup"><span data-stu-id="f2a87-123">x</span></span>      | <span data-ttu-id="f2a87-124">x</span><span class="sxs-lookup"><span data-stu-id="f2a87-124">x</span></span>    | <span data-ttu-id="f2a87-125">x</span><span class="sxs-lookup"><span data-stu-id="f2a87-125">x</span></span>      | <span data-ttu-id="f2a87-126">x</span><span class="sxs-lookup"><span data-stu-id="f2a87-126">x</span></span>        | <span data-ttu-id="f2a87-127">x</span><span class="sxs-lookup"><span data-stu-id="f2a87-127">x</span></span>     | <span data-ttu-id="f2a87-128">x</span><span class="sxs-lookup"><span data-stu-id="f2a87-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="f2a87-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2a87-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2a87-130">Méthodes Load4</span><span class="sxs-lookup"><span data-stu-id="f2a87-130">Load4 methods</span></span>](byteaddressbuffer-load4.md)
</dt> <dt>

[<span data-ttu-id="f2a87-131">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="f2a87-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




