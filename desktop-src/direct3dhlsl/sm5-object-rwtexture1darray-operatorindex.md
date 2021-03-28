---
title: 'RWTexture1DArray :: Operator, fonction'
description: 'Retourne une variable de ressource. | RWTexture1DArray :: Operator, fonction'
ms.assetid: 7047e670-dd78-4b73-8d80-5575e458f27c
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
ms.openlocfilehash: 6f8623ab25b42f6865e401c5b263a1774206c752
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974227"
---
# <a name="rwtexture1darrayoperator--function"></a><span data-ttu-id="6216d-105">RWTexture1DArray :: Operator, fonction</span><span class="sxs-lookup"><span data-stu-id="6216d-105">RWTexture1DArray::Operator  function</span></span>

<span data-ttu-id="6216d-106">Retourne une variable de ressource.</span><span class="sxs-lookup"><span data-stu-id="6216d-106">Returns a resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="6216d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6216d-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="6216d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6216d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6216d-109">*pos* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6216d-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6216d-110">Type : **uint2**</span><span class="sxs-lookup"><span data-stu-id="6216d-110">Type: **uint2**</span></span>

<span data-ttu-id="6216d-111">Position d’index.</span><span class="sxs-lookup"><span data-stu-id="6216d-111">The index position.</span></span> <span data-ttu-id="6216d-112">Le premier composant contient la coordonnée x.</span><span class="sxs-lookup"><span data-stu-id="6216d-112">The first component contains the x coordinate.</span></span> <span data-ttu-id="6216d-113">Le deuxième composant indique la tranche de tableau souhaitée.</span><span class="sxs-lookup"><span data-stu-id="6216d-113">The second component indicates the desired array slice.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6216d-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6216d-114">Return value</span></span>

<span data-ttu-id="6216d-115">Type : **R**</span><span class="sxs-lookup"><span data-stu-id="6216d-115">Type: **R**</span></span>

<span data-ttu-id="6216d-116">Variable de ressource.</span><span class="sxs-lookup"><span data-stu-id="6216d-116">A resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="6216d-117">Notes</span><span class="sxs-lookup"><span data-stu-id="6216d-117">Remarks</span></span>

<span data-ttu-id="6216d-118">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="6216d-118">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="6216d-119">Sommet</span><span class="sxs-lookup"><span data-stu-id="6216d-119">Vertex</span></span> | <span data-ttu-id="6216d-120">Forme</span><span class="sxs-lookup"><span data-stu-id="6216d-120">Hull</span></span> | <span data-ttu-id="6216d-121">Domain</span><span class="sxs-lookup"><span data-stu-id="6216d-121">Domain</span></span> | <span data-ttu-id="6216d-122">Géométrie</span><span class="sxs-lookup"><span data-stu-id="6216d-122">Geometry</span></span> | <span data-ttu-id="6216d-123">Pixel</span><span class="sxs-lookup"><span data-stu-id="6216d-123">Pixel</span></span> | <span data-ttu-id="6216d-124">Compute</span><span class="sxs-lookup"><span data-stu-id="6216d-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="6216d-125">x</span><span class="sxs-lookup"><span data-stu-id="6216d-125">x</span></span>     | <span data-ttu-id="6216d-126">x</span><span class="sxs-lookup"><span data-stu-id="6216d-126">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="6216d-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6216d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6216d-128">RWTexture1DArray</span><span class="sxs-lookup"><span data-stu-id="6216d-128">RWTexture1DArray</span></span>](sm5-object-rwtexture1darray.md)
</dt> <dt>

[<span data-ttu-id="6216d-129">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="6216d-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




