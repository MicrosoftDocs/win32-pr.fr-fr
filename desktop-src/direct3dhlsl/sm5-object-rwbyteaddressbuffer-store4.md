---
title: 'RWByteAddressBuffer :: Store4, fonction'
description: Définit quatre valeurs.
ms.assetid: 261dd270-79a7-4566-9fbd-52bd8dc3e1bf
keywords:
- Store4 fonction HLSL
topic_type:
- apiref
api_name:
- Store4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 219cd04e4f68ad6f0d16d964e6685c558fed98b1
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2019
ms.locfileid: "104381033"
---
# <a name="store4-function"></a><span data-ttu-id="1b76f-104">Store4 fonction)</span><span class="sxs-lookup"><span data-stu-id="1b76f-104">Store4 function</span></span>

<span data-ttu-id="1b76f-105">Définit quatre valeurs.</span><span class="sxs-lookup"><span data-stu-id="1b76f-105">Sets four values.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b76f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1b76f-106">Syntax</span></span>

``` syntax
void Store4(
  in uint address,
  in uint4 values
);
```

## <a name="parameters"></a><span data-ttu-id="1b76f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1b76f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b76f-108">*adresse* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1b76f-108">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b76f-109">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="1b76f-109">Type: **uint**</span></span>

<span data-ttu-id="1b76f-110">Adresse d’entrée en octets, qui doit être un multiple de 4.</span><span class="sxs-lookup"><span data-stu-id="1b76f-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="1b76f-111">*valeurs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1b76f-111">*values* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b76f-112">Type : **uint4**</span><span class="sxs-lookup"><span data-stu-id="1b76f-112">Type: **uint4**</span></span>

<span data-ttu-id="1b76f-113">Quatre valeurs d’entrée.</span><span class="sxs-lookup"><span data-stu-id="1b76f-113">Four input values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b76f-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1b76f-114">Return value</span></span>

<span data-ttu-id="1b76f-115">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="1b76f-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b76f-116">Notes</span><span class="sxs-lookup"><span data-stu-id="1b76f-116">Remarks</span></span>

<span data-ttu-id="1b76f-117">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="1b76f-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="1b76f-118">Sommet</span><span class="sxs-lookup"><span data-stu-id="1b76f-118">Vertex</span></span> | <span data-ttu-id="1b76f-119">Forme</span><span class="sxs-lookup"><span data-stu-id="1b76f-119">Hull</span></span> | <span data-ttu-id="1b76f-120">Domain</span><span class="sxs-lookup"><span data-stu-id="1b76f-120">Domain</span></span> | <span data-ttu-id="1b76f-121">Géométrie</span><span class="sxs-lookup"><span data-stu-id="1b76f-121">Geometry</span></span> | <span data-ttu-id="1b76f-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="1b76f-122">Pixel</span></span> | <span data-ttu-id="1b76f-123">Compute</span><span class="sxs-lookup"><span data-stu-id="1b76f-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="1b76f-124">x</span><span class="sxs-lookup"><span data-stu-id="1b76f-124">x</span></span>     | <span data-ttu-id="1b76f-125">x</span><span class="sxs-lookup"><span data-stu-id="1b76f-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="1b76f-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b76f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b76f-127">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="1b76f-127">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="1b76f-128">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="1b76f-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




