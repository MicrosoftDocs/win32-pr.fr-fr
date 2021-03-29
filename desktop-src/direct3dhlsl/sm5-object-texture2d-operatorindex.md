---
title: 'Texture2D :: Operator, fonction'
description: 'Retourne une variable de ressource en lecture seule. | Texture2D :: Operator, fonction'
ms.assetid: 72ba3fc8-04c3-479a-b307-525020898bac
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
ms.openlocfilehash: 2c397b1b80836f48cb856d03ccdf52ad2c95ce48
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974223"
---
# <a name="texture2doperator--function"></a><span data-ttu-id="280d4-105">Texture2D :: Operator, fonction</span><span class="sxs-lookup"><span data-stu-id="280d4-105">Texture2D::Operator  function</span></span>

<span data-ttu-id="280d4-106">Retourne une variable de ressource en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="280d4-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="280d4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="280d4-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="280d4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="280d4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="280d4-109">*pos* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="280d4-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="280d4-110">Type : **uint2**</span><span class="sxs-lookup"><span data-stu-id="280d4-110">Type: **uint2**</span></span>

<span data-ttu-id="280d4-111">Position d’index.</span><span class="sxs-lookup"><span data-stu-id="280d4-111">The index position.</span></span> <span data-ttu-id="280d4-112">Contient les coordonnées (x, y).</span><span class="sxs-lookup"><span data-stu-id="280d4-112">Contains the (x, y) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="280d4-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="280d4-113">Return value</span></span>

<span data-ttu-id="280d4-114">Type : **R**</span><span class="sxs-lookup"><span data-stu-id="280d4-114">Type: **R**</span></span>

<span data-ttu-id="280d4-115">Variable de ressource en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="280d4-115">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="280d4-116">Notes</span><span class="sxs-lookup"><span data-stu-id="280d4-116">Remarks</span></span>

<span data-ttu-id="280d4-117">Cette méthode accède toujours au premier niveau MIP.</span><span class="sxs-lookup"><span data-stu-id="280d4-117">This method always accesses the first mip level.</span></span> <span data-ttu-id="280d4-118">Pour spécifier d’autres niveaux MIP, utilisez plutôt la méthode [**MIP. Operator \[ \] \[ \]**](sm5-object-texture2d-mipsoperatorindex.md) .</span><span class="sxs-lookup"><span data-stu-id="280d4-118">To specify other mip levels, use the [**mip.operator\[\]\[\]**](sm5-object-texture2d-mipsoperatorindex.md) method instead.</span></span>

<span data-ttu-id="280d4-119">Les échantillons de texture peuvent être utilisés pour l’interpolation bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="280d4-119">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="280d4-120">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="280d4-120">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="280d4-121">Sommet</span><span class="sxs-lookup"><span data-stu-id="280d4-121">Vertex</span></span> | <span data-ttu-id="280d4-122">Forme</span><span class="sxs-lookup"><span data-stu-id="280d4-122">Hull</span></span> | <span data-ttu-id="280d4-123">Domain</span><span class="sxs-lookup"><span data-stu-id="280d4-123">Domain</span></span> | <span data-ttu-id="280d4-124">Géométrie</span><span class="sxs-lookup"><span data-stu-id="280d4-124">Geometry</span></span> | <span data-ttu-id="280d4-125">Pixel</span><span class="sxs-lookup"><span data-stu-id="280d4-125">Pixel</span></span> | <span data-ttu-id="280d4-126">Compute</span><span class="sxs-lookup"><span data-stu-id="280d4-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="280d4-127">x</span><span class="sxs-lookup"><span data-stu-id="280d4-127">x</span></span>      | <span data-ttu-id="280d4-128">x</span><span class="sxs-lookup"><span data-stu-id="280d4-128">x</span></span>    | <span data-ttu-id="280d4-129">x</span><span class="sxs-lookup"><span data-stu-id="280d4-129">x</span></span>      | <span data-ttu-id="280d4-130">x</span><span class="sxs-lookup"><span data-stu-id="280d4-130">x</span></span>        | <span data-ttu-id="280d4-131">x</span><span class="sxs-lookup"><span data-stu-id="280d4-131">x</span></span>     | <span data-ttu-id="280d4-132">x</span><span class="sxs-lookup"><span data-stu-id="280d4-132">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="280d4-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="280d4-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="280d4-134">Texture2D</span><span class="sxs-lookup"><span data-stu-id="280d4-134">Texture2D</span></span>](sm5-object-texture2d.md)
</dt> <dt>

[<span data-ttu-id="280d4-135">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="280d4-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




