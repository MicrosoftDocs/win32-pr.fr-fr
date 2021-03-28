---
title: 'RWTexture2D :: Operator, fonction'
description: 'Retourne une variable de ressource. | RWTexture2D :: Operator, fonction'
ms.assetid: 339dba7d-b0c6-4112-ae40-555661577a3e
keywords:
- Fonction d’opérateur HLSL
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8c1ff25cdf4a0f33d041500f6a81220261f216c4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974190"
---
# <a name="rwtexture2doperator--function"></a><span data-ttu-id="be93d-105">RWTexture2D :: Operator, fonction</span><span class="sxs-lookup"><span data-stu-id="be93d-105">RWTexture2D::Operator  function</span></span>

<span data-ttu-id="be93d-106">Retourne une variable de ressource.</span><span class="sxs-lookup"><span data-stu-id="be93d-106">Returns a resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="be93d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be93d-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="be93d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="be93d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be93d-109">*pos* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="be93d-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be93d-110">Type : **uint2**</span><span class="sxs-lookup"><span data-stu-id="be93d-110">Type: **uint2**</span></span>

<span data-ttu-id="be93d-111">Position d’index.</span><span class="sxs-lookup"><span data-stu-id="be93d-111">The index position.</span></span> <span data-ttu-id="be93d-112">Contient les coordonnées (x, y).</span><span class="sxs-lookup"><span data-stu-id="be93d-112">Contains the (x, y) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be93d-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="be93d-113">Return value</span></span>

<span data-ttu-id="be93d-114">Type : **R**</span><span class="sxs-lookup"><span data-stu-id="be93d-114">Type: **R**</span></span>

<span data-ttu-id="be93d-115">Variable de ressource.</span><span class="sxs-lookup"><span data-stu-id="be93d-115">A resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="be93d-116">Notes</span><span class="sxs-lookup"><span data-stu-id="be93d-116">Remarks</span></span>

<span data-ttu-id="be93d-117">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="be93d-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="be93d-118">Sommet</span><span class="sxs-lookup"><span data-stu-id="be93d-118">Vertex</span></span> | <span data-ttu-id="be93d-119">Forme</span><span class="sxs-lookup"><span data-stu-id="be93d-119">Hull</span></span> | <span data-ttu-id="be93d-120">Domain</span><span class="sxs-lookup"><span data-stu-id="be93d-120">Domain</span></span> | <span data-ttu-id="be93d-121">Géométrie</span><span class="sxs-lookup"><span data-stu-id="be93d-121">Geometry</span></span> | <span data-ttu-id="be93d-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="be93d-122">Pixel</span></span> | <span data-ttu-id="be93d-123">Compute</span><span class="sxs-lookup"><span data-stu-id="be93d-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="be93d-124">x</span><span class="sxs-lookup"><span data-stu-id="be93d-124">x</span></span>     | <span data-ttu-id="be93d-125">x</span><span class="sxs-lookup"><span data-stu-id="be93d-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="be93d-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be93d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be93d-127">RWTexture2D</span><span class="sxs-lookup"><span data-stu-id="be93d-127">RWTexture2D</span></span>](sm5-object-rwtexture2d.md)
</dt> <dt>

[<span data-ttu-id="be93d-128">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="be93d-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




