---
description: Crée la valeur de couleur négative d’une valeur de couleur.
ms.assetid: 74143126-93f8-49fa-abe3-fd730b644d87
title: D3DXColorNegative, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorNegative
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a6d4d8559e64580897aec5261c450dc739496e75
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106542165"
---
# <a name="d3dxcolornegative-function"></a><span data-ttu-id="a9fb7-103">D3DXColorNegative fonction)</span><span class="sxs-lookup"><span data-stu-id="a9fb7-103">D3DXColorNegative function</span></span>

<span data-ttu-id="a9fb7-104">Crée la valeur de couleur négative d’une valeur de couleur.</span><span class="sxs-lookup"><span data-stu-id="a9fb7-104">Creates the negative color value of a color value.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9fb7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a9fb7-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorNegative(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC
);
```



## <a name="parameters"></a><span data-ttu-id="a9fb7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a9fb7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9fb7-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a9fb7-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a9fb7-108">Type : **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="a9fb7-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="a9fb7-109">Pointeur vers une structure [**D3DXCOLOR**](d3dxcolor.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="a9fb7-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a9fb7-110">*ordinateur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a9fb7-110">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9fb7-111">Type : **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="a9fb7-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="a9fb7-112">Pointeur vers une structure [**D3DXCOLOR**](d3dxcolor.md) source.</span><span class="sxs-lookup"><span data-stu-id="a9fb7-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9fb7-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a9fb7-113">Return value</span></span>

<span data-ttu-id="a9fb7-114">Type : **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="a9fb7-114">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="a9fb7-115">Cette fonction retourne un pointeur vers une structure [**D3DXCOLOR**](d3dxcolor.md) qui est la valeur de couleur négative de la valeur de couleur.</span><span class="sxs-lookup"><span data-stu-id="a9fb7-115">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the negative color value of the color value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9fb7-116">Notes</span><span class="sxs-lookup"><span data-stu-id="a9fb7-116">Remarks</span></span>

<span data-ttu-id="a9fb7-117">Le canal alpha d’entrée est copié, sans modification, sur le canal alpha de sortie.</span><span class="sxs-lookup"><span data-stu-id="a9fb7-117">The input alpha channel is copied, unmodified, to the output alpha channel.</span></span>

<span data-ttu-id="a9fb7-118">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="a9fb7-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="a9fb7-119">De cette façon, la fonction **D3DXColorNegative** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="a9fb7-119">In this way, the **D3DXColorNegative** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="a9fb7-120">Cette fonction retourne la valeur de couleur négative en soustrayant 1,0 des composants de couleur de la structure [**D3DXCOLOR**](d3dxcolor.md) , comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="a9fb7-120">This function returns the negative color value by subtracting 1.0 from the color components of the [**D3DXCOLOR**](d3dxcolor.md) structure, as shown in the following example.</span></span>


```
pOut->r = 1.0f - pC->r;
```



## <a name="requirements"></a><span data-ttu-id="a9fb7-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a9fb7-121">Requirements</span></span>



| <span data-ttu-id="a9fb7-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a9fb7-122">Requirement</span></span> | <span data-ttu-id="a9fb7-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9fb7-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9fb7-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="a9fb7-124">Header</span></span><br/>  | <dl> <span data-ttu-id="a9fb7-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9fb7-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="a9fb7-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a9fb7-126">Library</span></span><br/> | <dl> <span data-ttu-id="a9fb7-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a9fb7-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a9fb7-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9fb7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9fb7-129">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="a9fb7-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="a9fb7-130">**D3DXColorLerp**</span><span class="sxs-lookup"><span data-stu-id="a9fb7-130">**D3DXColorLerp**</span></span>](d3dxcolorlerp.md)
</dt> <dt>

[<span data-ttu-id="a9fb7-131">**D3DXColorModulate**</span><span class="sxs-lookup"><span data-stu-id="a9fb7-131">**D3DXColorModulate**</span></span>](d3dxcolormodulate.md)
</dt> <dt>

[<span data-ttu-id="a9fb7-132">**D3DXColorScale**</span><span class="sxs-lookup"><span data-stu-id="a9fb7-132">**D3DXColorScale**</span></span>](d3dxcolorscale.md)
</dt> </dl>

 

 




