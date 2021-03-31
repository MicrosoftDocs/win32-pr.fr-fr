---
title: 'StructuredBuffer :: GetDimensions,, fonction'
description: 'Obtient les dimensions de ressource. | StructuredBuffer :: GetDimensions,, fonction'
ms.assetid: 423ea79c-4440-4837-b637-95180a1d5019
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
ms.openlocfilehash: 2b3d7c879c77386ddee80a63053711b8ae34ee8c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322161"
---
# <a name="structuredbuffergetdimensions-function"></a><span data-ttu-id="eef5d-105">StructuredBuffer :: GetDimensions,, fonction</span><span class="sxs-lookup"><span data-stu-id="eef5d-105">StructuredBuffer::GetDimensions function</span></span>

<span data-ttu-id="eef5d-106">Obtient les dimensions de ressource.</span><span class="sxs-lookup"><span data-stu-id="eef5d-106">Gets the resource dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="eef5d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eef5d-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint numStructs,
  out uint stride
);
```

## <a name="parameters"></a><span data-ttu-id="eef5d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eef5d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eef5d-109">*numStructs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="eef5d-109">*numStructs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eef5d-110">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="eef5d-110">Type: **uint**</span></span>

<span data-ttu-id="eef5d-111">Nombre de structures dans la ressource.</span><span class="sxs-lookup"><span data-stu-id="eef5d-111">The number of structures in the resource.</span></span>

</dd> <dt>

<span data-ttu-id="eef5d-112">*Stride* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="eef5d-112">*stride* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eef5d-113">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="eef5d-113">Type: **uint**</span></span>

<span data-ttu-id="eef5d-114">STRIDE, en octets, de chaque élément de structure.</span><span class="sxs-lookup"><span data-stu-id="eef5d-114">The stride, in bytes, of each structure element.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eef5d-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="eef5d-115">Return value</span></span>

<span data-ttu-id="eef5d-116">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="eef5d-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eef5d-117">Notes</span><span class="sxs-lookup"><span data-stu-id="eef5d-117">Remarks</span></span>

<span data-ttu-id="eef5d-118">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="eef5d-118">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="eef5d-119">Sommet</span><span class="sxs-lookup"><span data-stu-id="eef5d-119">Vertex</span></span> | <span data-ttu-id="eef5d-120">Forme</span><span class="sxs-lookup"><span data-stu-id="eef5d-120">Hull</span></span> | <span data-ttu-id="eef5d-121">Domain</span><span class="sxs-lookup"><span data-stu-id="eef5d-121">Domain</span></span> | <span data-ttu-id="eef5d-122">Géométrie</span><span class="sxs-lookup"><span data-stu-id="eef5d-122">Geometry</span></span> | <span data-ttu-id="eef5d-123">Pixel</span><span class="sxs-lookup"><span data-stu-id="eef5d-123">Pixel</span></span> | <span data-ttu-id="eef5d-124">Compute</span><span class="sxs-lookup"><span data-stu-id="eef5d-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="eef5d-125">x</span><span class="sxs-lookup"><span data-stu-id="eef5d-125">x</span></span>      | <span data-ttu-id="eef5d-126">x</span><span class="sxs-lookup"><span data-stu-id="eef5d-126">x</span></span>    | <span data-ttu-id="eef5d-127">x</span><span class="sxs-lookup"><span data-stu-id="eef5d-127">x</span></span>      | <span data-ttu-id="eef5d-128">x</span><span class="sxs-lookup"><span data-stu-id="eef5d-128">x</span></span>        | <span data-ttu-id="eef5d-129">x</span><span class="sxs-lookup"><span data-stu-id="eef5d-129">x</span></span>     | <span data-ttu-id="eef5d-130">x</span><span class="sxs-lookup"><span data-stu-id="eef5d-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="eef5d-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eef5d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eef5d-132">StructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="eef5d-132">StructuredBuffer</span></span>](sm5-object-structuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="eef5d-133">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="eef5d-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




