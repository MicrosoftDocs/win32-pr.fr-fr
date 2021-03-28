---
title: 'Texture2DMS :: Sample. Operator, fonction'
description: 'Récupère une valeur de la ressource à l’emplacement et l’exemple d’index fournis. | Texture2DMS :: Sample. Operator, fonction'
ms.assetid: 5bc24129-b690-44dd-ae85-8533b10befaa
keywords:
- exemple. Fonction d’opérateur HLSL
topic_type:
- apiref
api_name:
- sample.Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1a73577fa67992b212b4769059f1523e584acbaf
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211629"
---
# <a name="texture2dmssampleoperator----function"></a><span data-ttu-id="e7e46-105">Texture2DMS :: Sample. Operator, fonction</span><span class="sxs-lookup"><span data-stu-id="e7e46-105">Texture2DMS::sample.Operator    function</span></span>

<span data-ttu-id="e7e46-106">Récupère une valeur de la ressource à l’emplacement et l’exemple d’index fournis.</span><span class="sxs-lookup"><span data-stu-id="e7e46-106">Retrieves a value from the resource at the location and sample index provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7e46-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e7e46-107">Syntax</span></span>

``` syntax
R sample.Operator[][](
  in uint sampleSlice,
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="e7e46-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7e46-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7e46-109">*sampleSlice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7e46-109">*sampleSlice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7e46-110">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="e7e46-110">Type: **uint**</span></span>

<span data-ttu-id="e7e46-111">Exemple d’index de la tranche.</span><span class="sxs-lookup"><span data-stu-id="e7e46-111">The sample slice index.</span></span>

</dd> <dt>

<span data-ttu-id="e7e46-112">*pos* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7e46-112">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7e46-113">Type : **uint2**</span><span class="sxs-lookup"><span data-stu-id="e7e46-113">Type: **uint2**</span></span>

<span data-ttu-id="e7e46-114">Position d’index.</span><span class="sxs-lookup"><span data-stu-id="e7e46-114">The index position.</span></span> <span data-ttu-id="e7e46-115">Les composants contiennent les coordonnées (x, y).</span><span class="sxs-lookup"><span data-stu-id="e7e46-115">The components contain the (x, y) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7e46-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e7e46-116">Return value</span></span>

<span data-ttu-id="e7e46-117">Type : **R**</span><span class="sxs-lookup"><span data-stu-id="e7e46-117">Type: **R**</span></span>

<span data-ttu-id="e7e46-118">Variable de ressource en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="e7e46-118">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7e46-119">Notes</span><span class="sxs-lookup"><span data-stu-id="e7e46-119">Remarks</span></span>

### <a name="usage-example"></a><span data-ttu-id="e7e46-120">Exemple d'utilisation</span><span class="sxs-lookup"><span data-stu-id="e7e46-120">Usage Example</span></span>


```
Texture2DMS<float4, 8> tex;

float4 main( float3 tcoord : texturecoord0 ) : SV_Target
{
     return s_msTexture.sample[2][tcoord];
}
```



<span data-ttu-id="e7e46-121">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="e7e46-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="e7e46-122">Sommet</span><span class="sxs-lookup"><span data-stu-id="e7e46-122">Vertex</span></span> | <span data-ttu-id="e7e46-123">Forme</span><span class="sxs-lookup"><span data-stu-id="e7e46-123">Hull</span></span> | <span data-ttu-id="e7e46-124">Domain</span><span class="sxs-lookup"><span data-stu-id="e7e46-124">Domain</span></span> | <span data-ttu-id="e7e46-125">Géométrie</span><span class="sxs-lookup"><span data-stu-id="e7e46-125">Geometry</span></span> | <span data-ttu-id="e7e46-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="e7e46-126">Pixel</span></span> | <span data-ttu-id="e7e46-127">Compute</span><span class="sxs-lookup"><span data-stu-id="e7e46-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="e7e46-128">x</span><span class="sxs-lookup"><span data-stu-id="e7e46-128">x</span></span>      | <span data-ttu-id="e7e46-129">x</span><span class="sxs-lookup"><span data-stu-id="e7e46-129">x</span></span>    | <span data-ttu-id="e7e46-130">x</span><span class="sxs-lookup"><span data-stu-id="e7e46-130">x</span></span>      | <span data-ttu-id="e7e46-131">x</span><span class="sxs-lookup"><span data-stu-id="e7e46-131">x</span></span>        | <span data-ttu-id="e7e46-132">x</span><span class="sxs-lookup"><span data-stu-id="e7e46-132">x</span></span>     | <span data-ttu-id="e7e46-133">x</span><span class="sxs-lookup"><span data-stu-id="e7e46-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="e7e46-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7e46-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7e46-135">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="e7e46-135">Texture2DMS</span></span>](sm5-object-texture2dms.md)
</dt> <dt>

[<span data-ttu-id="e7e46-136">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="e7e46-136">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




