---
title: 'Texture1DArray :: MIPS. Operator, fonction'
description: 'Retourne une variable de ressource en lecture seule. | Texture1DArray :: MIPS. Operator, fonction'
ms.assetid: b8f2ef78-4b50-4051-a00f-5b81cd77d1e0
keywords:
- mips. Fonction d’opérateur HLSL
topic_type:
- apiref
api_name:
- mips.Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cbe2d1116839cede8dda69f1b0b8cf9a049595e9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104043034"
---
# <a name="texture1darraymipsoperator----function"></a><span data-ttu-id="db7b9-105">Texture1DArray :: MIPS. Operator, fonction</span><span class="sxs-lookup"><span data-stu-id="db7b9-105">Texture1DArray::mips.Operator    function</span></span>

<span data-ttu-id="db7b9-106">Retourne une variable de ressource en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="db7b9-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="db7b9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="db7b9-107">Syntax</span></span>

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="db7b9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="db7b9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db7b9-109">*mipSlice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="db7b9-109">*mipSlice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db7b9-110">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="db7b9-110">Type: **uint**</span></span>

<span data-ttu-id="db7b9-111">Index de la tranche MIP.</span><span class="sxs-lookup"><span data-stu-id="db7b9-111">The mip slice index.</span></span>

</dd> <dt>

<span data-ttu-id="db7b9-112">*pos* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="db7b9-112">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db7b9-113">Type : **uint2**</span><span class="sxs-lookup"><span data-stu-id="db7b9-113">Type: **uint2**</span></span>

<span data-ttu-id="db7b9-114">Position d’index.</span><span class="sxs-lookup"><span data-stu-id="db7b9-114">The index position.</span></span> <span data-ttu-id="db7b9-115">Le premier composant contient la coordonnée x.</span><span class="sxs-lookup"><span data-stu-id="db7b9-115">The first component contains the x-coordinate.</span></span> <span data-ttu-id="db7b9-116">Le deuxième composant indique la tranche de tableau souhaitée.</span><span class="sxs-lookup"><span data-stu-id="db7b9-116">The second component indicates the desired array slice.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db7b9-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="db7b9-117">Return value</span></span>

<span data-ttu-id="db7b9-118">Type : **R**</span><span class="sxs-lookup"><span data-stu-id="db7b9-118">Type: **R**</span></span>

<span data-ttu-id="db7b9-119">Variable de ressource en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="db7b9-119">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="db7b9-120">Notes</span><span class="sxs-lookup"><span data-stu-id="db7b9-120">Remarks</span></span>

### <a name="usage-example"></a><span data-ttu-id="db7b9-121">Exemple d'utilisation</span><span class="sxs-lookup"><span data-stu-id="db7b9-121">Usage Example</span></span>


```
Texture1DArray<float4> tex;
uint mip = 2;
uint2 pos_x_and_array = {1234, 3};
float4 f = tex.mips[mip][pos_x_and_array];        
        
```



<span data-ttu-id="db7b9-122">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="db7b9-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="db7b9-123">Sommet</span><span class="sxs-lookup"><span data-stu-id="db7b9-123">Vertex</span></span> | <span data-ttu-id="db7b9-124">Forme</span><span class="sxs-lookup"><span data-stu-id="db7b9-124">Hull</span></span> | <span data-ttu-id="db7b9-125">Domain</span><span class="sxs-lookup"><span data-stu-id="db7b9-125">Domain</span></span> | <span data-ttu-id="db7b9-126">Géométrie</span><span class="sxs-lookup"><span data-stu-id="db7b9-126">Geometry</span></span> | <span data-ttu-id="db7b9-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="db7b9-127">Pixel</span></span> | <span data-ttu-id="db7b9-128">Compute</span><span class="sxs-lookup"><span data-stu-id="db7b9-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="db7b9-129">x</span><span class="sxs-lookup"><span data-stu-id="db7b9-129">x</span></span>      | <span data-ttu-id="db7b9-130">x</span><span class="sxs-lookup"><span data-stu-id="db7b9-130">x</span></span>    | <span data-ttu-id="db7b9-131">x</span><span class="sxs-lookup"><span data-stu-id="db7b9-131">x</span></span>      | <span data-ttu-id="db7b9-132">x</span><span class="sxs-lookup"><span data-stu-id="db7b9-132">x</span></span>        | <span data-ttu-id="db7b9-133">x</span><span class="sxs-lookup"><span data-stu-id="db7b9-133">x</span></span>     | <span data-ttu-id="db7b9-134">x</span><span class="sxs-lookup"><span data-stu-id="db7b9-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="db7b9-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db7b9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db7b9-136">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="db7b9-136">Texture1DArray</span></span>](sm5-object-texture1darray.md)
</dt> <dt>

[<span data-ttu-id="db7b9-137">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="db7b9-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




