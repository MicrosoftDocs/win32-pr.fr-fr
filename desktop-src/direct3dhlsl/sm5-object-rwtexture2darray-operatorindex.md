---
title: 'RWTexture2DArray :: Operator, fonction'
description: 'Retourne une variable de ressource. | RWTexture2DArray :: Operator, fonction'
ms.assetid: ae3d0697-ea0a-450d-bdfe-7bc5d8faf11a
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
ms.openlocfilehash: faf49c48fbf5042ce2765005cd8daea4d1227255
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104042997"
---
# <a name="rwtexture2darrayoperator--function"></a><span data-ttu-id="44d0f-105">RWTexture2DArray :: Operator, fonction</span><span class="sxs-lookup"><span data-stu-id="44d0f-105">RWTexture2DArray::Operator  function</span></span>

<span data-ttu-id="44d0f-106">Retourne une variable de ressource.</span><span class="sxs-lookup"><span data-stu-id="44d0f-106">Returns a resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="44d0f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="44d0f-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint3 pos
);
```

## <a name="parameters"></a><span data-ttu-id="44d0f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="44d0f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44d0f-109">*pos* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="44d0f-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44d0f-110">Type : **uint3**</span><span class="sxs-lookup"><span data-stu-id="44d0f-110">Type: **uint3**</span></span>

<span data-ttu-id="44d0f-111">Position d’index.</span><span class="sxs-lookup"><span data-stu-id="44d0f-111">The index position.</span></span> <span data-ttu-id="44d0f-112">Le premier et le deuxième composant contiennent les coordonnées (x, y).</span><span class="sxs-lookup"><span data-stu-id="44d0f-112">The first and second components contain the (x, y) coordinates.</span></span> <span data-ttu-id="44d0f-113">Le troisième composant indique la tranche de tableau souhaitée.</span><span class="sxs-lookup"><span data-stu-id="44d0f-113">The third component indicates the desired array slice.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44d0f-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="44d0f-114">Return value</span></span>

<span data-ttu-id="44d0f-115">Type : **R**</span><span class="sxs-lookup"><span data-stu-id="44d0f-115">Type: **R**</span></span>

<span data-ttu-id="44d0f-116">Variable de ressource.</span><span class="sxs-lookup"><span data-stu-id="44d0f-116">A resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="44d0f-117">Notes</span><span class="sxs-lookup"><span data-stu-id="44d0f-117">Remarks</span></span>

<span data-ttu-id="44d0f-118">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="44d0f-118">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="44d0f-119">Sommet</span><span class="sxs-lookup"><span data-stu-id="44d0f-119">Vertex</span></span> | <span data-ttu-id="44d0f-120">Forme</span><span class="sxs-lookup"><span data-stu-id="44d0f-120">Hull</span></span> | <span data-ttu-id="44d0f-121">Domain</span><span class="sxs-lookup"><span data-stu-id="44d0f-121">Domain</span></span> | <span data-ttu-id="44d0f-122">Géométrie</span><span class="sxs-lookup"><span data-stu-id="44d0f-122">Geometry</span></span> | <span data-ttu-id="44d0f-123">Pixel</span><span class="sxs-lookup"><span data-stu-id="44d0f-123">Pixel</span></span> | <span data-ttu-id="44d0f-124">Compute</span><span class="sxs-lookup"><span data-stu-id="44d0f-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="44d0f-125">x</span><span class="sxs-lookup"><span data-stu-id="44d0f-125">x</span></span>     | <span data-ttu-id="44d0f-126">x</span><span class="sxs-lookup"><span data-stu-id="44d0f-126">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="44d0f-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44d0f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44d0f-128">RWTexture2DArray</span><span class="sxs-lookup"><span data-stu-id="44d0f-128">RWTexture2DArray</span></span>](sm5-object-rwtexture2darray.md)
</dt> <dt>

[<span data-ttu-id="44d0f-129">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="44d0f-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




