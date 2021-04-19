---
description: Calcule le produit transposé de deux matrices.
ms.assetid: 3db4138c-407c-47b5-b8b9-04af8771e98e
title: D3DXMatrixMultiplyTranspose, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixMultiplyTranspose
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 187912a4117ab502ea7b0b1b3fc1ea105ecbc3e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106532478"
---
# <a name="d3dxmatrixmultiplytranspose-function-d3dx10mathh"></a><span data-ttu-id="802fd-103">D3DXMatrixMultiplyTranspose, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="802fd-103">D3DXMatrixMultiplyTranspose function (D3DX10Math.h)</span></span>

<span data-ttu-id="802fd-104">Calcule le produit transposé de deux matrices.</span><span class="sxs-lookup"><span data-stu-id="802fd-104">Calculates the transposed product of two matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="802fd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="802fd-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixMultiplyTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a><span data-ttu-id="802fd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="802fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="802fd-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="802fd-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="802fd-108">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="802fd-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="802fd-109">Pointeur vers la structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="802fd-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="802fd-110">*pM1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="802fd-110">*pM1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="802fd-111">Type : **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="802fd-111">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="802fd-112">Pointeur vers une structure source D3DXMATRIX (côté gauche).</span><span class="sxs-lookup"><span data-stu-id="802fd-112">Pointer to a source D3DXMATRIX structure (left hand side).</span></span>

</dd> <dt>

<span data-ttu-id="802fd-113">*pM2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="802fd-113">*pM2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="802fd-114">Type : **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="802fd-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="802fd-115">Pointeur vers une structure source D3DXMATRIX (à droite).</span><span class="sxs-lookup"><span data-stu-id="802fd-115">Pointer to a source D3DXMATRIX structure (right hand side).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="802fd-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="802fd-116">Return value</span></span>

<span data-ttu-id="802fd-117">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="802fd-117">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="802fd-118">Pointeur vers une structure D3DXMATRIX qui est le produit de deux matrices.</span><span class="sxs-lookup"><span data-stu-id="802fd-118">Pointer to a D3DXMATRIX structure that is the product of two matrices.</span></span>

## <a name="remarks"></a><span data-ttu-id="802fd-119">Notes</span><span class="sxs-lookup"><span data-stu-id="802fd-119">Remarks</span></span>

<span data-ttu-id="802fd-120">Le résultat est le transpose du produit de deux matrices de transformation, out = T (M1 \* m2).</span><span class="sxs-lookup"><span data-stu-id="802fd-120">The result is the transposed of the product of two transformation matrices, Out = T(M1\*M2).</span></span>

<span data-ttu-id="802fd-121">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="802fd-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="802fd-122">De cette façon, la fonction D3DXMatrixMultiplyTranspose peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="802fd-122">In this way, the D3DXMatrixMultiplyTranspose function can be used as a parameter for another function.</span></span>

<span data-ttu-id="802fd-123">Cette fonction est utile pour définir des matrices en tant que constantes pour les nuanceurs de sommets et de pixels.</span><span class="sxs-lookup"><span data-stu-id="802fd-123">This function is useful to set matrices as constants for vertex and pixel shaders.</span></span>

## <a name="requirements"></a><span data-ttu-id="802fd-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="802fd-124">Requirements</span></span>



| <span data-ttu-id="802fd-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="802fd-125">Requirement</span></span> | <span data-ttu-id="802fd-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="802fd-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="802fd-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="802fd-127">Header</span></span><br/>  | <dl> <span data-ttu-id="802fd-128"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="802fd-128"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="802fd-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="802fd-129">Library</span></span><br/> | <dl> <span data-ttu-id="802fd-130"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="802fd-130"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="802fd-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="802fd-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="802fd-132">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="802fd-132">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
