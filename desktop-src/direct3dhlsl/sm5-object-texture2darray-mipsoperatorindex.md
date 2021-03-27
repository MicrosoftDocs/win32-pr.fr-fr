---
title: 'Texture2DArray :: MIPS. Operator, fonction'
description: 'Retourne une variable de ressource en lecture seule. | Texture2DArray :: MIPS. Operator, fonction'
ms.assetid: 66639bf6-74dd-4c69-9cc1-74cc9314de57
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
ms.openlocfilehash: 17f24dd54768f3583f508527b7e03f72399bf98e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761827"
---
# <a name="texture2darraymipsoperator----function"></a><span data-ttu-id="ed0ca-105">Texture2DArray :: MIPS. Operator, fonction</span><span class="sxs-lookup"><span data-stu-id="ed0ca-105">Texture2DArray::mips.Operator    function</span></span>

<span data-ttu-id="ed0ca-106">Retourne une variable de ressource en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="ed0ca-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed0ca-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ed0ca-107">Syntax</span></span>

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint3 pos
);
```

## <a name="parameters"></a><span data-ttu-id="ed0ca-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ed0ca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed0ca-109">*mipSlice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ed0ca-109">*mipSlice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed0ca-110">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="ed0ca-110">Type: **uint**</span></span>

<span data-ttu-id="ed0ca-111">Index de la tranche MIP.</span><span class="sxs-lookup"><span data-stu-id="ed0ca-111">The mip slice index.</span></span>

</dd> <dt>

<span data-ttu-id="ed0ca-112">*pos* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ed0ca-112">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed0ca-113">Type : **uint3**</span><span class="sxs-lookup"><span data-stu-id="ed0ca-113">Type: **uint3**</span></span>

<span data-ttu-id="ed0ca-114">Position d’index.</span><span class="sxs-lookup"><span data-stu-id="ed0ca-114">The index position.</span></span> <span data-ttu-id="ed0ca-115">Le premier et le deuxième composant contiennent les coordonnées (x, y).</span><span class="sxs-lookup"><span data-stu-id="ed0ca-115">The first and second components contain the (x, y) coordinates.</span></span> <span data-ttu-id="ed0ca-116">Le troisième composant indique la tranche de tableau souhaitée.</span><span class="sxs-lookup"><span data-stu-id="ed0ca-116">The third component indicates the desired array slice.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed0ca-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ed0ca-117">Return value</span></span>

<span data-ttu-id="ed0ca-118">Type : **R**</span><span class="sxs-lookup"><span data-stu-id="ed0ca-118">Type: **R**</span></span>

<span data-ttu-id="ed0ca-119">Variable de ressource en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="ed0ca-119">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed0ca-120">Notes</span><span class="sxs-lookup"><span data-stu-id="ed0ca-120">Remarks</span></span>

### <a name="usage-example"></a><span data-ttu-id="ed0ca-121">Exemple d'utilisation</span><span class="sxs-lookup"><span data-stu-id="ed0ca-121">Usage Example</span></span>


```
Texture2DArray<float4> tex;
uint mip = 2;
uint2 pos_xy_and_array = {123, 456, 3};
float4 f = tex.mips[mip][pos_xy_and_array];
        
```



<span data-ttu-id="ed0ca-122">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="ed0ca-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="ed0ca-123">Sommet</span><span class="sxs-lookup"><span data-stu-id="ed0ca-123">Vertex</span></span> | <span data-ttu-id="ed0ca-124">Forme</span><span class="sxs-lookup"><span data-stu-id="ed0ca-124">Hull</span></span> | <span data-ttu-id="ed0ca-125">Domain</span><span class="sxs-lookup"><span data-stu-id="ed0ca-125">Domain</span></span> | <span data-ttu-id="ed0ca-126">Géométrie</span><span class="sxs-lookup"><span data-stu-id="ed0ca-126">Geometry</span></span> | <span data-ttu-id="ed0ca-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="ed0ca-127">Pixel</span></span> | <span data-ttu-id="ed0ca-128">Compute</span><span class="sxs-lookup"><span data-stu-id="ed0ca-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ed0ca-129">x</span><span class="sxs-lookup"><span data-stu-id="ed0ca-129">x</span></span>      | <span data-ttu-id="ed0ca-130">x</span><span class="sxs-lookup"><span data-stu-id="ed0ca-130">x</span></span>    | <span data-ttu-id="ed0ca-131">x</span><span class="sxs-lookup"><span data-stu-id="ed0ca-131">x</span></span>      | <span data-ttu-id="ed0ca-132">x</span><span class="sxs-lookup"><span data-stu-id="ed0ca-132">x</span></span>        | <span data-ttu-id="ed0ca-133">x</span><span class="sxs-lookup"><span data-stu-id="ed0ca-133">x</span></span>     | <span data-ttu-id="ed0ca-134">x</span><span class="sxs-lookup"><span data-stu-id="ed0ca-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ed0ca-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed0ca-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed0ca-136">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="ed0ca-136">Texture2DArray</span></span>](sm5-object-texture2darray.md)
</dt> <dt>

[<span data-ttu-id="ed0ca-137">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="ed0ca-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




