---
description: Soustrait deux valeurs de couleur pour créer une nouvelle valeur de couleur.
ms.assetid: c21f8402-c1c2-4909-896f-2872ef518537
title: D3DXColorSubtract, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorSubtract
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 47f28ea3a3fb6d1556e699fed3820e228faf6604
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522357"
---
# <a name="d3dxcolorsubtract-function"></a><span data-ttu-id="ee7de-103">D3DXColorSubtract fonction)</span><span class="sxs-lookup"><span data-stu-id="ee7de-103">D3DXColorSubtract function</span></span>

<span data-ttu-id="ee7de-104">Soustrait deux valeurs de couleur pour créer une nouvelle valeur de couleur.</span><span class="sxs-lookup"><span data-stu-id="ee7de-104">Subtracts two color values to create a new color value.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee7de-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ee7de-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorSubtract(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC1,
  _In_    const D3DXCOLOR *pC2
);
```



## <a name="parameters"></a><span data-ttu-id="ee7de-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ee7de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee7de-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ee7de-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee7de-108">Type : **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="ee7de-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="ee7de-109">Pointeur vers une structure [**D3DXCOLOR**](d3dxcolor.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="ee7de-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ee7de-110">*PC1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ee7de-110">*pC1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee7de-111">Type : **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="ee7de-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="ee7de-112">Pointeur vers une structure [**D3DXCOLOR**](d3dxcolor.md) source.</span><span class="sxs-lookup"><span data-stu-id="ee7de-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="ee7de-113">*pC2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ee7de-113">*pC2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee7de-114">Type : **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="ee7de-114">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="ee7de-115">Pointeur vers une structure [**D3DXCOLOR**](d3dxcolor.md) source.</span><span class="sxs-lookup"><span data-stu-id="ee7de-115">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee7de-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ee7de-116">Return value</span></span>

<span data-ttu-id="ee7de-117">Type : **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="ee7de-117">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="ee7de-118">Cette fonction retourne un pointeur vers une structure [**D3DXCOLOR**](d3dxcolor.md) qui est la différence entre deux valeurs de couleur.</span><span class="sxs-lookup"><span data-stu-id="ee7de-118">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the difference between two color values.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee7de-119">Notes</span><span class="sxs-lookup"><span data-stu-id="ee7de-119">Remarks</span></span>

<span data-ttu-id="ee7de-120">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="ee7de-120">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="ee7de-121">De cette façon, la fonction **D3DXColorSubtract** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="ee7de-121">In this way, the **D3DXColorSubtract** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee7de-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ee7de-122">Requirements</span></span>



| <span data-ttu-id="ee7de-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ee7de-123">Requirement</span></span> | <span data-ttu-id="ee7de-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee7de-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee7de-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="ee7de-125">Header</span></span><br/>  | <dl> <span data-ttu-id="ee7de-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee7de-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="ee7de-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ee7de-127">Library</span></span><br/> | <dl> <span data-ttu-id="ee7de-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ee7de-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ee7de-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee7de-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee7de-130">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="ee7de-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="ee7de-131">**D3DXColorAdd**</span><span class="sxs-lookup"><span data-stu-id="ee7de-131">**D3DXColorAdd**</span></span>](d3dxcoloradd.md)
</dt> </dl>

 

 




