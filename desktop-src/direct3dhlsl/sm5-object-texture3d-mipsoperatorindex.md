---
title: 'Texture3D :: MIPS. Operator, fonction'
description: 'Retourne une variable de ressource en lecture seule. | Texture3D :: MIPS. Operator, fonction'
ms.assetid: d5f6cb3b-4163-44c2-8379-ac8a412b1aa6
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
ms.openlocfilehash: e8f7064459354ec4827ba6d96795e82ccab3800c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211437"
---
# <a name="texture3dmipsoperator----function"></a><span data-ttu-id="ac438-105">Texture3D :: MIPS. Operator, fonction</span><span class="sxs-lookup"><span data-stu-id="ac438-105">Texture3D::mips.Operator    function</span></span>

<span data-ttu-id="ac438-106">Retourne une variable de ressource en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="ac438-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac438-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ac438-107">Syntax</span></span>

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint3 pos
);
```

## <a name="parameters"></a><span data-ttu-id="ac438-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ac438-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac438-109">*mipSlice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ac438-109">*mipSlice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac438-110">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="ac438-110">Type: **uint**</span></span>

<span data-ttu-id="ac438-111">Index de la tranche MIP.</span><span class="sxs-lookup"><span data-stu-id="ac438-111">The mip slice index.</span></span>

</dd> <dt>

<span data-ttu-id="ac438-112">*pos* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ac438-112">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac438-113">Type : **uint3**</span><span class="sxs-lookup"><span data-stu-id="ac438-113">Type: **uint3**</span></span>

<span data-ttu-id="ac438-114">Position d’index.</span><span class="sxs-lookup"><span data-stu-id="ac438-114">The index position.</span></span> <span data-ttu-id="ac438-115">Contient les coordonnées (x, y, z).</span><span class="sxs-lookup"><span data-stu-id="ac438-115">Contains the (x, y, z) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac438-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ac438-116">Return value</span></span>

<span data-ttu-id="ac438-117">Type : **R**</span><span class="sxs-lookup"><span data-stu-id="ac438-117">Type: **R**</span></span>

<span data-ttu-id="ac438-118">Variable de ressource en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="ac438-118">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac438-119">Notes</span><span class="sxs-lookup"><span data-stu-id="ac438-119">Remarks</span></span>

### <a name="usage-example"></a><span data-ttu-id="ac438-120">Exemple d'utilisation</span><span class="sxs-lookup"><span data-stu-id="ac438-120">Usage Example</span></span>


```
Texture3D<float4> tex;
uint mip = 2;
uint3 pos_xyz = {123, 456, 789};
float4 f = tex.mips[mip][pos_xyz];
        
```



<span data-ttu-id="ac438-121">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="ac438-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="ac438-122">Sommet</span><span class="sxs-lookup"><span data-stu-id="ac438-122">Vertex</span></span> | <span data-ttu-id="ac438-123">Forme</span><span class="sxs-lookup"><span data-stu-id="ac438-123">Hull</span></span> | <span data-ttu-id="ac438-124">Domain</span><span class="sxs-lookup"><span data-stu-id="ac438-124">Domain</span></span> | <span data-ttu-id="ac438-125">Géométrie</span><span class="sxs-lookup"><span data-stu-id="ac438-125">Geometry</span></span> | <span data-ttu-id="ac438-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="ac438-126">Pixel</span></span> | <span data-ttu-id="ac438-127">Compute</span><span class="sxs-lookup"><span data-stu-id="ac438-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ac438-128">x</span><span class="sxs-lookup"><span data-stu-id="ac438-128">x</span></span>      | <span data-ttu-id="ac438-129">x</span><span class="sxs-lookup"><span data-stu-id="ac438-129">x</span></span>    | <span data-ttu-id="ac438-130">x</span><span class="sxs-lookup"><span data-stu-id="ac438-130">x</span></span>      | <span data-ttu-id="ac438-131">x</span><span class="sxs-lookup"><span data-stu-id="ac438-131">x</span></span>        | <span data-ttu-id="ac438-132">x</span><span class="sxs-lookup"><span data-stu-id="ac438-132">x</span></span>     | <span data-ttu-id="ac438-133">x</span><span class="sxs-lookup"><span data-stu-id="ac438-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ac438-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ac438-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac438-135">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ac438-135">Texture3D</span></span>](sm5-object-texture3d.md)
</dt> <dt>

[<span data-ttu-id="ac438-136">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="ac438-136">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




