---
description: 'Fonction D3DXColorAdjustSaturation (D3dx9math. h) : ajuste la valeur de saturation d’une couleur.'
ms.assetid: 1f66c3b4-2f02-4993-80c6-c484180c2459
title: D3DXColorAdjustSaturation, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorAdjustSaturation
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 878cdd83a04f594da3133eda314486af96ac3d56
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115867"
---
# <a name="d3dxcoloradjustsaturation-function-d3dx9mathh"></a><span data-ttu-id="47f0a-103">D3DXColorAdjustSaturation, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="47f0a-103">D3DXColorAdjustSaturation function (D3dx9math.h)</span></span>

<span data-ttu-id="47f0a-104">Ajuste la valeur de saturation d’une couleur.</span><span class="sxs-lookup"><span data-stu-id="47f0a-104">Adjusts the saturation value of a color.</span></span>

## <a name="syntax"></a><span data-ttu-id="47f0a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="47f0a-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorAdjustSaturation(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC,
  _In_          FLOAT     s
);
```



## <a name="parameters"></a><span data-ttu-id="47f0a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="47f0a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47f0a-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="47f0a-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="47f0a-108">Type : **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="47f0a-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="47f0a-109">Pointeur vers une structure [**D3DXCOLOR**](d3dxcolor.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="47f0a-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="47f0a-110">*ordinateur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="47f0a-110">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47f0a-111">Type : **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="47f0a-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="47f0a-112">Pointeur vers une structure [**D3DXCOLOR**](d3dxcolor.md) source.</span><span class="sxs-lookup"><span data-stu-id="47f0a-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="47f0a-113"> \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="47f0a-113">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47f0a-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="47f0a-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="47f0a-115">Valeur de saturation.</span><span class="sxs-lookup"><span data-stu-id="47f0a-115">Saturation value.</span></span> <span data-ttu-id="47f0a-116">Ce paramètre interpole de manière linéaire entre la couleur convertie en nuances de gris et la couleur d’origine, pC.</span><span class="sxs-lookup"><span data-stu-id="47f0a-116">This parameter linearly interpolates between the color converted to grayscale and the original color, pC.</span></span> <span data-ttu-id="47f0a-117">La valeur de s n’est pas limitée.</span><span class="sxs-lookup"><span data-stu-id="47f0a-117">There are no limits on the value of s.</span></span> <span data-ttu-id="47f0a-118">Si s est égal à 0, la couleur retournée est la couleur de nuances de gris.</span><span class="sxs-lookup"><span data-stu-id="47f0a-118">If s is 0, the returned color is the grayscale color.</span></span> <span data-ttu-id="47f0a-119">Si s est 1, la couleur retournée est la couleur d’origine.</span><span class="sxs-lookup"><span data-stu-id="47f0a-119">If s is 1, the returned color is the original color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47f0a-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="47f0a-120">Return value</span></span>

<span data-ttu-id="47f0a-121">Type : **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="47f0a-121">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="47f0a-122">Cette fonction retourne un pointeur vers une structure [**D3DXCOLOR**](d3dxcolor.md) qui est le résultat de l’ajustement de saturation.</span><span class="sxs-lookup"><span data-stu-id="47f0a-122">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the saturation adjustment.</span></span>

## <a name="remarks"></a><span data-ttu-id="47f0a-123">Notes </span><span class="sxs-lookup"><span data-stu-id="47f0a-123">Remarks</span></span>

<span data-ttu-id="47f0a-124">Le canal alpha d’entrée est copié, sans modification, sur le canal alpha de sortie.</span><span class="sxs-lookup"><span data-stu-id="47f0a-124">The input alpha channel is copied, unmodified, to the output alpha channel.</span></span>

<span data-ttu-id="47f0a-125">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="47f0a-125">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="47f0a-126">De cette façon, cette fonction peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="47f0a-126">In this way, this function can be used as a parameter for another function.</span></span>

<span data-ttu-id="47f0a-127">Cette fonction interpole les composants de couleur rouge, vert et bleu d’une structure [**D3DXCOLOR**](d3dxcolor.md) entre une couleur insaturée et une couleur, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="47f0a-127">This function interpolates the red, green, and blue color components of a [**D3DXCOLOR**](d3dxcolor.md) structure between an unsaturated color and a color, as shown in the following example.</span></span>


```
    // Approximate values for each component's contribution to luminance.
    // Based upon the NTSC standard described in ITU-R Recommendation BT.709.
    FLOAT grey = pC->r * 0.2125f + pC->g * 0.7154f + pC->b * 0.0721f;
    
    pOut->r = grey + s * (pC->r - grey);
```



<span data-ttu-id="47f0a-128">Si s est supérieur à 0 et inférieur à 1, la saturation est réduite.</span><span class="sxs-lookup"><span data-stu-id="47f0a-128">If s is greater than 0 and less than 1, the saturation is decreased.</span></span> <span data-ttu-id="47f0a-129">Si s est supérieur à 1, la saturation est augmentée.</span><span class="sxs-lookup"><span data-stu-id="47f0a-129">If s is greater than 1, the saturation is increased.</span></span>

<span data-ttu-id="47f0a-130">La couleur de nuances de gris est calculée comme suit :</span><span class="sxs-lookup"><span data-stu-id="47f0a-130">The grayscale color is computed as:</span></span>


```
r = g = b = 0.2125*r + 0.7154*g + 0.0721*b
```



## <a name="requirements"></a><span data-ttu-id="47f0a-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="47f0a-131">Requirements</span></span>



| <span data-ttu-id="47f0a-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="47f0a-132">Requirement</span></span> | <span data-ttu-id="47f0a-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="47f0a-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="47f0a-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="47f0a-134">Header</span></span><br/>  | <dl> <span data-ttu-id="47f0a-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="47f0a-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="47f0a-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="47f0a-136">Library</span></span><br/> | <dl> <span data-ttu-id="47f0a-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="47f0a-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="47f0a-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47f0a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47f0a-139">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="47f0a-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="47f0a-140">**D3DXColorAdjustContrast**</span><span class="sxs-lookup"><span data-stu-id="47f0a-140">**D3DXColorAdjustContrast**</span></span>](d3dxcoloradjustcontrast.md)
</dt> </dl>

 

 
