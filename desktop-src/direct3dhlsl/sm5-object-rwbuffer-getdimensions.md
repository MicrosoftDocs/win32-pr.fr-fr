---
title: 'RWBuffer :: GetDimensions,, fonction'
description: 'Obtient la longueur de la mémoire tampon. | RWBuffer :: GetDimensions,, fonction'
ms.assetid: 600147cb-9513-4b74-a873-1ed22b31cdf7
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
ms.openlocfilehash: 98e419d3e77a27f211f0e063573caffcd6c61ce8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992065"
---
# <a name="rwbuffergetdimensions-function"></a><span data-ttu-id="30739-105">RWBuffer :: GetDimensions,, fonction</span><span class="sxs-lookup"><span data-stu-id="30739-105">RWBuffer::GetDimensions function</span></span>

<span data-ttu-id="30739-106">Obtient la longueur de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="30739-106">Gets the length of the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="30739-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="30739-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint dim
);
```

## <a name="parameters"></a><span data-ttu-id="30739-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="30739-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30739-109">*Dim* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="30739-109">*dim* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="30739-110">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="30739-110">Type: **uint**</span></span>

<span data-ttu-id="30739-111">Longueur, en octets, de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="30739-111">The length, in bytes, of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30739-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="30739-112">Return value</span></span>

<span data-ttu-id="30739-113">Rien</span><span class="sxs-lookup"><span data-stu-id="30739-113">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="30739-114">Notes</span><span class="sxs-lookup"><span data-stu-id="30739-114">Remarks</span></span>

<span data-ttu-id="30739-115">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="30739-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="30739-116">Sommet</span><span class="sxs-lookup"><span data-stu-id="30739-116">Vertex</span></span> | <span data-ttu-id="30739-117">Forme</span><span class="sxs-lookup"><span data-stu-id="30739-117">Hull</span></span> | <span data-ttu-id="30739-118">Domain</span><span class="sxs-lookup"><span data-stu-id="30739-118">Domain</span></span> | <span data-ttu-id="30739-119">Géométrie</span><span class="sxs-lookup"><span data-stu-id="30739-119">Geometry</span></span> | <span data-ttu-id="30739-120">Pixel</span><span class="sxs-lookup"><span data-stu-id="30739-120">Pixel</span></span> | <span data-ttu-id="30739-121">Compute</span><span class="sxs-lookup"><span data-stu-id="30739-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="30739-122">x</span><span class="sxs-lookup"><span data-stu-id="30739-122">x</span></span>     | <span data-ttu-id="30739-123">x</span><span class="sxs-lookup"><span data-stu-id="30739-123">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="30739-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30739-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30739-125">RWBuffer</span><span class="sxs-lookup"><span data-stu-id="30739-125">RWBuffer</span></span>](sm5-object-rwbuffer.md)
</dt> <dt>

[<span data-ttu-id="30739-126">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="30739-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




