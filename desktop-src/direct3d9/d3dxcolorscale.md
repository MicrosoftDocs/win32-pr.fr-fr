---
description: Met à l’échelle une valeur de couleur.
ms.assetid: 35e8adee-7ce5-4db5-8276-f0e408748e78
title: D3DXColorScale, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorScale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 74020f302a26162df1e42cb4c9f020af3f64e59c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106527282"
---
# <a name="d3dxcolorscale-function"></a><span data-ttu-id="0899f-103">D3DXColorScale fonction)</span><span class="sxs-lookup"><span data-stu-id="0899f-103">D3DXColorScale function</span></span>

<span data-ttu-id="0899f-104">Met à l’échelle une valeur de couleur.</span><span class="sxs-lookup"><span data-stu-id="0899f-104">Scales a color value.</span></span>

## <a name="syntax"></a><span data-ttu-id="0899f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0899f-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorScale(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC,
  _In_          FLOAT     s
);
```



## <a name="parameters"></a><span data-ttu-id="0899f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0899f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0899f-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0899f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0899f-108">Type : **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="0899f-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="0899f-109">Pointeur vers une structure [**D3DXCOLOR**](d3dxcolor.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="0899f-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="0899f-110">*ordinateur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0899f-110">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0899f-111">Type : **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="0899f-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="0899f-112">Pointeur vers une structure [**D3DXCOLOR**](d3dxcolor.md) source.</span><span class="sxs-lookup"><span data-stu-id="0899f-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0899f-113"> \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0899f-113">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0899f-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0899f-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0899f-115">Facteur d’échelle.</span><span class="sxs-lookup"><span data-stu-id="0899f-115">Scale factor.</span></span> <span data-ttu-id="0899f-116">Il met à l’échelle la couleur, en la traitant comme un vecteur 4D.</span><span class="sxs-lookup"><span data-stu-id="0899f-116">It scales the color, treating it like a 4D vector.</span></span> <span data-ttu-id="0899f-117">La valeur de s n’est pas limitée.</span><span class="sxs-lookup"><span data-stu-id="0899f-117">There are no limits on the value of s.</span></span> <span data-ttu-id="0899f-118">Si s est 1, la couleur résultante est la couleur d’origine.</span><span class="sxs-lookup"><span data-stu-id="0899f-118">If s is 1, the resulting color is the original color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0899f-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0899f-119">Return value</span></span>

<span data-ttu-id="0899f-120">Type : **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="0899f-120">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="0899f-121">Cette fonction retourne un pointeur vers une structure [**D3DXCOLOR**](d3dxcolor.md) qui est la valeur de couleur mise à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="0899f-121">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the scaled color value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0899f-122">Notes</span><span class="sxs-lookup"><span data-stu-id="0899f-122">Remarks</span></span>

<span data-ttu-id="0899f-123">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="0899f-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="0899f-124">De cette façon, la fonction **D3DXColorScale** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="0899f-124">In this way, the **D3DXColorScale** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="0899f-125">Cette fonction calcule la valeur de couleur mise à l’échelle en multipliant les composants de couleur de la structure [**D3DXCOLOR**](d3dxcolor.md) par le facteur d’échelle spécifié, comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="0899f-125">This function computes the scaled color value by multiplying the color components of the [**D3DXCOLOR**](d3dxcolor.md) structure by the specified scale factor, as shown in the following example.</span></span>


```
pOut->r = pC->r * s;
```



## <a name="requirements"></a><span data-ttu-id="0899f-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0899f-126">Requirements</span></span>



| <span data-ttu-id="0899f-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0899f-127">Requirement</span></span> | <span data-ttu-id="0899f-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="0899f-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0899f-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="0899f-129">Header</span></span><br/>  | <dl> <span data-ttu-id="0899f-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="0899f-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="0899f-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0899f-131">Library</span></span><br/> | <dl> <span data-ttu-id="0899f-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0899f-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0899f-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0899f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0899f-134">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="0899f-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="0899f-135">**D3DXColorLerp**</span><span class="sxs-lookup"><span data-stu-id="0899f-135">**D3DXColorLerp**</span></span>](d3dxcolorlerp.md)
</dt> <dt>

[<span data-ttu-id="0899f-136">**D3DXColorModulate**</span><span class="sxs-lookup"><span data-stu-id="0899f-136">**D3DXColorModulate**</span></span>](d3dxcolormodulate.md)
</dt> <dt>

[<span data-ttu-id="0899f-137">**D3DXColorNegative**</span><span class="sxs-lookup"><span data-stu-id="0899f-137">**D3DXColorNegative**</span></span>](d3dxcolornegative.md)
</dt> </dl>

 

 
