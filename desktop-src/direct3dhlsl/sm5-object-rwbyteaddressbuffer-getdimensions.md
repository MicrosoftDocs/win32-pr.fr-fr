---
title: 'RWByteAddressBuffer :: GetDimensions,, fonction'
description: 'Obtient la longueur de la mémoire tampon. | RWByteAddressBuffer :: GetDimensions,, fonction'
ms.assetid: 7d78aa0d-75b8-43d5-85d9-0a6fb04ae64f
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
ms.openlocfilehash: 0d22b6f655802d77a92611fe8699a405aa323873
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322409"
---
# <a name="rwbyteaddressbuffergetdimensions-function"></a><span data-ttu-id="e1f44-105">RWByteAddressBuffer :: GetDimensions,, fonction</span><span class="sxs-lookup"><span data-stu-id="e1f44-105">RWByteAddressBuffer::GetDimensions function</span></span>

<span data-ttu-id="e1f44-106">Obtient la longueur de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="e1f44-106">Gets the length of the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1f44-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e1f44-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint dim
);
```

## <a name="parameters"></a><span data-ttu-id="e1f44-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e1f44-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1f44-109">*Dim* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e1f44-109">*dim* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e1f44-110">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="e1f44-110">Type: **uint**</span></span>

<span data-ttu-id="e1f44-111">Longueur, en octets, de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="e1f44-111">The length, in bytes, of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1f44-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e1f44-112">Return value</span></span>

<span data-ttu-id="e1f44-113">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="e1f44-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1f44-114">Notes</span><span class="sxs-lookup"><span data-stu-id="e1f44-114">Remarks</span></span>

<span data-ttu-id="e1f44-115">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="e1f44-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="e1f44-116">Sommet</span><span class="sxs-lookup"><span data-stu-id="e1f44-116">Vertex</span></span> | <span data-ttu-id="e1f44-117">Forme</span><span class="sxs-lookup"><span data-stu-id="e1f44-117">Hull</span></span> | <span data-ttu-id="e1f44-118">Domain</span><span class="sxs-lookup"><span data-stu-id="e1f44-118">Domain</span></span> | <span data-ttu-id="e1f44-119">Géométrie</span><span class="sxs-lookup"><span data-stu-id="e1f44-119">Geometry</span></span> | <span data-ttu-id="e1f44-120">Pixel</span><span class="sxs-lookup"><span data-stu-id="e1f44-120">Pixel</span></span> | <span data-ttu-id="e1f44-121">Compute</span><span class="sxs-lookup"><span data-stu-id="e1f44-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="e1f44-122">x</span><span class="sxs-lookup"><span data-stu-id="e1f44-122">x</span></span>     | <span data-ttu-id="e1f44-123">x</span><span class="sxs-lookup"><span data-stu-id="e1f44-123">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="e1f44-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1f44-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1f44-125">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="e1f44-125">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="e1f44-126">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="e1f44-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




