---
title: 'RWByteAddressBuffer :: Store, fonction'
description: Définit une valeur.
ms.assetid: edfda955-602c-44f4-adc3-77b61c9dcd05
keywords:
- Fonction de stockage HLSL
topic_type:
- apiref
api_name:
- Store
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9e161e4fb64d09e41c6529954e63b2ace55207e9
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2019
ms.locfileid: "104971486"
---
# <a name="store-function"></a><span data-ttu-id="f1559-104">Store, fonction</span><span class="sxs-lookup"><span data-stu-id="f1559-104">Store function</span></span>

<span data-ttu-id="f1559-105">Définit une valeur.</span><span class="sxs-lookup"><span data-stu-id="f1559-105">Sets one value.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1559-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f1559-106">Syntax</span></span>

``` syntax
void Store(
  in uint address,
  in uint value
);
```

## <a name="parameters"></a><span data-ttu-id="f1559-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f1559-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1559-108">*adresse* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f1559-108">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1559-109">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="f1559-109">Type: **uint**</span></span>

<span data-ttu-id="f1559-110">Adresse d’entrée en octets, qui doit être un multiple de 4.</span><span class="sxs-lookup"><span data-stu-id="f1559-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="f1559-111">*valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f1559-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1559-112">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="f1559-112">Type: **uint**</span></span>

<span data-ttu-id="f1559-113">Une valeur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="f1559-113">One input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1559-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f1559-114">Return value</span></span>

<span data-ttu-id="f1559-115">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="f1559-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1559-116">Notes</span><span class="sxs-lookup"><span data-stu-id="f1559-116">Remarks</span></span>

<span data-ttu-id="f1559-117">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="f1559-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="f1559-118">Sommet</span><span class="sxs-lookup"><span data-stu-id="f1559-118">Vertex</span></span> | <span data-ttu-id="f1559-119">Forme</span><span class="sxs-lookup"><span data-stu-id="f1559-119">Hull</span></span> | <span data-ttu-id="f1559-120">Domain</span><span class="sxs-lookup"><span data-stu-id="f1559-120">Domain</span></span> | <span data-ttu-id="f1559-121">Géométrie</span><span class="sxs-lookup"><span data-stu-id="f1559-121">Geometry</span></span> | <span data-ttu-id="f1559-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="f1559-122">Pixel</span></span> | <span data-ttu-id="f1559-123">Compute</span><span class="sxs-lookup"><span data-stu-id="f1559-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="f1559-124">x</span><span class="sxs-lookup"><span data-stu-id="f1559-124">x</span></span>     | <span data-ttu-id="f1559-125">x</span><span class="sxs-lookup"><span data-stu-id="f1559-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="f1559-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f1559-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1559-127">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="f1559-127">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="f1559-128">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="f1559-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




