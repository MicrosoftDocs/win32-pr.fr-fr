---
title: 'Texture3D :: Operator, fonction'
description: 'Retourne une variable de ressource en lecture seule. | Texture3D :: Operator, fonction'
ms.assetid: d7e27778-6a96-47f8-a58a-1966452adf04
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
ms.openlocfilehash: 5c3bb3718094ee859d1e33a046fde7016973a0aa
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761725"
---
# <a name="texture3doperator--function"></a><span data-ttu-id="9a018-105">Texture3D :: Operator, fonction</span><span class="sxs-lookup"><span data-stu-id="9a018-105">Texture3D::Operator  function</span></span>

<span data-ttu-id="9a018-106">Retourne une variable de ressource en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="9a018-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a018-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9a018-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint3 pos
);
```

## <a name="parameters"></a><span data-ttu-id="9a018-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9a018-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a018-109">*pos* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9a018-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a018-110">Type : **uint3**</span><span class="sxs-lookup"><span data-stu-id="9a018-110">Type: **uint3**</span></span>

<span data-ttu-id="9a018-111">Position d’index.</span><span class="sxs-lookup"><span data-stu-id="9a018-111">The index position.</span></span> <span data-ttu-id="9a018-112">Contient les coordonnées (x, y, z).</span><span class="sxs-lookup"><span data-stu-id="9a018-112">Contains the (x, y, z) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a018-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9a018-113">Return value</span></span>

<span data-ttu-id="9a018-114">Type : **R**</span><span class="sxs-lookup"><span data-stu-id="9a018-114">Type: **R**</span></span>

<span data-ttu-id="9a018-115">Variable de ressource en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="9a018-115">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a018-116">Notes</span><span class="sxs-lookup"><span data-stu-id="9a018-116">Remarks</span></span>

<span data-ttu-id="9a018-117">Cette méthode accède toujours au premier niveau MIP.</span><span class="sxs-lookup"><span data-stu-id="9a018-117">This method always accesses the first mip level.</span></span> <span data-ttu-id="9a018-118">Pour spécifier d’autres niveaux MIP, utilisez plutôt l' [**\[ \] \[ \] opérateur MIP.**](sm5-object-texture3d-mipsoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="9a018-118">To specify other mip levels use the [**mip.operator\[\]\[\]**](sm5-object-texture3d-mipsoperatorindex.md) instead.</span></span>

<span data-ttu-id="9a018-119">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="9a018-119">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="9a018-120">Sommet</span><span class="sxs-lookup"><span data-stu-id="9a018-120">Vertex</span></span> | <span data-ttu-id="9a018-121">Forme</span><span class="sxs-lookup"><span data-stu-id="9a018-121">Hull</span></span> | <span data-ttu-id="9a018-122">Domain</span><span class="sxs-lookup"><span data-stu-id="9a018-122">Domain</span></span> | <span data-ttu-id="9a018-123">Géométrie</span><span class="sxs-lookup"><span data-stu-id="9a018-123">Geometry</span></span> | <span data-ttu-id="9a018-124">Pixel</span><span class="sxs-lookup"><span data-stu-id="9a018-124">Pixel</span></span> | <span data-ttu-id="9a018-125">Compute</span><span class="sxs-lookup"><span data-stu-id="9a018-125">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="9a018-126">x</span><span class="sxs-lookup"><span data-stu-id="9a018-126">x</span></span>      | <span data-ttu-id="9a018-127">x</span><span class="sxs-lookup"><span data-stu-id="9a018-127">x</span></span>    | <span data-ttu-id="9a018-128">x</span><span class="sxs-lookup"><span data-stu-id="9a018-128">x</span></span>      | <span data-ttu-id="9a018-129">x</span><span class="sxs-lookup"><span data-stu-id="9a018-129">x</span></span>        | <span data-ttu-id="9a018-130">x</span><span class="sxs-lookup"><span data-stu-id="9a018-130">x</span></span>     | <span data-ttu-id="9a018-131">x</span><span class="sxs-lookup"><span data-stu-id="9a018-131">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="9a018-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a018-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a018-133">Texture3D</span><span class="sxs-lookup"><span data-stu-id="9a018-133">Texture3D</span></span>](sm5-object-texture3d.md)
</dt> <dt>

[<span data-ttu-id="9a018-134">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="9a018-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




