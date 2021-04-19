---
description: Calcule le produit transposé de deux matrices.
ms.assetid: 43927500-9413-41a4-a6ee-974d85dd1054
title: D3DXMatrixMultiplyTranspose, fonction (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b599453ae108a5a8bab8ee896858760c85799948
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522334"
---
# <a name="d3dxmatrixmultiplytranspose-function-d3dx9mathh"></a><span data-ttu-id="0b1b4-103">D3DXMatrixMultiplyTranspose, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="0b1b4-103">D3DXMatrixMultiplyTranspose function (D3dx9math.h)</span></span>

<span data-ttu-id="0b1b4-104">Calcule le produit transposé de deux matrices.</span><span class="sxs-lookup"><span data-stu-id="0b1b4-104">Calculates the transposed product of two matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b1b4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0b1b4-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixMultiplyTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a><span data-ttu-id="0b1b4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0b1b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b1b4-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0b1b4-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0b1b4-108">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="0b1b4-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0b1b4-109">Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="0b1b4-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="0b1b4-110">*pM1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0b1b4-110">*pM1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b1b4-111">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="0b1b4-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0b1b4-112">Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) source.</span><span class="sxs-lookup"><span data-stu-id="0b1b4-112">Pointer to a source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0b1b4-113">*pM2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0b1b4-113">*pM2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b1b4-114">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="0b1b4-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0b1b4-115">Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) source.</span><span class="sxs-lookup"><span data-stu-id="0b1b4-115">Pointer to a source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b1b4-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0b1b4-116">Return value</span></span>

<span data-ttu-id="0b1b4-117">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="0b1b4-117">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0b1b4-118">Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) qui est le produit de deux matrices.</span><span class="sxs-lookup"><span data-stu-id="0b1b4-118">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the product of two matrices.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b1b4-119">Notes</span><span class="sxs-lookup"><span data-stu-id="0b1b4-119">Remarks</span></span>

<span data-ttu-id="0b1b4-120">Le résultat est le transpose du produit de deux matrices de transformation, out = T (M1 \* m2).</span><span class="sxs-lookup"><span data-stu-id="0b1b4-120">The result is the transposed of the product of two transformation matrices, Out = T(M1\*M2).</span></span>

<span data-ttu-id="0b1b4-121">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="0b1b4-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="0b1b4-122">De cette façon, la fonction **D3DXMatrixMultiplyTranspose** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="0b1b4-122">In this way, the **D3DXMatrixMultiplyTranspose** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="0b1b4-123">Cette fonction est utile pour définir des matrices en tant que constantes pour les nuanceurs de sommets et de pixels.</span><span class="sxs-lookup"><span data-stu-id="0b1b4-123">This function is useful to set matrices as constants for vertex and pixel shaders.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b1b4-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0b1b4-124">Requirements</span></span>



| <span data-ttu-id="0b1b4-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0b1b4-125">Requirement</span></span> | <span data-ttu-id="0b1b4-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b1b4-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b1b4-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="0b1b4-127">Header</span></span><br/>  | <dl> <span data-ttu-id="0b1b4-128"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b1b4-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="0b1b4-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0b1b4-129">Library</span></span><br/> | <dl> <span data-ttu-id="0b1b4-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0b1b4-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0b1b4-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b1b4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b1b4-132">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="0b1b4-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="0b1b4-133">**D3DXMatrixMultiply**</span><span class="sxs-lookup"><span data-stu-id="0b1b4-133">**D3DXMatrixMultiply**</span></span>](d3dxmatrixmultiply.md)
</dt> <dt>

[<span data-ttu-id="0b1b4-134">**D3DXQuaternionMultiply**</span><span class="sxs-lookup"><span data-stu-id="0b1b4-134">**D3DXQuaternionMultiply**</span></span>](d3dxquaternionmultiply.md)
</dt> </dl>

 

 




