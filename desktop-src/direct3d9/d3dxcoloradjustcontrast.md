---
description: 'D3DXColorAdjustContrast, fonction (D3dx9math. h) : ajuste la valeur de contraste d’une couleur.'
ms.assetid: be49c9c7-b625-4cbc-bd63-1d5766ae2dbb
title: D3DXColorAdjustContrast, fonction (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9dc9bb79d1ebbe536661347d76d13846dead6aa8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115877"
---
# <a name="d3dxcoloradjustcontrast-function-d3dx9mathh"></a><span data-ttu-id="f409e-103">D3DXColorAdjustContrast, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="f409e-103">D3DXColorAdjustContrast function (D3dx9math.h)</span></span>

<span data-ttu-id="f409e-104">Ajuste la valeur de contraste d’une couleur.</span><span class="sxs-lookup"><span data-stu-id="f409e-104">Adjusts the contrast value of a color.</span></span>

## <a name="syntax"></a><span data-ttu-id="f409e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f409e-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorAdjustContrast(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC,
  _In_          FLOAT     c
);
```



## <a name="parameters"></a><span data-ttu-id="f409e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f409e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f409e-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f409e-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f409e-108">Type : **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="f409e-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="f409e-109">Pointeur vers une structure [**D3DXCOLOR**](d3dxcolor.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="f409e-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f409e-110">*ordinateur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f409e-110">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f409e-111">Type : **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="f409e-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="f409e-112">Pointeur vers une structure [**D3DXCOLOR**](d3dxcolor.md) source.</span><span class="sxs-lookup"><span data-stu-id="f409e-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f409e-113">*c* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f409e-113">*c* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f409e-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f409e-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f409e-115">Valeur de contraste.</span><span class="sxs-lookup"><span data-stu-id="f409e-115">Contrast value.</span></span> <span data-ttu-id="f409e-116">Ce paramètre interpole de manière linéaire entre 50% de gris et la couleur, le pC.</span><span class="sxs-lookup"><span data-stu-id="f409e-116">This parameter linearly interpolates between fifty percent gray and the color, pC.</span></span> <span data-ttu-id="f409e-117">Il n’y a pas de limites sur la valeur de c.</span><span class="sxs-lookup"><span data-stu-id="f409e-117">There are not limits on the value of c.</span></span> <span data-ttu-id="f409e-118">Si ce paramètre est égal à zéro, la couleur retournée est 50% de gris.</span><span class="sxs-lookup"><span data-stu-id="f409e-118">If this parameter is zero, then the returned color is fifty percent gray.</span></span> <span data-ttu-id="f409e-119">Si ce paramètre est 1, la couleur retournée est la couleur d’origine.</span><span class="sxs-lookup"><span data-stu-id="f409e-119">If this parameter is 1, then the returned color is the original color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f409e-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f409e-120">Return value</span></span>

<span data-ttu-id="f409e-121">Type : **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="f409e-121">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="f409e-122">Cette fonction retourne un pointeur vers une structure [**D3DXCOLOR**](d3dxcolor.md) qui est le résultat de l’ajustement du contraste.</span><span class="sxs-lookup"><span data-stu-id="f409e-122">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the contrast adjustment.</span></span>

## <a name="remarks"></a><span data-ttu-id="f409e-123">Notes </span><span class="sxs-lookup"><span data-stu-id="f409e-123">Remarks</span></span>

<span data-ttu-id="f409e-124">Le canal alpha d’entrée est copié, sans modification, sur le canal alpha de sortie.</span><span class="sxs-lookup"><span data-stu-id="f409e-124">The input alpha channel is copied, unmodified, to the output alpha channel.</span></span>

<span data-ttu-id="f409e-125">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="f409e-125">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="f409e-126">De cette façon, cette fonction peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="f409e-126">In this way, this function can be used as a parameter for another function.</span></span>

<span data-ttu-id="f409e-127">Cette fonction interpole les composants de couleur rouge, vert et bleu d’une structure [**D3DXCOLOR**](d3dxcolor.md) entre 50% de gris et une valeur de contraste spécifiée, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="f409e-127">This function interpolates the red, green, and blue color components of a [**D3DXCOLOR**](d3dxcolor.md) structure between fifty percent gray and a specified contrast value, as shown in the following example.</span></span>


```
pOut->r = 0.5f + c * (pC->r - 0.5f);
```



<span data-ttu-id="f409e-128">Si c est supérieur à 0 et inférieur à 1, le contraste est réduit.</span><span class="sxs-lookup"><span data-stu-id="f409e-128">If c is greater than 0 and less than 1, the contrast is decreased.</span></span> <span data-ttu-id="f409e-129">Si c est supérieur à 1, le contraste est augmenté.</span><span class="sxs-lookup"><span data-stu-id="f409e-129">If c is greater than 1, the contrast is increased.</span></span>

## <a name="requirements"></a><span data-ttu-id="f409e-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f409e-130">Requirements</span></span>



| <span data-ttu-id="f409e-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f409e-131">Requirement</span></span> | <span data-ttu-id="f409e-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="f409e-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f409e-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="f409e-133">Header</span></span><br/>  | <dl> <span data-ttu-id="f409e-134"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f409e-134"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="f409e-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f409e-135">Library</span></span><br/> | <dl> <span data-ttu-id="f409e-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f409e-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f409e-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f409e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f409e-138">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="f409e-138">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="f409e-139">**D3DXColorAdjustSaturation**</span><span class="sxs-lookup"><span data-stu-id="f409e-139">**D3DXColorAdjustSaturation**</span></span>](d3dxcoloradjustsaturation.md)
</dt> </dl>

 

 
