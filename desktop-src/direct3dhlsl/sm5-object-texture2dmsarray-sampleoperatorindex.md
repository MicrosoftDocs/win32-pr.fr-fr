---
title: 'Texture2DMSArray :: Sample. Operator, fonction'
description: 'Retourne une variable de ressource en lecture seule. | Texture2DMSArray :: Sample. Operator, fonction'
ms.assetid: 5334c1d5-dfbd-4987-875c-0b92967b0f13
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
ms.openlocfilehash: e78746e0afe03e65a313982ca35c27a75ea14f1b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974379"
---
# <a name="texture2dmsarraysampleoperator----function"></a><span data-ttu-id="b8f9d-105">Texture2DMSArray :: Sample. Operator, fonction</span><span class="sxs-lookup"><span data-stu-id="b8f9d-105">Texture2DMSArray::sample.Operator    function</span></span>

<span data-ttu-id="b8f9d-106">Retourne une variable de ressource en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8f9d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b8f9d-107">Syntax</span></span>

``` syntax
R sample.Operator[][](
  in uint sampleSlice,
  in uint3 pos
);
```

## <a name="parameters"></a><span data-ttu-id="b8f9d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b8f9d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8f9d-109">*sampleSlice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b8f9d-109">*sampleSlice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8f9d-110">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="b8f9d-110">Type: **uint**</span></span>

<span data-ttu-id="b8f9d-111">Exemple d’index de la tranche.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-111">The sample slice index.</span></span>

</dd> <dt>

<span data-ttu-id="b8f9d-112">*pos* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b8f9d-112">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8f9d-113">Type : **uint3**</span><span class="sxs-lookup"><span data-stu-id="b8f9d-113">Type: **uint3**</span></span>

<span data-ttu-id="b8f9d-114">Position d’index.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-114">The index position.</span></span> <span data-ttu-id="b8f9d-115">Le premier et le deuxième composant contiennent les coordonnées (x, y).</span><span class="sxs-lookup"><span data-stu-id="b8f9d-115">The first and second components contain the (x, y) coordinates.</span></span> <span data-ttu-id="b8f9d-116">Le troisième composant indique la tranche de tableau souhaitée.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-116">The third component indicates the desired array slice.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8f9d-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b8f9d-117">Return value</span></span>

<span data-ttu-id="b8f9d-118">Type : **R**</span><span class="sxs-lookup"><span data-stu-id="b8f9d-118">Type: **R**</span></span>

<span data-ttu-id="b8f9d-119">Variable de ressource en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-119">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8f9d-120">Notes</span><span class="sxs-lookup"><span data-stu-id="b8f9d-120">Remarks</span></span>

### <a name="usage-example"></a><span data-ttu-id="b8f9d-121">Exemple d'utilisation</span><span class="sxs-lookup"><span data-stu-id="b8f9d-121">Usage Example</span></span>


```
Texture2DMSArray<float4, 4> alpha;

float4 main( float3 tcoord : texturecoord0 ) : SV_Target
{
     return s_msTexture.sample[2][tcoord];
}
```



<span data-ttu-id="b8f9d-122">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="b8f9d-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="b8f9d-123">Sommet</span><span class="sxs-lookup"><span data-stu-id="b8f9d-123">Vertex</span></span> | <span data-ttu-id="b8f9d-124">Forme</span><span class="sxs-lookup"><span data-stu-id="b8f9d-124">Hull</span></span> | <span data-ttu-id="b8f9d-125">Domain</span><span class="sxs-lookup"><span data-stu-id="b8f9d-125">Domain</span></span> | <span data-ttu-id="b8f9d-126">Géométrie</span><span class="sxs-lookup"><span data-stu-id="b8f9d-126">Geometry</span></span> | <span data-ttu-id="b8f9d-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="b8f9d-127">Pixel</span></span> | <span data-ttu-id="b8f9d-128">Compute</span><span class="sxs-lookup"><span data-stu-id="b8f9d-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="b8f9d-129">x</span><span class="sxs-lookup"><span data-stu-id="b8f9d-129">x</span></span>      | <span data-ttu-id="b8f9d-130">x</span><span class="sxs-lookup"><span data-stu-id="b8f9d-130">x</span></span>    | <span data-ttu-id="b8f9d-131">x</span><span class="sxs-lookup"><span data-stu-id="b8f9d-131">x</span></span>      | <span data-ttu-id="b8f9d-132">x</span><span class="sxs-lookup"><span data-stu-id="b8f9d-132">x</span></span>        | <span data-ttu-id="b8f9d-133">x</span><span class="sxs-lookup"><span data-stu-id="b8f9d-133">x</span></span>     | <span data-ttu-id="b8f9d-134">x</span><span class="sxs-lookup"><span data-stu-id="b8f9d-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="b8f9d-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8f9d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8f9d-136">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="b8f9d-136">Texture2DMSArray</span></span>](sm5-object-texture2dmsarray.md)
</dt> <dt>

[<span data-ttu-id="b8f9d-137">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="b8f9d-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




