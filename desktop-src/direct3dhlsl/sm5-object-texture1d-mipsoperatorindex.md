---
title: 'Texture1D :: MIPS. Operator, fonction'
description: Retourne une variable de ressource en lecture seule ou un Texture1D.
ms.assetid: 0b64f0d3-f9a1-474b-b229-d91d18922d5c
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
ms.openlocfilehash: 4713fe20fa52e948113a220969229c413c5dc4d1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104317069"
---
# <a name="texture1dmipsoperator----function"></a><span data-ttu-id="9efce-104">Texture1D :: MIPS. Operator, fonction</span><span class="sxs-lookup"><span data-stu-id="9efce-104">Texture1D::mips.Operator    function</span></span>

<span data-ttu-id="9efce-105">Retourne une variable de ressource en lecture seule ou un [**Texture1D**](sm5-object-texture1d.md).</span><span class="sxs-lookup"><span data-stu-id="9efce-105">Returns a read-only resource variable or a [**Texture1D**](sm5-object-texture1d.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9efce-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9efce-106">Syntax</span></span>

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint pos
);
```

## <a name="parameters"></a><span data-ttu-id="9efce-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9efce-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9efce-108">*mipSlice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9efce-108">*mipSlice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9efce-109">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="9efce-109">Type: **uint**</span></span>

<span data-ttu-id="9efce-110">Index de la tranche MIP.</span><span class="sxs-lookup"><span data-stu-id="9efce-110">The mip slice index.</span></span>

</dd> <dt>

<span data-ttu-id="9efce-111">*pos* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9efce-111">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9efce-112">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="9efce-112">Type: **uint**</span></span>

<span data-ttu-id="9efce-113">Position d’index.</span><span class="sxs-lookup"><span data-stu-id="9efce-113">The index position.</span></span> <span data-ttu-id="9efce-114">Contient la coordonnée x.</span><span class="sxs-lookup"><span data-stu-id="9efce-114">Contains the x-coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9efce-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9efce-115">Return value</span></span>

<span data-ttu-id="9efce-116">Type : **R**</span><span class="sxs-lookup"><span data-stu-id="9efce-116">Type: **R**</span></span>

<span data-ttu-id="9efce-117">Variable de ressource en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="9efce-117">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="9efce-118">Notes</span><span class="sxs-lookup"><span data-stu-id="9efce-118">Remarks</span></span>

### <a name="usage-example"></a><span data-ttu-id="9efce-119">Exemple d'utilisation</span><span class="sxs-lookup"><span data-stu-id="9efce-119">Usage Example</span></span>


```
Texture1D<float4> tex;
uint mip = 2;
uint pos = 1234;
float4 f = tex.mips[mip][pos];
      
```



<span data-ttu-id="9efce-120">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="9efce-120">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="9efce-121">Sommet</span><span class="sxs-lookup"><span data-stu-id="9efce-121">Vertex</span></span> | <span data-ttu-id="9efce-122">Forme</span><span class="sxs-lookup"><span data-stu-id="9efce-122">Hull</span></span> | <span data-ttu-id="9efce-123">Domain</span><span class="sxs-lookup"><span data-stu-id="9efce-123">Domain</span></span> | <span data-ttu-id="9efce-124">Géométrie</span><span class="sxs-lookup"><span data-stu-id="9efce-124">Geometry</span></span> | <span data-ttu-id="9efce-125">Pixel</span><span class="sxs-lookup"><span data-stu-id="9efce-125">Pixel</span></span> | <span data-ttu-id="9efce-126">Compute</span><span class="sxs-lookup"><span data-stu-id="9efce-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="9efce-127">x</span><span class="sxs-lookup"><span data-stu-id="9efce-127">x</span></span>      | <span data-ttu-id="9efce-128">x</span><span class="sxs-lookup"><span data-stu-id="9efce-128">x</span></span>    | <span data-ttu-id="9efce-129">x</span><span class="sxs-lookup"><span data-stu-id="9efce-129">x</span></span>      | <span data-ttu-id="9efce-130">x</span><span class="sxs-lookup"><span data-stu-id="9efce-130">x</span></span>        | <span data-ttu-id="9efce-131">x</span><span class="sxs-lookup"><span data-stu-id="9efce-131">x</span></span>     | <span data-ttu-id="9efce-132">x</span><span class="sxs-lookup"><span data-stu-id="9efce-132">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="9efce-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9efce-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9efce-134">Texture1D</span><span class="sxs-lookup"><span data-stu-id="9efce-134">Texture1D</span></span>](sm5-object-texture1d.md)
</dt> <dt>

[<span data-ttu-id="9efce-135">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="9efce-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




