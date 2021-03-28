---
title: 'Texture2DArray :: Operator, fonction'
description: 'Retourne une variable de ressource en lecture seule. | Texture2DArray :: Operator, fonction'
ms.assetid: eb6ff496-c46f-405f-a172-ab747415a2f9
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
ms.openlocfilehash: 1b86aad839fbf28a4fc666b3a5fe5c5788b7b3ae
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104042996"
---
# <a name="texture2darrayoperator--function"></a><span data-ttu-id="705ad-105">Texture2DArray :: Operator, fonction</span><span class="sxs-lookup"><span data-stu-id="705ad-105">Texture2DArray::Operator  function</span></span>

<span data-ttu-id="705ad-106">Retourne une variable de ressource en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="705ad-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="705ad-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="705ad-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint3 pos
);
```

## <a name="parameters"></a><span data-ttu-id="705ad-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="705ad-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="705ad-109">*pos* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="705ad-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="705ad-110">Type : **uint3**</span><span class="sxs-lookup"><span data-stu-id="705ad-110">Type: **uint3**</span></span>

<span data-ttu-id="705ad-111">Position d’index.</span><span class="sxs-lookup"><span data-stu-id="705ad-111">The index position.</span></span> <span data-ttu-id="705ad-112">Le premier et le deuxième composant contiennent les coordonnées (x, y).</span><span class="sxs-lookup"><span data-stu-id="705ad-112">The first and second components contain the (x, y) coordinates.</span></span> <span data-ttu-id="705ad-113">Le troisième composant indique la tranche de tableau souhaitée.</span><span class="sxs-lookup"><span data-stu-id="705ad-113">The third component indicates the desired array slice.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="705ad-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="705ad-114">Return value</span></span>

<span data-ttu-id="705ad-115">Type : **R**</span><span class="sxs-lookup"><span data-stu-id="705ad-115">Type: **R**</span></span>

<span data-ttu-id="705ad-116">Variable de ressource en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="705ad-116">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="705ad-117">Notes</span><span class="sxs-lookup"><span data-stu-id="705ad-117">Remarks</span></span>

<span data-ttu-id="705ad-118">Cette méthode accède toujours au premier niveau MIP.</span><span class="sxs-lookup"><span data-stu-id="705ad-118">This method always accesses the first mip level.</span></span> <span data-ttu-id="705ad-119">Pour spécifier d’autres niveaux MIP, utilisez plutôt la méthode [**MIP. Operator \[ \] \[ \]**](sm5-object-texture2darray-mipsoperatorindex.md) .</span><span class="sxs-lookup"><span data-stu-id="705ad-119">To specify other mip levels, use the [**mip.operator\[\]\[\]**](sm5-object-texture2darray-mipsoperatorindex.md) method instead.</span></span>

<span data-ttu-id="705ad-120">Les échantillons de texture peuvent être utilisés pour l’interpolation bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="705ad-120">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="705ad-121">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="705ad-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="705ad-122">Sommet</span><span class="sxs-lookup"><span data-stu-id="705ad-122">Vertex</span></span> | <span data-ttu-id="705ad-123">Forme</span><span class="sxs-lookup"><span data-stu-id="705ad-123">Hull</span></span> | <span data-ttu-id="705ad-124">Domain</span><span class="sxs-lookup"><span data-stu-id="705ad-124">Domain</span></span> | <span data-ttu-id="705ad-125">Géométrie</span><span class="sxs-lookup"><span data-stu-id="705ad-125">Geometry</span></span> | <span data-ttu-id="705ad-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="705ad-126">Pixel</span></span> | <span data-ttu-id="705ad-127">Compute</span><span class="sxs-lookup"><span data-stu-id="705ad-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="705ad-128">x</span><span class="sxs-lookup"><span data-stu-id="705ad-128">x</span></span>      | <span data-ttu-id="705ad-129">x</span><span class="sxs-lookup"><span data-stu-id="705ad-129">x</span></span>    | <span data-ttu-id="705ad-130">x</span><span class="sxs-lookup"><span data-stu-id="705ad-130">x</span></span>      | <span data-ttu-id="705ad-131">x</span><span class="sxs-lookup"><span data-stu-id="705ad-131">x</span></span>        | <span data-ttu-id="705ad-132">x</span><span class="sxs-lookup"><span data-stu-id="705ad-132">x</span></span>     | <span data-ttu-id="705ad-133">x</span><span class="sxs-lookup"><span data-stu-id="705ad-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="705ad-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="705ad-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="705ad-135">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="705ad-135">Texture2DArray</span></span>](sm5-object-texture2darray.md)
</dt> <dt>

[<span data-ttu-id="705ad-136">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="705ad-136">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




