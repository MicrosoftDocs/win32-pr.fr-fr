---
description: Transforme le vecteur 2D normal par la matrice donnée.
ms.assetid: fc238bb1-155f-4018-9c92-16352726920d
title: D3DXVec2TransformNormal, fonction (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c4043a8f5a57f14be3e8506dc257690ef581835d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953866"
---
# <a name="d3dxvec2transformnormal-function-d3dx10mathh"></a><span data-ttu-id="986cc-103">D3DXVec2TransformNormal, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="986cc-103">D3DXVec2TransformNormal function (D3DX10Math.h)</span></span>

<span data-ttu-id="986cc-104">Transforme le vecteur 2D normal par la matrice donnée.</span><span class="sxs-lookup"><span data-stu-id="986cc-104">Transforms the 2D vector normal by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="986cc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="986cc-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformNormal(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="986cc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="986cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="986cc-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="986cc-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="986cc-108">Type : **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="986cc-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="986cc-109">Pointeur vers le [**D3DXVECTOR2**](d3d10-d3dxvector2.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="986cc-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="986cc-110">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="986cc-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="986cc-111">Type : **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="986cc-111">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="986cc-112">Pointeur vers la structure D3DXVECTOR2 source.</span><span class="sxs-lookup"><span data-stu-id="986cc-112">Pointer to the source D3DXVECTOR2 structure.</span></span>

</dd> <dt>

<span data-ttu-id="986cc-113">*GCF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="986cc-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="986cc-114">Type : **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="986cc-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="986cc-115">Pointeur vers la structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) source.</span><span class="sxs-lookup"><span data-stu-id="986cc-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="986cc-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="986cc-116">Return value</span></span>

<span data-ttu-id="986cc-117">Type : **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="986cc-117">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="986cc-118">Pointeur vers une structure D3DXVECTOR2 qui est le vecteur transformé.</span><span class="sxs-lookup"><span data-stu-id="986cc-118">Pointer to a D3DXVECTOR2 structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="986cc-119">Notes</span><span class="sxs-lookup"><span data-stu-id="986cc-119">Remarks</span></span>

<span data-ttu-id="986cc-120">Cette fonction transforme le vecteur (pV->x, pV->y, 0, 0) par la matrice désignée par pM.</span><span class="sxs-lookup"><span data-stu-id="986cc-120">This function transforms the vector (pV->x, pV->y, 0, 0) by the matrix pointed to by pM.</span></span>

<span data-ttu-id="986cc-121">Si vous souhaitez transformer un normal, la matrice que vous transmettez à cette fonction doit être la transposer de l’inverse de la matrice que vous utiliseriez pour transformer un point.</span><span class="sxs-lookup"><span data-stu-id="986cc-121">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="986cc-122">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="986cc-122">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="986cc-123">De cette façon, la fonction **D3DXVec2TransformNormal** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="986cc-123">In this way, the **D3DXVec2TransformNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="986cc-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="986cc-124">Requirements</span></span>



| <span data-ttu-id="986cc-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="986cc-125">Requirement</span></span> | <span data-ttu-id="986cc-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="986cc-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="986cc-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="986cc-127">Header</span></span><br/>  | <dl> <span data-ttu-id="986cc-128"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="986cc-128"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="986cc-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="986cc-129">Library</span></span><br/> | <dl> <span data-ttu-id="986cc-130"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="986cc-130"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="986cc-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="986cc-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="986cc-132">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="986cc-132">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
