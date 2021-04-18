---
title: 'ByteAddressBuffer :: GetDimensions,, fonction'
description: 'Obtient la longueur de la mémoire tampon. | ByteAddressBuffer :: GetDimensions,, fonction'
ms.assetid: 32099118-8d8a-440e-96ba-2580d905f068
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
ms.openlocfilehash: 1cbb705789e444a6fa54aeb87190912996f65621
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991869"
---
# <a name="byteaddressbuffergetdimensions-function"></a><span data-ttu-id="ae999-105">ByteAddressBuffer :: GetDimensions,, fonction</span><span class="sxs-lookup"><span data-stu-id="ae999-105">ByteAddressBuffer::GetDimensions function</span></span>

<span data-ttu-id="ae999-106">Obtient la longueur de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="ae999-106">Gets the length of the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae999-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ae999-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint dim
);
```

## <a name="parameters"></a><span data-ttu-id="ae999-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ae999-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae999-109">*Dim* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ae999-109">*dim* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae999-110">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="ae999-110">Type: **uint**</span></span>

<span data-ttu-id="ae999-111">Longueur, en octets, de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="ae999-111">The length, in bytes, of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae999-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ae999-112">Return value</span></span>

<span data-ttu-id="ae999-113">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="ae999-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae999-114">Notes</span><span class="sxs-lookup"><span data-stu-id="ae999-114">Remarks</span></span>

<span data-ttu-id="ae999-115">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="ae999-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="ae999-116">Sommet</span><span class="sxs-lookup"><span data-stu-id="ae999-116">Vertex</span></span> | <span data-ttu-id="ae999-117">Forme</span><span class="sxs-lookup"><span data-stu-id="ae999-117">Hull</span></span> | <span data-ttu-id="ae999-118">Domain</span><span class="sxs-lookup"><span data-stu-id="ae999-118">Domain</span></span> | <span data-ttu-id="ae999-119">Géométrie</span><span class="sxs-lookup"><span data-stu-id="ae999-119">Geometry</span></span> | <span data-ttu-id="ae999-120">Pixel</span><span class="sxs-lookup"><span data-stu-id="ae999-120">Pixel</span></span> | <span data-ttu-id="ae999-121">Compute</span><span class="sxs-lookup"><span data-stu-id="ae999-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ae999-122">x</span><span class="sxs-lookup"><span data-stu-id="ae999-122">x</span></span>      | <span data-ttu-id="ae999-123">x</span><span class="sxs-lookup"><span data-stu-id="ae999-123">x</span></span>    | <span data-ttu-id="ae999-124">x</span><span class="sxs-lookup"><span data-stu-id="ae999-124">x</span></span>      | <span data-ttu-id="ae999-125">x</span><span class="sxs-lookup"><span data-stu-id="ae999-125">x</span></span>        | <span data-ttu-id="ae999-126">x</span><span class="sxs-lookup"><span data-stu-id="ae999-126">x</span></span>     | <span data-ttu-id="ae999-127">x</span><span class="sxs-lookup"><span data-stu-id="ae999-127">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ae999-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae999-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae999-129">ByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="ae999-129">ByteAddressBuffer</span></span>](sm5-object-byteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="ae999-130">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="ae999-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




