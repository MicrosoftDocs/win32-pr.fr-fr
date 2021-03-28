---
title: 'Texture2D :: MIPS. Operator, fonction'
description: 'Retourne une variable de ressource en lecture seule. | Texture2D :: MIPS. Operator, fonction'
ms.assetid: 201996a7-741f-4457-ab77-9cd653f3682b
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
ms.openlocfilehash: 994ede49563b1d4e568769be48a0e60592fe3dde
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104973958"
---
# <a name="texture2dmipsoperator----function"></a><span data-ttu-id="a243e-105">Texture2D :: MIPS. Operator, fonction</span><span class="sxs-lookup"><span data-stu-id="a243e-105">Texture2D::mips.Operator    function</span></span>

<span data-ttu-id="a243e-106">Retourne une variable de ressource en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="a243e-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="a243e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a243e-107">Syntax</span></span>

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="a243e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a243e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a243e-109">*mipSlice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a243e-109">*mipSlice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a243e-110">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="a243e-110">Type: **uint**</span></span>

<span data-ttu-id="a243e-111">Index de la tranche MIP.</span><span class="sxs-lookup"><span data-stu-id="a243e-111">The mip slice index.</span></span>

</dd> <dt>

<span data-ttu-id="a243e-112">*pos* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a243e-112">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a243e-113">Type : **uint2**</span><span class="sxs-lookup"><span data-stu-id="a243e-113">Type: **uint2**</span></span>

<span data-ttu-id="a243e-114">Position d’index.</span><span class="sxs-lookup"><span data-stu-id="a243e-114">The index position.</span></span> <span data-ttu-id="a243e-115">Contient les coordonnées (x, y).</span><span class="sxs-lookup"><span data-stu-id="a243e-115">Contains the (x, y) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a243e-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a243e-116">Return value</span></span>

<span data-ttu-id="a243e-117">Type : **R**</span><span class="sxs-lookup"><span data-stu-id="a243e-117">Type: **R**</span></span>

<span data-ttu-id="a243e-118">Variable de ressource en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="a243e-118">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="a243e-119">Notes</span><span class="sxs-lookup"><span data-stu-id="a243e-119">Remarks</span></span>

### <a name="usage-example"></a><span data-ttu-id="a243e-120">Exemple d'utilisation</span><span class="sxs-lookup"><span data-stu-id="a243e-120">Usage Example</span></span>


```
Texture2D<float4> tex;
uint mip = 2;
uint2 pos_xy = {123, 456};
float4 f = tex.mips[mip][pos_xy];
        
```



<span data-ttu-id="a243e-121">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="a243e-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="a243e-122">Sommet</span><span class="sxs-lookup"><span data-stu-id="a243e-122">Vertex</span></span> | <span data-ttu-id="a243e-123">Forme</span><span class="sxs-lookup"><span data-stu-id="a243e-123">Hull</span></span> | <span data-ttu-id="a243e-124">Domain</span><span class="sxs-lookup"><span data-stu-id="a243e-124">Domain</span></span> | <span data-ttu-id="a243e-125">Géométrie</span><span class="sxs-lookup"><span data-stu-id="a243e-125">Geometry</span></span> | <span data-ttu-id="a243e-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="a243e-126">Pixel</span></span> | <span data-ttu-id="a243e-127">Compute</span><span class="sxs-lookup"><span data-stu-id="a243e-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="a243e-128">x</span><span class="sxs-lookup"><span data-stu-id="a243e-128">x</span></span>      | <span data-ttu-id="a243e-129">x</span><span class="sxs-lookup"><span data-stu-id="a243e-129">x</span></span>    | <span data-ttu-id="a243e-130">x</span><span class="sxs-lookup"><span data-stu-id="a243e-130">x</span></span>      | <span data-ttu-id="a243e-131">x</span><span class="sxs-lookup"><span data-stu-id="a243e-131">x</span></span>        | <span data-ttu-id="a243e-132">x</span><span class="sxs-lookup"><span data-stu-id="a243e-132">x</span></span>     | <span data-ttu-id="a243e-133">x</span><span class="sxs-lookup"><span data-stu-id="a243e-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="a243e-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a243e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a243e-135">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a243e-135">Texture2D</span></span>](sm5-object-texture2d.md)
</dt> <dt>

[<span data-ttu-id="a243e-136">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="a243e-136">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




