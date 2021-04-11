---
description: Utilise une interpolation linéaire pour créer une valeur de couleur.
ms.assetid: bf7bf2f4-5fb5-44d3-a7e5-7998640d7d49
title: D3DXColorLerp, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorLerp
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3521ee9e76aecd486093f903d336c08553e0e4ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870126"
---
# <a name="d3dxcolorlerp-function"></a><span data-ttu-id="7441f-103">D3DXColorLerp fonction)</span><span class="sxs-lookup"><span data-stu-id="7441f-103">D3DXColorLerp function</span></span>

<span data-ttu-id="7441f-104">Utilise une interpolation linéaire pour créer une valeur de couleur.</span><span class="sxs-lookup"><span data-stu-id="7441f-104">Uses linear interpolation to create a color value.</span></span>

## <a name="syntax"></a><span data-ttu-id="7441f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7441f-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorLerp(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC1,
  _In_    const D3DXCOLOR *pC2,
  _In_          FLOAT     s
);
```



## <a name="parameters"></a><span data-ttu-id="7441f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7441f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7441f-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7441f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7441f-108">Type : **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="7441f-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="7441f-109">Pointeur vers une structure [**D3DXCOLOR**](d3dxcolor.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="7441f-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="7441f-110">*PC1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7441f-110">*pC1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7441f-111">Type : **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="7441f-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="7441f-112">Pointeur vers une structure [**D3DXCOLOR**](d3dxcolor.md) source.</span><span class="sxs-lookup"><span data-stu-id="7441f-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7441f-113">*pC2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7441f-113">*pC2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7441f-114">Type : **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="7441f-114">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="7441f-115">Pointeur vers une structure [**D3DXCOLOR**](d3dxcolor.md) source.</span><span class="sxs-lookup"><span data-stu-id="7441f-115">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7441f-116"> \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7441f-116">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7441f-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7441f-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7441f-118">Paramètre qui interpole de manière linéaire entre les couleurs pC1 et pC2, en les traitant à la fois comme vecteurs 4D.</span><span class="sxs-lookup"><span data-stu-id="7441f-118">Parameter that linearly interpolates between the colors, pC1 and pC2, treating them both as 4D vectors.</span></span> <span data-ttu-id="7441f-119">La valeur de s n’est pas limitée.</span><span class="sxs-lookup"><span data-stu-id="7441f-119">There are no limits on the value of s.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7441f-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7441f-120">Return value</span></span>

<span data-ttu-id="7441f-121">Type : **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="7441f-121">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="7441f-122">Cette fonction retourne un pointeur vers une structure [**D3DXCOLOR**](d3dxcolor.md) qui est le résultat de l’interpolation linéaire.</span><span class="sxs-lookup"><span data-stu-id="7441f-122">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the linear interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="7441f-123">Notes</span><span class="sxs-lookup"><span data-stu-id="7441f-123">Remarks</span></span>

<span data-ttu-id="7441f-124">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="7441f-124">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="7441f-125">De cette façon, la fonction **D3DXColorLerp** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="7441f-125">In this way, the **D3DXColorLerp** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="7441f-126">Cette fonction interpole les composants rouge, vert, bleu et alpha d’une structure [**D3DXCOLOR**](d3dxcolor.md) entre deux couleurs, comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="7441f-126">This function interpolates the red, green, blue, and alpha components of a [**D3DXCOLOR**](d3dxcolor.md) structure between two colors, as shown in the following example.</span></span>


```
   
pOut->r = pC1->r + s * (pC2->r - pC1->r);
```



<span data-ttu-id="7441f-127">Si vous effectuez une interpolation linéaire entre les couleurs A et B, et que s est égal à 0, la couleur résultante est. Si s est 1, la couleur résultante est la couleur B.</span><span class="sxs-lookup"><span data-stu-id="7441f-127">If you are linearly interpolating between the colors A and B, and s is 0, the resulting color is A. If s is 1, the resulting color is color B.</span></span>

## <a name="requirements"></a><span data-ttu-id="7441f-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7441f-128">Requirements</span></span>



| <span data-ttu-id="7441f-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7441f-129">Requirement</span></span> | <span data-ttu-id="7441f-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="7441f-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7441f-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="7441f-131">Header</span></span><br/>  | <dl> <span data-ttu-id="7441f-132"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="7441f-132"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="7441f-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7441f-133">Library</span></span><br/> | <dl> <span data-ttu-id="7441f-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7441f-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7441f-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7441f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7441f-136">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="7441f-136">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="7441f-137">**D3DXColorModulate**</span><span class="sxs-lookup"><span data-stu-id="7441f-137">**D3DXColorModulate**</span></span>](d3dxcolormodulate.md)
</dt> <dt>

[<span data-ttu-id="7441f-138">**D3DXColorNegative**</span><span class="sxs-lookup"><span data-stu-id="7441f-138">**D3DXColorNegative**</span></span>](d3dxcolornegative.md)
</dt> <dt>

[<span data-ttu-id="7441f-139">**D3DXColorScale**</span><span class="sxs-lookup"><span data-stu-id="7441f-139">**D3DXColorScale**</span></span>](d3dxcolorscale.md)
</dt> </dl>

 

 
