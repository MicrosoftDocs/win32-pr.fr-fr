---
title: 'Texture1DArray :: Operator, fonction'
description: 'Retourne une variable de ressource en lecture seule. | Texture1DArray :: Operator, fonction'
ms.assetid: 05ec9652-b5dd-41cf-8bef-730c507c5ba4
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
ms.openlocfilehash: 578d778cd1e0e064c435c19fb094feb66f651e05
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974187"
---
# <a name="texture1darrayoperator--function"></a><span data-ttu-id="87fe3-105">Texture1DArray :: Operator, fonction</span><span class="sxs-lookup"><span data-stu-id="87fe3-105">Texture1DArray::Operator  function</span></span>

<span data-ttu-id="87fe3-106">Retourne une variable de ressource en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="87fe3-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="87fe3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="87fe3-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="87fe3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87fe3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87fe3-109">*pos* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="87fe3-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87fe3-110">Type : **uint2**</span><span class="sxs-lookup"><span data-stu-id="87fe3-110">Type: **uint2**</span></span>

<span data-ttu-id="87fe3-111">Position d’index.</span><span class="sxs-lookup"><span data-stu-id="87fe3-111">The index position.</span></span> <span data-ttu-id="87fe3-112">Le premier composant contient la coordonnée x.</span><span class="sxs-lookup"><span data-stu-id="87fe3-112">The first component contains the x-coordinate.</span></span> <span data-ttu-id="87fe3-113">Le deuxième composant indique la tranche de tableau souhaitée.</span><span class="sxs-lookup"><span data-stu-id="87fe3-113">The second component indicates the desired array slice.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87fe3-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="87fe3-114">Return value</span></span>

<span data-ttu-id="87fe3-115">Type : **R**</span><span class="sxs-lookup"><span data-stu-id="87fe3-115">Type: **R**</span></span>

<span data-ttu-id="87fe3-116">Variable de ressource en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="87fe3-116">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="87fe3-117">Notes</span><span class="sxs-lookup"><span data-stu-id="87fe3-117">Remarks</span></span>

<span data-ttu-id="87fe3-118">Cette méthode accède toujours au premier niveau MIP.</span><span class="sxs-lookup"><span data-stu-id="87fe3-118">This method always accesses the first mip level.</span></span> <span data-ttu-id="87fe3-119">Pour spécifier d’autres niveaux MIP, utilisez plutôt la méthode [**MIP. Operator \[ \] \[ \]**](sm5-object-texture1darray-mipsoperatorindex.md) .</span><span class="sxs-lookup"><span data-stu-id="87fe3-119">To specify other mip levels, use the [**mip.operator\[\]\[\]**](sm5-object-texture1darray-mipsoperatorindex.md) method instead.</span></span>

<span data-ttu-id="87fe3-120">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="87fe3-120">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="87fe3-121">Sommet</span><span class="sxs-lookup"><span data-stu-id="87fe3-121">Vertex</span></span> | <span data-ttu-id="87fe3-122">Forme</span><span class="sxs-lookup"><span data-stu-id="87fe3-122">Hull</span></span> | <span data-ttu-id="87fe3-123">Domain</span><span class="sxs-lookup"><span data-stu-id="87fe3-123">Domain</span></span> | <span data-ttu-id="87fe3-124">Géométrie</span><span class="sxs-lookup"><span data-stu-id="87fe3-124">Geometry</span></span> | <span data-ttu-id="87fe3-125">Pixel</span><span class="sxs-lookup"><span data-stu-id="87fe3-125">Pixel</span></span> | <span data-ttu-id="87fe3-126">Compute</span><span class="sxs-lookup"><span data-stu-id="87fe3-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="87fe3-127">x</span><span class="sxs-lookup"><span data-stu-id="87fe3-127">x</span></span>      | <span data-ttu-id="87fe3-128">x</span><span class="sxs-lookup"><span data-stu-id="87fe3-128">x</span></span>    | <span data-ttu-id="87fe3-129">x</span><span class="sxs-lookup"><span data-stu-id="87fe3-129">x</span></span>      | <span data-ttu-id="87fe3-130">x</span><span class="sxs-lookup"><span data-stu-id="87fe3-130">x</span></span>        | <span data-ttu-id="87fe3-131">x</span><span class="sxs-lookup"><span data-stu-id="87fe3-131">x</span></span>     | <span data-ttu-id="87fe3-132">x</span><span class="sxs-lookup"><span data-stu-id="87fe3-132">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="87fe3-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87fe3-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87fe3-134">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="87fe3-134">Texture1DArray</span></span>](sm5-object-texture1darray.md)
</dt> <dt>

[<span data-ttu-id="87fe3-135">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="87fe3-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




