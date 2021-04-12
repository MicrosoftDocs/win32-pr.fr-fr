---
description: Fusionne deux couleurs.
ms.assetid: deff70c7-2359-48b2-ab40-8c418acf5a07
title: D3DXColorModulate, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorModulate
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cf9b202da786f6ec87ceca9816c2a4fc86776577
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211834"
---
# <a name="d3dxcolormodulate-function"></a><span data-ttu-id="c9978-103">D3DXColorModulate fonction)</span><span class="sxs-lookup"><span data-stu-id="c9978-103">D3DXColorModulate function</span></span>

<span data-ttu-id="c9978-104">Fusionne deux couleurs.</span><span class="sxs-lookup"><span data-stu-id="c9978-104">Blends two colors.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9978-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9978-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorModulate(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC1,
  _In_    const D3DXCOLOR *pC2
);
```



## <a name="parameters"></a><span data-ttu-id="c9978-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9978-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9978-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c9978-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9978-108">Type : **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="c9978-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="c9978-109">Pointeur vers une structure [**D3DXCOLOR**](d3dxcolor.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="c9978-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c9978-110">*PC1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c9978-110">*pC1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9978-111">Type : **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="c9978-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="c9978-112">Pointeur vers une structure [**D3DXCOLOR**](d3dxcolor.md) source.</span><span class="sxs-lookup"><span data-stu-id="c9978-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c9978-113">*pC2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c9978-113">*pC2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9978-114">Type : **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="c9978-114">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="c9978-115">Pointeur vers une structure [**D3DXCOLOR**](d3dxcolor.md) source.</span><span class="sxs-lookup"><span data-stu-id="c9978-115">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9978-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c9978-116">Return value</span></span>

<span data-ttu-id="c9978-117">Type : **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="c9978-117">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="c9978-118">Cette fonction retourne un pointeur vers une structure [**D3DXCOLOR**](d3dxcolor.md) qui est le résultat de l’opération de fusion.</span><span class="sxs-lookup"><span data-stu-id="c9978-118">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the blending operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9978-119">Notes</span><span class="sxs-lookup"><span data-stu-id="c9978-119">Remarks</span></span>

<span data-ttu-id="c9978-120">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="c9978-120">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="c9978-121">De cette façon, la fonction **D3DXColorModulate** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="c9978-121">In this way, the **D3DXColorModulate** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="c9978-122">Cette fonction fusionne deux couleurs en multipliant les composants de couleur correspondants, comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="c9978-122">This function blends together two colors by multiplying matching color components, as shown in the following example.</span></span>


```
pOut->r = pC1->r * pC2->r;
```



## <a name="requirements"></a><span data-ttu-id="c9978-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c9978-123">Requirements</span></span>



| <span data-ttu-id="c9978-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c9978-124">Requirement</span></span> | <span data-ttu-id="c9978-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9978-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9978-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="c9978-126">Header</span></span><br/>  | <dl> <span data-ttu-id="c9978-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9978-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c9978-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c9978-128">Library</span></span><br/> | <dl> <span data-ttu-id="c9978-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c9978-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c9978-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9978-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9978-131">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="c9978-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="c9978-132">**D3DXColorLerp**</span><span class="sxs-lookup"><span data-stu-id="c9978-132">**D3DXColorLerp**</span></span>](d3dxcolorlerp.md)
</dt> <dt>

[<span data-ttu-id="c9978-133">**D3DXColorNegative**</span><span class="sxs-lookup"><span data-stu-id="c9978-133">**D3DXColorNegative**</span></span>](d3dxcolornegative.md)
</dt> <dt>

[<span data-ttu-id="c9978-134">**D3DXColorScale**</span><span class="sxs-lookup"><span data-stu-id="c9978-134">**D3DXColorScale**</span></span>](d3dxcolorscale.md)
</dt> </dl>

 

 




