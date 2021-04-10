---
description: Transforme le vecteur 2D normal par la matrice donnée.
ms.assetid: aa9adf6d-5aae-4acf-bbd9-f5c14d90470e
title: D3DXVec2TransformNormal, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformNormal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 154268b272f6cac00acb1d770d3c919cf65d6297
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953876"
---
# <a name="d3dxvec2transformnormal-function-d3dx9mathh"></a><span data-ttu-id="bcf45-103">D3DXVec2TransformNormal, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="bcf45-103">D3DXVec2TransformNormal function (D3dx9math.h)</span></span>

<span data-ttu-id="bcf45-104">Transforme le vecteur 2D normal par la matrice donnée.</span><span class="sxs-lookup"><span data-stu-id="bcf45-104">Transforms the 2D vector normal by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcf45-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bcf45-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformNormal(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="bcf45-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bcf45-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcf45-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="bcf45-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bcf45-108">Type : **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="bcf45-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="bcf45-109">Pointeur vers la structure [**D3DXVECTOR2**](d3dxvector2.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="bcf45-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="bcf45-110">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bcf45-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcf45-111">Type : **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="bcf45-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="bcf45-112">Pointeur vers la structure [**D3DXVECTOR2**](d3dxvector2.md) source.</span><span class="sxs-lookup"><span data-stu-id="bcf45-112">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="bcf45-113">*GCF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bcf45-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcf45-114">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="bcf45-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="bcf45-115">Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) source.</span><span class="sxs-lookup"><span data-stu-id="bcf45-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcf45-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bcf45-116">Return value</span></span>

<span data-ttu-id="bcf45-117">Type : **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="bcf45-117">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="bcf45-118">Pointeur vers une structure [**D3DXVECTOR2**](d3dxvector2.md) qui est le vecteur transformé.</span><span class="sxs-lookup"><span data-stu-id="bcf45-118">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="bcf45-119">Notes</span><span class="sxs-lookup"><span data-stu-id="bcf45-119">Remarks</span></span>

<span data-ttu-id="bcf45-120">Cette fonction transforme le vecteur (*PV-*>x, *PV-*>y, 0, 0) par la matrice désignée par *PM*.</span><span class="sxs-lookup"><span data-stu-id="bcf45-120">This function transforms the vector (*pV-*>x, *pV-*>y, 0, 0) by the matrix pointed to by *pM*.</span></span>

<span data-ttu-id="bcf45-121">Si vous souhaitez transformer un normal, la matrice que vous transmettez à cette fonction doit être la transposer de l’inverse de la matrice que vous utiliseriez pour transformer un point.</span><span class="sxs-lookup"><span data-stu-id="bcf45-121">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="bcf45-122">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="bcf45-122">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="bcf45-123">De cette façon, la fonction **D3DXVec2TransformNormal** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="bcf45-123">In this way, the **D3DXVec2TransformNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcf45-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bcf45-124">Requirements</span></span>



| <span data-ttu-id="bcf45-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bcf45-125">Requirement</span></span> | <span data-ttu-id="bcf45-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="bcf45-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bcf45-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="bcf45-127">Header</span></span><br/>  | <dl> <span data-ttu-id="bcf45-128"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="bcf45-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="bcf45-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bcf45-129">Library</span></span><br/> | <dl> <span data-ttu-id="bcf45-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bcf45-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bcf45-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bcf45-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcf45-132">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="bcf45-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="bcf45-133">**D3DXVec2Transform**</span><span class="sxs-lookup"><span data-stu-id="bcf45-133">**D3DXVec2Transform**</span></span>](d3dxvec2transform.md)
</dt> <dt>

[<span data-ttu-id="bcf45-134">**D3DXVec2TransformCoord**</span><span class="sxs-lookup"><span data-stu-id="bcf45-134">**D3DXVec2TransformCoord**</span></span>](d3dxvec2transformcoord.md)
</dt> </dl>

 

 




