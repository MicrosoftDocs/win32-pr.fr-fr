---
description: Ajuste la valeur de contraste d’une couleur.
ms.assetid: c111d3c7-19c6-4a6b-af0d-a9e1bc0bb7d9
title: D3DXColorAdjustContrast, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorAdjustContrast
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 24586b2a8d2206d6818e00af9ea86e4c5e9758fa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523216"
---
# <a name="d3dxcoloradjustcontrast-function-d3dx10mathh"></a><span data-ttu-id="589d3-103">D3DXColorAdjustContrast, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="589d3-103">D3DXColorAdjustContrast function (D3DX10Math.h)</span></span>

<span data-ttu-id="589d3-104">Ajuste la valeur de contraste d’une couleur.</span><span class="sxs-lookup"><span data-stu-id="589d3-104">Adjusts the contrast value of a color.</span></span>

## <a name="syntax"></a><span data-ttu-id="589d3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="589d3-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorAdjustContrast(
  _In_       D3DXCOLOR *pOut,
  _In_ const D3DXCOLOR *pC,
  _In_       FLOAT     c
);
```



## <a name="parameters"></a><span data-ttu-id="589d3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="589d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="589d3-107">*moue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="589d3-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="589d3-108">Type : **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="589d3-108">Type: **[**D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span></span>

<span data-ttu-id="589d3-109">\[dans, pointeur de sortie \] vers un [**D3DXCOLOR**](d3d10-d3dxcolor.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="589d3-109">\[in, out\] Pointer to a [**D3DXCOLOR**](d3d10-d3dxcolor.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="589d3-110">*ordinateur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="589d3-110">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="589d3-111">Type : **const [**D3DXCOLOR**](../direct3d9/d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="589d3-111">Type: **const [**D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span></span>

<span data-ttu-id="589d3-112">Pointeur vers une structure D3DXCOLOR source.</span><span class="sxs-lookup"><span data-stu-id="589d3-112">Pointer to a source D3DXCOLOR structure.</span></span>

</dd> <dt>

<span data-ttu-id="589d3-113">*c* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="589d3-113">*c* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="589d3-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="589d3-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="589d3-115">Valeur de contraste.</span><span class="sxs-lookup"><span data-stu-id="589d3-115">Contrast value.</span></span> <span data-ttu-id="589d3-116">Ce paramètre interpole de manière linéaire entre 50% de gris et la couleur, le pC.</span><span class="sxs-lookup"><span data-stu-id="589d3-116">This parameter linearly interpolates between fifty percent gray and the color, pC.</span></span> <span data-ttu-id="589d3-117">Il n’existe aucune limite quant à la valeur de c.</span><span class="sxs-lookup"><span data-stu-id="589d3-117">There are no limits on the value of c.</span></span> <span data-ttu-id="589d3-118">Si ce paramètre est égal à zéro, la couleur retournée est 50% de gris.</span><span class="sxs-lookup"><span data-stu-id="589d3-118">If this parameter is zero, then the returned color is fifty percent gray.</span></span> <span data-ttu-id="589d3-119">Si ce paramètre est 1, la couleur retournée est la couleur d’origine.</span><span class="sxs-lookup"><span data-stu-id="589d3-119">If this parameter is 1, then the returned color is the original color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="589d3-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="589d3-120">Return value</span></span>

<span data-ttu-id="589d3-121">Type : **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="589d3-121">Type: **[**D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span></span>

<span data-ttu-id="589d3-122">Cette fonction retourne un pointeur vers une structure D3DXCOLOR qui est le résultat de l’ajustement du contraste.</span><span class="sxs-lookup"><span data-stu-id="589d3-122">This function returns a pointer to a D3DXCOLOR structure that is the result of the contrast adjustment.</span></span>

## <a name="remarks"></a><span data-ttu-id="589d3-123">Notes</span><span class="sxs-lookup"><span data-stu-id="589d3-123">Remarks</span></span>

<span data-ttu-id="589d3-124">Le canal alpha d’entrée est copié, sans modification, sur le canal alpha de sortie.</span><span class="sxs-lookup"><span data-stu-id="589d3-124">The input alpha channel is copied, unmodified, to the output alpha channel.</span></span>

<span data-ttu-id="589d3-125">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="589d3-125">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="589d3-126">De cette façon, cette fonction peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="589d3-126">In this way, this function can be used as a parameter for another function.</span></span>

<span data-ttu-id="589d3-127">Cette fonction interpole les composants de couleur rouge, vert et bleu d’une structure D3DXCOLOR entre 50% de gris et une valeur de contraste spécifiée, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="589d3-127">This function interpolates the red, green, and blue color components of a D3DXCOLOR structure between fifty percent gray and a specified contrast value, as shown in the following example.</span></span>


```
pOut->r = 0.5f + c * (pC->r - 0.5f);
```



<span data-ttu-id="589d3-128">Si c est supérieur à 0 et inférieur à 1, le contraste est réduit.</span><span class="sxs-lookup"><span data-stu-id="589d3-128">If c is greater than 0 and less than 1, the contrast is decreased.</span></span> <span data-ttu-id="589d3-129">Si c est supérieur à 1, le contraste est augmenté.</span><span class="sxs-lookup"><span data-stu-id="589d3-129">If c is greater than 1, the contrast is increased.</span></span>

## <a name="requirements"></a><span data-ttu-id="589d3-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="589d3-130">Requirements</span></span>



| <span data-ttu-id="589d3-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="589d3-131">Requirement</span></span> | <span data-ttu-id="589d3-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="589d3-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="589d3-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="589d3-133">Header</span></span><br/>  | <dl> <span data-ttu-id="589d3-134"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="589d3-134"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="589d3-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="589d3-135">Library</span></span><br/> | <dl> <span data-ttu-id="589d3-136"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="589d3-136"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="589d3-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="589d3-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="589d3-138">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="589d3-138">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
