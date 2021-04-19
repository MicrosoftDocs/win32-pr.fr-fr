---
description: Additionne deux valeurs de couleur pour créer une nouvelle valeur de couleur.
ms.assetid: 7743392d-4676-4408-93e9-f92d4bf02411
title: D3DXColorAdd, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorAdd
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f326c9bec4802a9a94accc76b825cd1c6ea28fd5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106542173"
---
# <a name="d3dxcoloradd-function"></a><span data-ttu-id="b5d2f-103">D3DXColorAdd fonction)</span><span class="sxs-lookup"><span data-stu-id="b5d2f-103">D3DXColorAdd function</span></span>

<span data-ttu-id="b5d2f-104">Additionne deux valeurs de couleur pour créer une nouvelle valeur de couleur.</span><span class="sxs-lookup"><span data-stu-id="b5d2f-104">Adds two color values together to create a new color value.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5d2f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b5d2f-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorAdd(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC1,
  _In_    const D3DXCOLOR *pC2
);
```



## <a name="parameters"></a><span data-ttu-id="b5d2f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b5d2f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5d2f-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b5d2f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5d2f-108">Type : **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="b5d2f-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="b5d2f-109">Pointeur vers une structure [**D3DXCOLOR**](d3dxcolor.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="b5d2f-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="b5d2f-110">*PC1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b5d2f-110">*pC1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5d2f-111">Type : **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="b5d2f-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="b5d2f-112">Pointeur vers une structure [**D3DXCOLOR**](d3dxcolor.md) source.</span><span class="sxs-lookup"><span data-stu-id="b5d2f-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b5d2f-113">*pC2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b5d2f-113">*pC2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5d2f-114">Type : **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="b5d2f-114">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="b5d2f-115">Pointeur vers une structure [**D3DXCOLOR**](d3dxcolor.md) source.</span><span class="sxs-lookup"><span data-stu-id="b5d2f-115">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5d2f-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b5d2f-116">Return value</span></span>

<span data-ttu-id="b5d2f-117">Type : **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="b5d2f-117">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="b5d2f-118">Cette fonction retourne un pointeur vers une structure [**D3DXCOLOR**](d3dxcolor.md) qui est la somme de deux valeurs de couleur.</span><span class="sxs-lookup"><span data-stu-id="b5d2f-118">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the sum of two color values.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5d2f-119">Notes</span><span class="sxs-lookup"><span data-stu-id="b5d2f-119">Remarks</span></span>

<span data-ttu-id="b5d2f-120">La valeur de retour de cette fonction est la même que celle retournée dans moue.</span><span class="sxs-lookup"><span data-stu-id="b5d2f-120">The return value for this function is the same value returned in pOut.</span></span> <span data-ttu-id="b5d2f-121">De cette façon, la fonction **D3DXColorAdd** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="b5d2f-121">In this way, the **D3DXColorAdd** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5d2f-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5d2f-122">Requirements</span></span>



| <span data-ttu-id="b5d2f-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5d2f-123">Requirement</span></span> | <span data-ttu-id="b5d2f-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5d2f-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5d2f-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="b5d2f-125">Header</span></span><br/>  | <dl> <span data-ttu-id="b5d2f-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5d2f-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="b5d2f-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b5d2f-127">Library</span></span><br/> | <dl> <span data-ttu-id="b5d2f-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5d2f-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b5d2f-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5d2f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5d2f-130">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="b5d2f-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="b5d2f-131">**D3DXColorModulate**</span><span class="sxs-lookup"><span data-stu-id="b5d2f-131">**D3DXColorModulate**</span></span>](d3dxcolormodulate.md)
</dt> <dt>

[<span data-ttu-id="b5d2f-132">**D3DXColorSubtract**</span><span class="sxs-lookup"><span data-stu-id="b5d2f-132">**D3DXColorSubtract**</span></span>](d3dxcolorsubtract.md)
</dt> </dl>

 

 




